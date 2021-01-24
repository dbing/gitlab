# Gitlab 部署说明

## 配置 Gitlab 的存储目录

```shell
cp .env.example .env
```

按照实际环境设置相关环境变量。

## HTTPS 证书配置

将证书文件放置于 `$GITLAB_HOME/config/ssl` 目录下，并配置 `.env` 中的如下两项：

```shell
SSL_CERTIFICATE=
SSL_CERTIFICATE_KEY=
```

> 这里的路径是 Gitlab 容器里的绝对路径，也就是 /etc/gitlab/ssl/{你证书的文件名}

## 启动服务

```shell
docker-compose up -d
```
