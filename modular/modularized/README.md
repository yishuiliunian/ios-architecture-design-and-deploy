# 模块化

模块主要是再说运行态的隔离，核心在于运行时能够对于系统资源按照模块进行管控，即运行结构。例如安卓的模块化，会将一个业务模块打成 apk ，然后走动态下发的形式，iOS 如果动态库能够下发的话，基于动态库下发搞的也是模块化（虽然技术上可行，但是过不了 AppStore 的审核）。而模块化则说的是，使用模块这种形式，组织程序逻辑单元在运行时的结构。
