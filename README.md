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
