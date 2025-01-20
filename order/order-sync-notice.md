# 🔔订单异步通知

> 订单完成后，系统会自动向订单关联的回调地址（notifyUrl）发送通知消息，告知该笔订单的最终状态。

**请求方式：**POST

**请求类型：**application/json

**请求参数：**

| 字段名称 | 字段类型 | 是否必填 | 是否签名 | 示例值| 说明
| --- | --- | --- | --- | --- | --- |
| app_id | string  | 是  | 是 | Zu78qwe1 | APP ID
|  merchant_order_no |  string | 是  | 是 | Order202409291231 | 商户端自主生成的订单号，在商户端要保证唯一性
|  chain_type | string  |是  | 是 | 1| 链路：波场(TRC20) 以太坊(ERC20) PayPal(PYUSD)  
|  fiat_amount| string  |是  | 是 | 50.98| 法币金额，精确到小数点后 4 位
|  attach| string   |否  | 否 | 自定义 | 用户自定义数据，在回调到  notifyUrl 的时候会原样返回
|  notify_url| string   |是  | 是 | https://callbacknotify.com/callback | 接收异步通知的回调地址。必须为可直接访问的 URL，不能带参数、session 验证、csrf 验证
|  redirect_url| string   |否  | 否 | https://productdetail.com | 支付成功后，前端重定向地址。务必包含 http:// 或 https:// 开头
|  signature | string  |是  | 是 | 6F3B90783FABE56DBB771D03E0EAADD0 | 数据签名

## 通知返回：

商户在收到通知信息后，在响应体的 body 中输出 OK 或者 ok（php例子：echo "OK";) ，否则会重复 5 次发送点对点通知。

## 重试规则如下
如第一次通知失败