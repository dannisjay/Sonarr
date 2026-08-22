# Sonarr

磁力聚合搜索 + 115 离线下载 + Telegram 机器人，闭源发布。

## 镜像

- Docker Hub：`dannis1514/Sonarr`
- 标签：`1.7.1`、`latest`
- 支持架构：`linux/amd64`、`linux/arm64`

## 快速部署

```yaml
services:
  sonarr:
    image: dannis1514/Sonarr:1.7.1
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

- 默认账号：`admin`
- 默认密码：`change-me`
- 首次登录后请尽快在设置中心修改密码。

## 手动拉取镜像

```bash
docker pull dannis1514/Sonarr:1.7.1
```

## 说明

本项目为闭源软件，此仓库仅提供部署文档，不包含任何源码。
