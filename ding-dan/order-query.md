# 🔍订单查询


> 该接口供商户主动查询订单信息。

**请求地址：**/v1/orders/search

**请求方式：**POST

**请求类型：**application/json

**请求参数：**

| 字段名称 | 字段类型 | 是否必填 | 是否签名 | 示例值| 说明
| --- | --- | --- | --- | --- | --- |
| appId | string  | 是  | 是 | Zu78qwe1 | APP ID
|  merchantOrderNo |  string | 是  | 是 | Order202409291231 | 商户端自主生成的订单号，在商户端要保证唯一性
|  signature | string  |是  | 是 | 6F3B90783FABE56DBB771D03E0EAADD0 | 数据签名

**返回值 data 参数：**

| 字段名称 | 字段类型 |  说明
| --- | --- | --- |
| appId | string  | APP ID
|orderNo | string | UPay 订单号
|  merchantOrderNo |  string | 商户订单号
| crypto| string  | 订单金额，单位 USDT / PYUSD
| status | string | 订单状态
|  attach |  string | 用户自定义数据
|  createdAt|  string | 订单创建时间
