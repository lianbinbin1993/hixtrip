# hixtrip 

## 需求
实现一个标准电商平台的一个下单功能

1. 完整实现一个下单功能，包含以下功能：查询SKU价格(模拟，不需要实现)，扣减库存，支付(模拟,不需要实现,但要处理结果回调), 生成订单
2. 围绕下单功能，设计相关业务库表结构，并生成mybatis代码, 至少包括库存、订单

## 技术要求
1. 【10分】基于基础代码实现，要求理解DDD思想, 按示例要求(注意看代码注释和TODO)分层实现下单业务。 
   领域服务已定义, 请注意看代码注释, 并在APP层进行调用。
   业务逻辑使用充血模型
2. 【20分】支付回调使用策略模式(支付成功、支付失败、重复支付)
3. 【10分】基础设施层限制使用mybatis\spring data redis实现（不考虑事务及分布式事务）。
4. 【20分】resources/sql中给出建表语句，包含索引设计。
   其中订单表需要包含分库分表设计，在注释中给出索引、分库键、分表键的设计思路(需要同时满足买家及卖家的高频订单查询)，
   其它特殊数据处理(如历史订单删除等)说明思路即可，考虑越全越优。
5. 【40分】库存扣减需要考虑并发，避免超卖。（按100并发进行设计实现）
