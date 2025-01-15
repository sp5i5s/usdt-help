1. [订单](/api/cn/order)

# 📥 提交订单

> 用于生成指定数字货币的支付数据，商户可以通过支付链接引导用户跳转至 UPay 收银台付款。在用户支付成功后，系统将即时进行**回调通知**。
>
> 注意：用户必须严格按照订单金额进行付款，如果付款金额不一致，将会导致**订单无法被处理**。

**请求地址：**/v1/order/apply

**请求方式：**POST

**请求类型：**application/json

**请求参数：**

| 字段名称        | 字段类型 | 是否必填 | 是否签名 | 示例值                              | 说明                                                                                |
| --------------- | -------- | -------- | -------- | ----------------------------------- | ----------------------------------------------------------------------------------- |
| appId           | string   | 是       | 是       | Zu78qwe1                            | APP ID                                                                              |
| merchantOrderNo | string   | 是       | 是       | Order202409291231                   | 商户端自主生成的订单号，在商户端要保证唯一性                                        |
| chainType       | string   | 是       | 是       | 1                                   | 链路：波场(TRC20) 以太坊(ERC20) PayPal(PYUSD)                                       |
| fiatAmount      | string   | 是       | 是       | 50.98                               | 法币金额，精确到小数点后 4 位                                                       |
| attach          | string   | 否       | 否       | 自定义                              | 用户自定义数据，在回调到 notifyUrl 的时候会原样返回                                 |
| notifyUrl       | string   | 是       | 是       | https://callbacknotify.com/callback | 接收异步通知的回调地址。必须为可直接访问的 URL，不能带参数、session 验证、csrf 验证 |
| redirectUrl     | string   | 否       | 否       | https://productdetail.com           | 支付成功后，前端重定向地址。务必包含 http:// 或 https:// 开头                       |
| signature       | string   | 是       | 是       | 6F3B90783FABE56DBB771D03E0EAADD0    | 数据签名                                                                            |

**返回值 data 参数：**

| 字段名称        | 字段类型 | 说明                                         |
| --------------- | -------- | -------------------------------------------- |
| appId           | string   | APP ID                                       |
| orderNo         | string   | UPay 订单号                                  |
| merchantOrderNo | string   | 商户订单号                                   |
| crypto          | string   | 订单金额，单位 USDT / PYUSD                  |
| status          | string   | 订单状态                                     |
| payUrl          | string   | 收银台地址，商户可直接跳转到该地址供用户支付 |
