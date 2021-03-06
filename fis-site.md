FIS官网改版发布
--------------

经过一周多的内测，FIS的新官网正式发布了，大家可以通过 http://fis.baidu.com 访问。原FIS-PLUS解决方案可以继续通过 http://fis.baidu.com/fis-plus 访问。

## 背景

FIS开源一年多以来，已经有不少公司基于FIS打造了适应自身业务的前端解决方案，这让我们备受鼓舞，但是FIS不仅仅可以用于打造大型项目的一体化解决方案，也非常适合**个人**或**小型团队**使用，通过很少的配置甚至**零配置**，就可以完成前端项目的自动构建、优化工作。

在过去的一年里，FIS官网历经2次改版，最初的官网从FIS的前端工程化思想出发，从语言能力、资源管理、性能优化等方面给出了FIS自己的思考与解决思路；第二次改版的官网则详细介绍了使用FIS构建的FIS-PLUS解决方案，向大家展示了一个成熟的工程化解决方案，让用户完整的感受FIS的魅力。

我们一直都在强调FIS对前端工程化的解决思路，通过组件化拆分降低系统耦合解决系统复杂度问题；通过FIS的静态资源管理能力，我们可以将业务代码编写与性能优化工作分离，让我们的系统不会因为业务膨胀导致性能的急剧下降。但是FIS实际上是静态资源管理能力的基石，即使没有模块化开发，没有静态资源管理，使用FIS依然可以帮助你完成大量的**构建和优化**工作，因此我们希望让更多的用户了解FIS的这项能力，进一步的引导用户使用FIS。

本次改版是FIS官网的第三次改版。这一次我们更加专注于介绍FIS作为**工具**的能力，同时通过**大量的教程更新**，我们进一步的降低了FIS的使用门槛与学习曲线，希望可以让更多的用户加入FIS社区，让FIS社区更加充满活力！

## 变化

闲话扯了很多了，让我们看看这次FIS官网改版为我们带来了什么

1. 在FIS官网中会将原有的集成解决方案方面的内容迁移到站外，不会在文档中详细的描述，让FIS的学习过程更加平滑和通用。

1. FIS的整体介绍更加面向了使用用户，将FIS的实现原理与细节后置，让大家即使不理解或者不关心FIS的原理，也可以享受FIS带来的便利。

1. 更加完整的快速入门，涵盖了资源压缩、缓存管理、资源合并等方面的内容，阅读完快速入门，你就可以使用FIS完成传统Web项目的优化工作。

1. roadmap.path是FIS配置中最复杂也是功能最强大的一部分。是的，我们也知道光看API文档很难学会(¬､¬)，因此我们专门撰文给出了roadmap.path的实战宝典，帮助大家全面的了解这个神奇的配置。

1. 谈起FIS的模块化思想，其中一个核心就是后端静态资源管理，一提到后端大家也许就有点呆了，自己实现终归不好上手。不过现在也没关系了，我们补充了FIS的纯前端模块化方案，让你不依赖任何后端，也可以享受模块化开发的爽快！

1. 在后端静态资源管理方面，我们也提供了大部分流行语言的实现[DEMO](http://fis.baidu.com/docs/dev/more.html#更多解决方案)，可以帮助有需要的朋友实现更加灵活模块化方案。

1. 嗯，还有一个高大上的首页，以及全新的[视频教学](http://v.youku.com/v_show/id_XNzI1MjQ2OTI0.html)哟，看到最后有彩蛋哟-`д´-

## 后续

1. 文档方面我们会继续根据大家的意见进行调整与补充
1. 静态资源管理与模块化方向将会做进一步的探索，为大家提供更多的选择
1. 解决方案与服务也会进一步的开源，比如Node.js全站解决方案、自动打包服务等等，解决前端开发中的实际问题

## 社区交流

如果在使用过程中遇到了无法解决的问题，可以先查看一下[FAQ](https://github.com/fex-team/fis/issues?labels=faq&page=1&state=open)，我们会定期收集经常被提到的问题。

如果FAQ中也无法找到答案，我们也提供多种渠道解决你的问题。

* **推荐**在Github中提交[Issue](https://github.com/fex-team/fis/issues/new) 
* 在文档评论中提问
* 在QQ交流群315973236中直接沟通

## 参与改进

FIS开发团队非常欢迎大家能够参与到FIS社区发展中，你可以用各种方式帮助FIS，包括但不限于

* 提交BUG，建议以[Issue](https://github.com/fex-team/fis/issues/new)的形式告知我们。
* 提出改进意见，欢迎以Issue的形式向我们提出建议，也可以让更多的人参与讨论。
* 帮助我们调整[FIS文档](https://github.com/fex-team/fis-site)，你同样可以以Issue或者Pull Request的形式调整文档。
* 分享FIS的使用心得，帮助我们推广FIS
* 贡献FIS插件，丰富FIS的功能
* 为FIS核心修复BUG或增加新功能

我们会以开放自由的心态接受大家的意见，我们还会邀请一些活跃的开发者加入FIS核心开发团队。
