---
icon: globe-pointer
---

# 签名算法

### 签名生成的通用步骤如下 <a href="#qian-ming-sheng-cheng-de-tong-yong-bu-zhou-ru-xia" id="qian-ming-sheng-cheng-de-tong-yong-bu-zhou-ru-xia"></a>

1. 设所有发送或者接收到的数据为集合 M，将集合 M 内 **需要加签** 的参数按照参数名 ASCII 码从小到大排序（字典序），使用 URL 键值对的格式（即 key1=value1\&key2=value2…）拼接成字符串 stringA。
2. 在 stringA 最后拼接上 `&appSecret=密钥` 得到 stringSignTemp 字符串，并对 stringSignTemp 进行 MD5 运算，再将得到的字符串所有字符转换为大写，得到 signature 值。

### 特别注意以下重要规则 <a href="#te-bie-zhu-yi-yi-xia-zhong-yao-gui-ze" id="te-bie-zhu-yi-yi-xia-zhong-yao-gui-ze"></a>

* 参数名 ASCII 码从小到大排序（字典序）。
* 参数名区分大小写。
* 传送的 signature 参数不参与签名，将生成的签名与该 signature 值作校验。
* 接口可能增加字段，验证签名时必须支持增加的扩展字段。

### 举例 (PHP) <a href="#ju-li-php" id="ju-li-php"></a>

例如传递的参数如下：

Copy

```
appId: 12345
chainType: 1
merchantOrderNo: 123123123123
productName：Goods
```

第一步：去掉 **不需要加签** 的参数，对 **需要加签** 的参数按照 key=value 的格式，并按照参数名 ASCII 字典序排序如下

Copy

```
$stringA = 'appId=12345&chainType=1&merchantOrderNo=123123123123';
```

第二步：对上一步中的字符串拼接 `&appSecret=密钥`

Copy

```
$stringSignTemp = $stringA.'&appSecret=密钥';
```

第三步：对上一步中字符串取 md5 值

Copy

```
$signature = md5($stringSignTemp);
```

第四步：对上面 md5 值转化为大写

Copy

```
$signature = strtoupper($signature);
```
