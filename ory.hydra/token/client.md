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



支持的全局参数

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| --config | string | Config file \(default is $HOME/.hydra.yaml\) |
| --fail-after | duration | Stop retrying after the specified duration \(default 1m0s\) |
| --fake-tls-termination |  | fake tls termination by adding "X-Forwarded-Proto: https" to http headers |
| --skip-tls-verify |  | Foolishly accept TLS certificates signed by unkown certificate authorities |

## 2.  示例

通过用户认证授权处理

```bash
$ hydra token client --endpoint http://localhost:4444/ --client-id 426d602a-9ee4-4765-93a9-46e4d0dafbe1 --client-secret fT3cZmqCW7XJT9paLDiT~UdciC
```

