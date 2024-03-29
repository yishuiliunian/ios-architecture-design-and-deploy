# 基于组件构建研发流程

架构工作主要是面向工程复杂性的工作，需要通过一定的手段让整个工程的复杂度限制在受控的状态。在软件规模膨胀的情况下，复杂度仍然处于受控的状态。评估架构工作的好坏，可以使用复杂度控制的好坏。架构工作与业务的关系是支撑与约束关系。打个比喻，像是一个牧羊人。既要给羊喂草，又不能让羊儿乱跑。让业务在受控的复杂度下往前奔跑。而我们也在探索使用何种手段能更好的去”牧之“整个工程。而使用工具无疑是比较好的手段。就像在日常开发中我们已经开始大规模的使用cocoapods、cathage、fastlane等工具。

同时，我们也会看到在工程复杂性控制上一个基本的策略就是组件化&模块化。将问题范围缩小。控制在一定范围之内，一个模块所承担的责任越少。他的固有复杂性越低。如果将一个巨大的问题，拆解成一个个小的可控的问题。则更加有利于系统性的复杂性控制。去降低资源管理的粒度,管理一个复杂性更低的”模块“，能将复杂性囿于一隅。因而需要建立起真对细粒度模块构建的整套的工具链。回头看看业界的做法，目前还没有一个事实上的标准来处理这个问题。大部分方案都是基于cocoapods的简单实用。

我们转变一下视角，从以App为基础单元进行开发转变到以模块为基础单元进行开发。原先我们以App为思考的起点，已经构建起了一整套的研发体系。但是，这套体系随着工程规模的扩张我们已经开始逐步的遇到问题，愈来愈臃肿的工程，当个app动辄上百万的代码行数，内部类之间千丝万缕的耦合，重构困难。于是我们开始使用各种手段去“缓解”这些问题，我们引入了模块化使用cocoapods或者cathage对代码进行物理隔离，我们使用fastlane等来简化我们app开发的流程。可以看到此时我们的主要的目标还是“拆”，如何将App中不同的代码拆解到不同的模块中。本质上大家还是在一个宏大的工程中开发。既然我们要进行模块化，那么我们不妨转换一下视角。从“模块”的视角出发。我们开发维护的基础单元就是“模块”，而App只是模块最终“聚合”出来的一个产物。那么我们就需要能够单独开发与维护一个“模块”的能力。每个开发人员只需要关注自己的模块，最终产物app是筛选这些模块然后聚合的产物。他可以是个App，也可以是framework，甚至其他。

软件生产本身也是一种制造业，一般被称之为软件制造业。在传统制造业中已经完成了更加细粒度的分工，有些工厂负责生产原材料，有些工厂负责集成和组装。而我们所谓的模块化，也是这种思路下，从最终产品制造的角度去思考得到的解法。如果严格按照制造业的逻辑，材料是制造业的基础，强大的产品是由强大的基础材料组成。因而，我们需要能够构建强大原材料的方案。

根据[康威定律](https://zh.wikipedia.org/wiki/%E5%BA%B7%E5%A8%81%E5%AE%9A%E5%BE%8B)：设计系统的架构受制于产生这些设计的组织的沟通结构。我们可以很自然的推导出来，组件化其实并非一个单纯的技术问题。因为他希望最终去改造我们整体的工程结构， 也就一样会受限于维护这个工程的组织结构，同样也会影响这个维护这个工程的组织结构。 因而，我们在进行组件化的时候，同时也需要考虑生产这些组件和使用这些组件的组织的结构。

组件化除了影响组件之间的关系，也会通过技术去影响我们的生产关系。 我们把视野拉长一点，发现宏观的组织结构与组件的结构之间，会逐步的趋向于“[同态](https://zh.wikipedia.org/wiki/%E5%90%8C%E6%80%81)“。
