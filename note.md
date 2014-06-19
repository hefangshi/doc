Note
---------------

* https://github.com/node-task/spec task runner的规范标准，目前处于HOLD状态，希望更多的基础库自身就以按照接入task runner的规范进行编写，降低接入难度，想法很赞

* html中引用a.css，但是在文件不存在的情况下fis release一次，html将会保存缓存，这时将a.css文件创建后，由于html的缓存依赖中也没有保存a.css，导致再次编译时，html仍然会命中缓存，不会处理a.css

