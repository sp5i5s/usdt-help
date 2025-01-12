# 常见问题

## 📌常见问题

UPay API 常见问题，如有其他问题请联系客服。

### 下单时提示余额不足 <a href="#xia-dan-shi-ti-shi-yuebu-zu" id="xia-dan-shi-ti-shi-yuebu-zu"></a>

商户需要预充余额用于向我平台支付收款手续费，具体收款手续费率请在商户主页查看。

充值教程：[https://docs.upay.ink/help/cn/howtouse/recharge](https://docs.upay.ink/help/cn/howtouse/recharge?utm_medium=chat\&utm_campaign=link-shared-in-chat\&utm_source=livechat.com\&utm_content=upay.ink)

### 下单时提示需要绑定收款地址 <a href="#xia-dan-shi-ti-shi-xu-yao-bang-ding-shou-kuan-di-zhi" id="xia-dan-shi-ti-shi-xu-yao-bang-ding-shou-kuan-di-zhi"></a>

所有的订单金额都会直接进入商户的收款地址。

收款地址配置教程：[https://docs.upay.ink/help/cn/howtouse/receiving-address](https://docs.upay.ink/help/cn/howtouse/receiving-address?utm_medium=chat\&utm_campaign=link-shared-in-chat\&utm_source=livechat.com\&utm_content=upay.ink)

### 签名无效 <a href="#qian-ming-wu-xiao" id="qian-ming-wu-xiao"></a>

注意查看字段名与文档所述是否一致，请检查不需要参与签名的字段是否被加签了，请注意参数描述中的 “是否必填” 与 “是否签名” 这两列。

### 商户收到回调后的响应 <a href="#shang-hu-shou-dao-hui-tiao-hou-de-xiang-ying" id="shang-hu-shou-dao-hui-tiao-hou-de-xiang-ying"></a>

商户在收到通知信息后，在响应体的 body 中输出 OK 或者 ok（php例子：echo "OK";) ，否则会重复 5 次发送点对点通知。

### 测试环境 <a href="#ce-shi-huan-jing" id="ce-shi-huan-jing"></a>

商户可以在 Upay 的测试环境注册测试商户，并使用该商户的 appId 和 appSecret 请求网关：[https://api-test.upay.ink](https://api-test.upay.ink/?utm_medium=chat\&utm_campaign=link-shared-in-chat\&utm_source=livechat.com\&utm_content=upay.ink) ‎

测试环境注册教程：[https://docs.upay.ink/help/cn/howtouse/login-register](https://docs.upay.ink/help/cn/howtouse/login-register?utm_medium=chat\&utm_campaign=link-shared-in-chat\&utm_source=livechat.com\&utm_content=upay.ink)
