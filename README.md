# J ❤ UV

## 项目结构

| 包名 | 子包名 | 描述 | 依赖 |
| ---- | ---- | ---- | ---- |
| domain | ability | 领域服务，即跨实体的服务 | 无 |
| domain | model | 领域模型 | 无 |
| domain | gateway | 基础设施接口 | 无 |
| infrastructure | config | 配置信息 | domain |
| infrastructure | gatewayimpl | 基础设施接口实现 | domain |
| infrastructure | mapper | 数据库mapper | domain |
| client | api | 应用服务接口 | 无 |
| client | dto | 服务DTO | 无 |
| app | consumer | 消息消费者 | domain\client\infrastructure |
| app | executor | 应用服务接口实现 | domain\client\infrastructure |
| app | scheduler | job | domain\client\infrastructure |
| adapter | web | web服务接口 | client |
| adapter | wireless | 无线服务接口 | client |
| starter |  | 启动服务 | client |

## domain层说明

### Entity（实体）
一个对象用来表示某种具有连续性和标识的事物，具备完整的生命周期。

### ValueObject（值对象）
一个对象用来表示某种状态的属性。

### Service（领域服务）
领域某些方面适合用动作表示，某些无状态的活动建模时可以用service表示。

### Aggregate（聚合）
划分出一个范围，这个范围内的模型元素在生命周期的各个阶段都维护固定规则。

### AggregateRoot（聚合根）
聚合中的一个特定实体，外部对象只能引用聚合根。

### Factory（工厂）
生命周期开始阶段，使用工厂创建和重建复杂对象和聚合。

### Repository（存储库）
生命周期中间和末尾阶段，使用存储库来提供持久化。

### 领域事件

## 边界上下文
边界上下文明确限定了模型的应用范围，一个模型只能在一个上下文使用。

### Context Map

## 补充

### Specification（规格）
适合用于进行规则判断，是一种VO。
- 验证
- 选择
- 根据要求创建
