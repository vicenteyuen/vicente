# Client

## 1. Token client 命令

本命令可支持同时启动public 和 admin  服务基础。

语法：

```bash
$  hydra token client [flags]
```



支持的参数包括

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| --audience | strings | Request a specific OAuth 2.0 Access Token Audience |
| --client-id | string | Use the provided OAuth 2.0 Client ID, defaults to environment variable OAUTH2\_CLIENT\_ID |
| --client-secret | string | Use the provided OAuth 2.0 Client Secret, defaults to environment variable OAUTH2\_CLIENT\_SECRET |
| --endpoint | string | Set the URL where ORY Hydra is hosted, defaults to environment variable HYDRA\_URL |
| -h, --help |  | help for client |
| --scope | srings | OAuth2 scope to request |
| -v, --verbose |  | Toggle verbose output mode |

