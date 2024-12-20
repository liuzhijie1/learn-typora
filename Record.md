# Record

## 场景题

### 在处理两个相同请求时，避免前一个请求因网络延迟而返回结果覆盖后一个请求的结果，可以采取以下几种策略

* 请求锁定：通过锁定请求按钮或输入框，确保在上一个请求完成之前，用户无法发起新的请求。这可以通过设置一个 loading 状态来实现。
* 防抖：在用户输入时使用防抖技术，确保只有在用户停止输入一段时间后才发起请求。这可以减少频繁的请求。
* 取消上次的请求： 使用 Axios 的取消令牌，当发起新请求时，如果上次的请求还未完成，则取消它。
* 时序控制：为每个请求分配一个唯一标识符，并在响应到达时检查该标识符。如果响应的标识符是最新的，则处理该响应，否则忽略它。

### graphql 比 restful api 有哪些优点

* 单一端点访问：GraphQL允许通过单个API端点访问所有数据，而RESTful API通常需要多个端点来获取不同资源。这种设计减少了网络请求的数量，提高了效率
* 精确的数据获取：在GraphQL中，客户端可以指定所需的数据字段，避免了过度获取（获取多余数据）和获取不足（未能获取所需数据）的问题。相对而言，RESTful API返回固定结构的数据，可能包含不必要的信息
* 灵活性和可扩展性：GraphQL的强类型系统允许开发者定义灵活的查询结构，使得API可以适应不断变化的前端需求。这种灵活性在处理复杂的前端应用时尤为重要
* 更好的性能: 由于GraphQL能够一次性获取所需的所有数据，它通常比RESTful API更快，尤其是在需要从多个资源中提取信息时。RESTful API可能需要多次请求才能组合所需的数据，这导致了额外的延迟
* 简化微服务架构：GraphQL可以将多个微服务整合到一个统一的API中，使得前端开发者可以更轻松地与后端服务交互，而无需关注各个微服务的细节
