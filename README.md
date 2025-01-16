
# 💡介绍

本文阅读对象：使用 UPay 收款系统的技术架构师、研发工程师、系统运维工程师。通过本文档，商户可了解 UPay 接入的技术、接入的产品业务、流程、接入规范等信息，以便于商户顺利完成接入工作。

![](https://docs.upay.ink/~gitbook/image?url=https%3A%2F%2F4108688087-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F1pnDJjcXI5yAsWksoEAL%252Fuploads%252FIDVe9w2NP9ID7rRo9EtR%252Fupay.ink.png%3Falt%3Dmedia%26token%3Db9c3b3cc-03d6-4c2c-b04a-37bd09f6697d&width=768&dpr=4&quality=100&sign=f295ee46&sv=2)


## 系统介绍

UPay 是专业的 USDT / PYUSD 支付平台，为商户提供简单易用、安全稳定、不掉单/不撞单，强大的财务管理功能。用户直接付款到您自己的钱包地址，确保您的资金安全，支持 API 收付款。自带 U 风控系统，可以避免您收到黑 U 和标记 U。可个性化功能定制、私有化部署。

## 收款演示


![](https://docs.upay.ink/~gitbook/image?url=https%3A%2F%2F4108688087-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F1pnDJjcXI5yAsWksoEAL%252Fuploads%252FgETQZukSZdv1tnMf9WK6%252FUPay-d1.gif%3Falt%3Dmedia%26token%3Dbeb8190f-f82e-43f8-8aaa-ae19ee8f96d2&width=768&dpr=4&quality=100&sign=b03b47a8&sv=2)

## 在开始接入之前，你需要：


1. 注册并登录 [**商户后台**](http://upay.ac/index.html#/login)
2. 在商户后台查看接入必需的 **appId** 和 **appSecret；**
3. 阅读我们有关 **安全说明** 及 **签名算法** 相关的说明；
4. 然后你可以阅读后续文档，并尝试通过接口发起 [**提交订单**](order/submit-order) 请求。

如你在接入过程中遇到任何问题，可随时联系在线客服和我们取得联系。