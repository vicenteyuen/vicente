---
description: 列表所有已经注册的客户端信息
---

# List

## 1. Client List 命令

本命令列出所有已经登记注册的客户端服务。

语法：

```bash
$ hydra clients list [flags]
```

Example:

```
$ hydra clients list
```

支持的参数包括

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| -h, --help |  | help for list |
| --limit | int | 每页显示返回的最大条目数量。（默认值为：20） |
| --page | int | 显示的当前页码。 \(默认值：当前页为第1页\) |

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

列出已经注册的客户端信息

```bash
$ hydra clients list --endpoint http://localhost:4445
```

