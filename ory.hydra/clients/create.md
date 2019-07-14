---
description: 创建客户端
---

# Create

## 1. Client Create 命令

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
| --pgp-key | string | Base64 encoded PGP encryption key for encrypting client secret |
| --pgp-key-url | string | PGP encryption key URL for encrypting client secret |
| --policy-uri | string | A URL string that points to a human-readable privacy policy document that describes how the deployment organization collects, uses, retains, and discloses personal data |
| --post-logout-callbacks | strings | List of allowed URLs to be redirected to after a logout |
| -r, --response-types | strings | A list of allowed response types \(default \[code\]\) |
| -a, --scope | strings | The scope the client is allowed to request |
| --secret | string | Provide the client's secret |
| --subject-type | string | Provide the client's secret |
| --token-endpoint-auth-method | string | Define which authentication method the client may use at the Token Endpoint. Valid values are "client\_secret\_post", "client\_secret\_basic", "private\_key\_jwt", and "none" \(default "client\_secret\_basic"\) |
| --tos-uri | string | A URL string that points to a human-readable terms of service document for the client that describes a contractual relationship between the end-user and the client that the end-user accepts when authorizing the client |



支持的全局参数包括

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| --access-token | string | Set an access token to be used in the Authorization header, defaults to environment variable OAUTH2\_ACCESS\_TOKEN |
| --config | string | Config file \(default is $HOME/.hydra.yaml\) |
| --endpoint | string | Set the URL where ORY Hydra is hosted, defaults to environment variable HYDRA\_ADMIN\_URL |
| --fail-after | duration | Stop retrying after the specified duration \(default 1m0s\) |
| --fake-tls-termination |  | Fake tls termination by adding "X-Forwarded-Proto: https" to http headers |
| --skip-tls-verify |  | Foolishly accept TLS certificates signed by unkown certificate authorities |

## 2.  示例

创建一个简单的Client

```bash
$ hydra clients create -n "first app" -c http://localhost:3000/cb -g authorization_code -r code -a core,foobar --endpoint http://localhost:4445
```

显示结果

```bash
OAuth 2.0 Client ID: 4a77fe34-7a6b-4a9b-befd-c7d9941a5d8d 
OAuth 2.0 Client Secret: q1u3b6V_2PJkLo~oS_h9NkjUiX
```

| 参数 = 值  | 值 | 说明 |
| :--- | :--- | :--- |
| --name  | first app | 该客户端指定名称为"first app" |
|  --callbacks | [http://localhost:3000/cb](http://localhost:3000/cb) | 需要回调的应用服务URL |
| --grant-types | authorization\_code | 授权类型为"authorization\_code" |
| --response-types | code | 响应返回类型 |
| --scope | core,foobar | 允许的客户端请示范围 |

