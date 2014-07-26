AMD模块化支持
----------------------

## 核心问题

需要解决FIS的目录调整与MD5戳功能和AMD模块联合时的路径问题

以requirejs为例，requirejs中与模块寻找有关的常用配置包括 `path`, `packages`, `baseUrl`，他解决的核心问题实际上和FIS的资源ID与资源路径解决的问题一致。

## 解决思路

1.  将所有模块的ID引用都替换为绝对路径，让用户干掉requirejs所有配置
2.  依然使用原ID，重写requirejs的loader层，让他从一个map.json读取，就和require.async有点类似了

虽然从可行性上都可行，但是方法2用户仍然需要关注require的配置，使用方法1可以将用户的关注点收敛到FIS的roadmap.path配置，同时理论上对AMD规范的其他加载器以及CMD规范的支持也会更加友好。

举个例子，用户使用echarts时，只需要设置roadmap.path使echart的id对应到echarts/echarts.js，echart/xxx/xx的id对应到echarts/xxx/xx.js即可，无需再进行packages设置。

## 处理步骤

1. 将amd模块中所有的相对路径调整为资源ID，针对define、require的参数进行调整，其中require有两种用法均需支持，需要注意的是应主动对无后缀名文件主动添加.js。对于requirejs中使用path和packages定义的ID型参数则无需处理。
  
  ```javascript
  //from
  define(function(require){
    var common = require('./common');
  });
  
  //to
  define(function(require){
    var common = require('js/lib/common');
  });
  ```

  ```javascript
  //from
  define(['./common'], function(common){
  });
  
  //to
  define(['js/lib/common'], function(common){
  });
  ```

  ```javascript
  //from
  require(['./common'], function(common){
  });
  
  //to
  require(['js/lib/common'], function(common){
  });
  ```

1. 对define封装将依赖解析前置，并将资源ID设置为模块ID

  ```javascript
  //from
  define(function(require){
    var common = require('js/lib/common');
  });
  
  //to
  define('amd', ['require', 'js/lib/common'], function(require){
    var common = require('js/lib/common');
  });
  ```

  ```javascript
  //from
  define(['js/lib/common'], function(common){
  });
  
  //to
  define('amd', ['js/lib/common'], function(common){
  });
  ```


1. 完成了路径到ID的替换后，使用requirejs的loader插件，配合map.json输出，将资源ID与实际路径匹配，具体细节包括

  - ID需要添加统一的fis loader前缀
  - 需要考虑其余loader plugin的兼容问题，确定是否可以组合使用，或替代其余loader plugin
  - 具体依赖可以参考autoload插件，按页面解析依赖进行处理
