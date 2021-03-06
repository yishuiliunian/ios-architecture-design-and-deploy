# 组件化

组件，主要是指一簇因可以完成一定的功能聚合在一起的代码、资源、配置文件等组成的一个实体。组件物理形态上的隔离，一般我们会使用目录结构、仓库等方式来完成隔离。

组件化主要是在说物理形态的隔离，核心在与物理（目录结构）上的隔离，即各种资源的物理结构。其中最核心的问题是依赖管理，文件管理、资源管理问题。一般会与 git 、svn 这种版本管理工具扯到一起。比如我们现在使用的Pod、Maven、Pip、Npm等包管理工具解决的主要是组件化的问题。（PS，不要参考前端组件化，前端组件化，和咱们说的组件化完成不是一个概念，他只是说把一个功能单元Package一下）。

通过组件化我们构建出来 SDK 一定的工程结构。并且在该工程结构上，构建出来适合于联盟业务的研发流程。

我们在谈组件化的时候，很多时候我们会谈到“拆库”，然后使用cocoapods在组装起来。而实际上这在谈一个事情“隔离”。

1. 如何做到业务和业务之间的隔离
2. 如何让业务自己独立的发版和迭代节奏
3. 如果进行有效的分层，让业务开发能够不用关注底层的变动

我们做到这些之后，能够给整体的业务提供非常好的扩展能力。而这些是基于“组件”这种结构之上建设起来的。



