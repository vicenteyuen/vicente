# All

## 1. Serve all 命令

本命令可支持同时启动public 和 admin  服务基础。

语法：

```bash
$  hydra serve admin [flags]
```



支持的参数包括

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| -h, --help | string | help for create |

支持的全局参数包括

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| --config | string | Config file \(default is $HOME/.hydra.yaml\) |
| --dangerous-allow-insecure-redirect-urls | strings | DO NOT USE THIS IN PRODUCTION - Disable HTTPS enforcement for the provided redirect URLs |
| --dangerous-force-http |  | DO NOT USE THIS IN PRODUCTION - Disables HTTP/2 over TLS \(HTTPS\) and serves HTTP instead |
| --disable-telemetry |  | Disable anonymized telemetry reports - for more information please visit [https://www.ory.sh/docs/ecosystem/sqa](https://www.ory.sh/docs/ecosystem/sqa) |
| --skip-tls-verify |  | Foolishly accept TLS certificates signed by unkown certificate authorities |
| --sqa-opt-out |  | Disable anonymized telemetry reports - for more information please visit [https://www.ory.sh/docs/ecosystem/sqa](https://www.ory.sh/docs/ecosystem/sqa) |

