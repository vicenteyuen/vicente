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

## 2.  示例

同时启动admin和public服务应用

```bash
$ hydra.exe serve all --config=./hydra-test.yml --dangerous-force-http
```

显示结果

```bash
{"level":"info","msg":"No tracer configured - skipping tracing setup","time":"2019-07-15T14:45:12+08:00"}
{"level":"warning","msg":"JSON Web Key Set \"hydra.openid.id-token\" does not exist yet, generating new key pair...","time":"2019-07-15T14:45:12+08:00"}
{"level":"warning","msg":"Configuration secrets.system is not set, generating a temporary, random secret...","time":"2019-07-15T14:45:13+08:00"}
{"level":"warning","msg":"Generated secret: fQF1QxkXQykGDV7aahSIDwb0~RfB0JdM","time":"2019-07-15T14:45:13+08:00"}
{"level":"warning","msg":"Do not use generate secrets in production. The secret will be leaked to the logs.","time":"2019-07-15T14:45:13+08:00"}
{"level":"warning","msg":"JSON Web Key Set \"hydra.jwt.access-token\" does not exist yet, generating new key pair...","time":"2019-07-15T14:45:13+08:00"}
Thank you for using ORY Hydra v1.0.0+oryOS.12!

Take security seriously and subscribe to the ORY Security Newsletter. Stay on top of new patches and security insights.

>> Subscribe now: http://eepurl.com/di390P <<
{"level":"info","msg":"Software quality assurance features are enabled. Learn more at: https://www.ory.sh/docs/ecosystem/sqa","time":"2019-07-15T14:45:15+08:00"}
{"level":"warning","msg":"JSON Web Key Set \"hydra.https-tls\" does not exist yet, generating new key pair...","time":"2019-07-15T14:45:15+08:00"}
{"level":"info","msg":"Setting up http server on localhost:4444","time":"2019-07-15T14:45:19+08:00"}
{"level":"warning","msg":"HTTPS disabled. Never do this in production.","time":"2019-07-15T14:45:19+08:00"}
{"level":"info","msg":"Setting up http server on :4445","time":"2019-07-15T14:45:19+08:00"}
{"level":"warning","msg":"HTTPS disabled. Never do this in production.","time":"2019-07-15T14:45:19+08:00"}
```

