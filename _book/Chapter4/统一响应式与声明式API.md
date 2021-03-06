# 第9节：统一响应式与声明式API

将响应式API与声明式API统一*（**Unifies Imperative and Reactive API**）*

云原生服务使用API提供服务，这些API基于REST、gRPC或thrift等协议。REST通常被用作通过HTTP公开API的最轻量级方式。为了提高性能，gRPC通常用于服务之间的内部通信，也可以使用thrift协议。

云原生中间件承担了运行时为应用动态赋能的重任，应用与中间件以API调用的形式进行通信与控制。响应式API描述为了达到某一个效果或者目标所需要完成的指令；声明式 API 描述的是应用期望的目标状态发出的指令，使系统更加健壮。从云原生理念上来讲，应用无需知道下层中间件及相关资源的具体实现方式，而声明式API使中间件服务调用时无需关注实现细节，在应用运行时动态赋予。

先来看看响应式API的一些特点：1.响应性，是说系统都可以及时的对请求响应，这是一个系统可用性和实用性的基础，是大多数系统应该具有的特性。2.弹性负载，系统可以根据上游的请求的动态压力而动态的对服务进行伸缩。3.消息驱动，通过消息驱动来很好的做系统解耦，以此来划分不同组件的边界。4.柔韧性，系统可以在一定失败的情况下仍然能够响应。以上这些特征都明显的符合云原生服务的特点。

声明式API更是CNCF定义的云原生技术，最为典型的使用就是在k8s中的使用。K8s也是凭借其强大的声明式API、丰富的特性和可扩展性，逐渐成为了容器编排领域的霸主。

大多数开发人员都熟悉命令式编程模，并希望在采用新平台时利用这种经验。同时，开发人员正在迅速采用云主机、事件驱动、异步和反应式模型来满足业务需求，以构建高度并发和响应的应用程序。云原生时代的中间件开发，应将两种开发模型无缝地集成在同一个平台中，从而在一个组织中产生强大的杠杆作用。