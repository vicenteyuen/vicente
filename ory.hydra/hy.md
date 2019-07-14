# Clients

Clients 命令

语法：

```text
hydra clients [command]
```

支持可用的命令如下：

| 命令 | 说明 |
| :--- | :--- |
| create |  |
| delete |  |
| get |  |
| import |  |
| list |  |

本命令可以支持的参数

| 参数标记 | 类型 | 说明 |
| :--- | :--- | :--- |
| ---access-token | string |  |
| --endpoint | string |  |
| --fail-after  | duration |  |
| --fake-tls-termination | string |  |

支持的全局参数

| 参数标记 | 类型 | 说明 |
| :--- | :--- | :--- |
| --config | string | 配置文件。默认为 \( $HOME/.hydra.yaml \) |
| --skip-tls-verify |  |  |

###  CREATE --- 创建客户端

```bash
hydra clients create
```

