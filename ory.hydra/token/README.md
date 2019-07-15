# Token

Token 命令

语法：

```text
$  hydra token [command]
```

支持可用的命令如下：

| 命令 | 说明 |
| :--- | :--- |
| client | An exemplary OAuth 2.0 Client performing the OAuth 2.0 Client Credentials Flow |
| flush | Removes inactive access tokens from the database |
| introspect | Introspect an access or refresh token |
| revoke | Revoke an access or refresh token |
| user | An exemplary OAuth 2.0 Client performing the OAuth 2.0 Authorize Code Flow |

本命令可以支持的参数

| 参数标记 | 类型 | 说明 |
| :--- | :--- | :--- |
| --fail-after | duration | Stop retrying after the specified duration \(default 1m0s\) |
| --fake-tls-termination |  | fake tls termination by adding "X-Forwarded-Proto: https" to http headers |
| -h, --help |  | help for token |

支持的全局参数

| 参数标记 | 类型 | 说明 |
| :--- | :--- | :--- |
| --config | string | Config file \(default is $HOME/.hydra.yaml\) |
| --skip-tls-verify |  | Foolishly accept TLS certificates signed by unkown certificate authorities |

