---
description: 业务服务启动命令
---

# Serve

Clients 命令

语法：

```text
$  hydra serve [command]
```

支持可用的命令如下：

| 命令 | 说明 |
| :--- | :--- |
| admin | Serves Administrative HTTP/2 APIs |
| public | Serves Public HTTP/2 APIs |
| all | Serves both public and administrative HTTP/2 APIs |

本命令可以支持的参数

| 参数标记 | 类型 | 说明 |
| :--- | :--- | :--- |
| --dangerous-allow-insecure-redirect-urls | strings | DO NOT USE THIS IN PRODUCTION - Disable HTTPS enforcement for the provided redirect URLs |
| --dangerous-force-http |  | DO NOT USE THIS IN PRODUCTION - Disables HTTP/2 over TLS \(HTTPS\) and serves HTTP instead |
| --disable-telemetry |  | Disable anonymized telemetry reports - for more information please visit [https://www.ory.sh/docs/ecosystem/sqa](https://www.ory.sh/docs/ecosystem/sqa) |
| -h, --help |  | help for serve |
| --sqa-opt-out |  | Disable anonymized telemetry reports - for more information please visit [https://www.ory.sh/docs/ecosystem/sqa](https://www.ory.sh/docs/ecosystem/sqa) |

支持的全局参数

| 参数标记 | 类型 | 说明 |
| :--- | :--- | :--- |
| --config | string | Config file \(default is $HOME/.hydra.yaml\) |
| --skip-tls-verify |  | Foolishly accept TLS certificates signed by unkown certificate authorities |

