# Swagger UI for TOS

Swagger UI presents interactive API documentation. Install the package for your NAS architecture on TOS 7 with Docker Engine.

1. Open Swagger UI from the desktop or visit `http://<NAS IP>:18883` from a trusted network. On first launch, it shows a small local example.
2. In Docker Manager, locate the host directory mounted at `/spec`. Put your OpenAPI document there as `openapi.yaml`, with read permissions for the container, and recreate the container. You can put YAML or JSON content in that file.
3. Expand an operation to read its parameters and responses. For **Try it out**, use a reachable server URL in your specification. If the API is on a different origin, its server must allow requests from the Swagger UI origin.

The specification is downloadable by anyone who can reach this service. Store only documents that the service's users may read. Back up the directory mounted at `/spec` before reinstalling.

In TOS package 5.35.1.2, the server runs as UID/GID `101:101`. When upgrading, check that this account can traverse the mounted directory and read `openapi.yaml`.

## TOS 使用说明

Swagger UI 用于展示可交互的 API 文档。请在安装了 Docker Engine 的 TOS 7 上选择适合 NAS 架构的安装包。

1. 从 TOS 桌面打开 Swagger UI，或在可信网络内访问 `http://<NAS IP>:18883`。首次打开时会显示一个本地示例。
2. 在 Docker 管理器中找到挂载到 `/spec` 的宿主目录，将自己的 OpenAPI 文档保存为 `openapi.yaml`，确保容器可读取后重建容器。文件内容可用 YAML 或 JSON。
3. 展开接口查看参数和响应。使用 **Try it out** 时，规范中要填写浏览器可访问的 API 地址；跨源请求还需要 API 服务端允许 Swagger UI 的来源。

能够访问此服务的人也可以下载接口文档，请只存放允许这些用户查看的文档。重新安装前请备份挂载到 `/spec` 的目录。

TOS 包 5.35.1.2 使用 UID/GID `101:101` 运行。升级时请确认该账号可进入挂载目录并读取 `openapi.yaml`。

[上游项目 / Upstream](https://github.com/swagger-api/swagger-ui) · [配置文档 / Configuration](https://swagger.io/docs/open-source-tools/swagger-ui/usage/configuration/)

[隐私政策 / Privacy policy](PRIVACY.md)
