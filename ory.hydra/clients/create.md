---
description: 创建客户端
---

# Create

## Client Create 命令

本命令创建支持OAuth2.0 流程 授权码，固定值和流程。

语法：

```text
$ hydra clients create [flags]
```

ORY Hydra 实现 OPENID 动态连接客户端标准，可以更多参数支持。

Example:

```
$ hydra clients create -n "my app" -c http://localhost/cb -g authorization_code -r code -a core,foobar
```

{% hint style="success" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

支持的参数包括

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| --allowed-cors-origins | strings | 支持可以跨域的请求URLS列表. Requires CORS\_ENABLED. |
| --audience | strings | The audience this client is allowed to request |
| -c, --callbacks | strings | REQUIRED list of allowed callback URLs |
| --client-uri | string | 提供关于客户端信息的页面URL。 |
| -g, --grant-types | string | A list of allowed grant types \(default \[authorization\_code\]\) |
| -h, --help | string | help for create |
| --id | string | 对本CLIENT 指定ID |
| --jwks-uri | string | Define the URL where the JSON Web Key Set should be fetched from when performing the "private\_key\_jwt" client authentication method |
| --keybase | string | Keybase username for encrypting client secret |
| --logo-uri | string | A URL string that references a logo for the client |
| -n, --name | string | The client's name |

```
// Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```



