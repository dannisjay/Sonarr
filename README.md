# Sonarr

磁力聚合搜索 + 115 离线下载 + Telegram 机器人，闭源发布。

## 镜像

- Docker Hub：`dannis1514/sonarr`
- 标签：`1.7.1`、`latest`
- 支持架构：`linux/amd64`、`linux/arm64`

## 快速部署

```yaml
services:
  sonarr:
    image: dannis1514/sonarr:latest
    container_name: sonarr
    restart: unless-stopped
    ports:
      - "8080:8080"
    volumes:
      - ./data:/app/data
```

将上面的内容保存为 `docker-compose.yml`，然后在同目录执行：

```bash
docker compose up -d
```

`data` 目录留空即可，首次启动会自动生成 `config.json`。

## 访问

浏览器打开 `http://<服务器IP>:8080`。

- 首次打开会进入初始化页面，设置管理员用户名和密码。
- 密码至少 6 位，初始化完成后使用该账号登录。

## 手动拉取镜像

```bash
docker pull dannis1514/sonarr:latest
```

## 说明

此仓库仅提供部署文档，不包含其它信息。
