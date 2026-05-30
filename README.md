# Nginx Gateway Local

通过子路径代理多个服务，含 frp 内网穿透支持

## 快速开始

```bash
npm run start       # 启动
npm run stop        # 停止
npm run logs        # 查看日志
```

## 前置条件

主项目已通过 `npm run start` 启动，并加入 `shared_gateway_net`。

## FRP 穿透配置

编辑 `frpc.toml`，填入 FRP 服务器信息：

```toml
serverAddr = "your-frp-server.com"
serverPort = 7000
auth.token = "your-token-here"
customDomains = ["your-domain.com"]
```

不需要穿透时直接删除或注释掉 docker-compose.yml 中的 `frpc` 服务。
