---
description: 创建客户端
---

# Create

## Client Create 命令

本命令创建支持OAuth2.0 流程 授权码，固定值和流程。

ORY Hydra 实现 OPENID 动态连接客户端标准，可以更多参数支持。

Example:

```
$ hydra clients create -n "my app" -c http://localhost/cb -g authorization_code -r code -a core,foobar
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

```
// Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```



