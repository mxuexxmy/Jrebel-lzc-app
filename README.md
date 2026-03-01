# Jrebel-lzc-app

JRebel 离线激活服务的懒猫微服应用，包含一个可直接访问的前端说明页和激活步骤引导。

## 项目内容

- `ui/index.html`：前端说明页面（包含激活步骤与动态域名提示）
- `ui/使用说明.md`：完整使用文档（安装、激活、热部署、常见问题）
- `lzc-manifest.yml`：懒猫应用清单，暴露 `12345` 端口到激活服务
- `lzc-build.yml`：打包配置，`contentdir` 指向 `ui`
- `docker-compse.yml`：本地 Docker 启动示例

## 快速开始

### 1) 本地启动激活服务（Docker）

```bash
docker compose -f docker-compse.yml up -d
```

启动后默认监听 `12345` 端口。

### 2) 打开说明页面

直接访问部署后的页面入口，或在本地打开 `ui/index.html` 查看操作指引。

### 3) IDEA 中激活 JRebel

- 生成 GUID
- 在 JRebel 的 `License Server URL` 填写：

```text
http://127.0.0.1:12345/{GUID}
```

- 选择在线激活（Activate online）
- 激活成功后切到离线模式（Work Offline）
- 邮箱可填写任意合法格式地址

## 详细文档

- 使用说明：`ui/使用说明.md`
- 参考仓库：[yu-xiaoyao/jrebel-license-active-server](https://github.com/yu-xiaoyao/jrebel-license-active-server)

## 打包产物

项目根目录包含已构建的 `.lpk` 包，可直接用于懒猫微服部署。
