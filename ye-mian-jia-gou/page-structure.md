# 页面架构

这一章聊一聊大家在聊架构的时候，聊的最多的一个问题：页面架构。就是我们如何去组织一个业务单元（包含页面交互）。常见的模式有 MVC，MVP，MVVM 等。其实，在我看来这些页面架构模式，本质上都在说一个问题：如何划分以及组织逻辑职责，并给予一定的结构。拿比较经典的 MVC 来说吧，就是把三部分功能职责进行了拆解：

* model 负责数据模型
* view 负责页面展示及交互
* controller 作为中间的胶水，粘合 model 和 view 。同时，组织两者之间的业务逻辑。

而最近常常被提及的 MVVM ，大概是因为 controller 层职责承载过多，导致了一系列的问题。然后就对其职责进行了进一步的拆解，搞出来一个 view-model 进一步的将业务逻辑拆的粒度更细。基于新的功能职责拆解，页面逻辑组织于是就有了新的结构。

并非说越新的技术越好， MVVM 一定优于 MVC。还是得看和业务本身的契合度。技术先进性是一个需要综合衡量的事情，而非越新越sex的越好。更应该关注和业务本身的契合度。对于不一样的业务场景可能需要不同的页面架构模型。

例如对于交互简单，展示较多的页面，高概率使用系统默认提供的 MVC 框架即可；而对于交互复杂、页面结构复杂的页面可能需要引入 MVVM 架构，可能还需要响应式编程的一些库。

