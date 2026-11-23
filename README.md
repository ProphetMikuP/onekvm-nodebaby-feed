# OneKVM NodeBaby independent feed

独立签名的软件源，当前版本 **0.1.0-r1**。这是非官方实验扩展，尚未通过真实 NanoKVM Pro 设备验收。

## OneKVM 接入

软件源地址（GitHub Pages 发布成功后使用）：

```text
src/gz nodebaby-independent https://prophetmikup.github.io/onekvm-nodebaby-feed/aarch64_cortex-a53
```

在 OneKVM 软件源管理中添加此地址，并单独粘贴 [GPG 公钥](aarch64_cortex-a53/nodebaby-feed-public.asc)。核对完整指纹：

```text
7F3D21B869A478AFA7992C2B352A75F8531979C0
```

安装时取消“安装后启用”。进程运行、端口就绪不代表业务在线；此版本业务在线会显示未确认。
请保留本地管理通道，后续设备测试需单独确认。

## 下载与校验

- [IPK](aarch64_cortex-a53/onekvm-extension-nodebaby_0.1.0-r1_aarch64_cortex-a53.ipk)
- [IPK 签名](aarch64_cortex-a53/onekvm-extension-nodebaby_0.1.0-r1_aarch64_cortex-a53.ipk.asc)
- [索引](aarch64_cortex-a53/Packages)、[索引签名](aarch64_cortex-a53/Packages.asc)
- [完整扩展源码](source/onekvm-extension-nodebaby-0.1.0-r1-source.zip)
- [本地测试记录](validation/TEST-RESULTS.json)

IPK SHA256：`1f77cc6563c5f317ba8230ee11ccdf1bddf6526434df9a317d0ed28ad285484b`。
签名证明密钥及下载字节完整性，不代表 OneKVM 或节点小宝官方认证。
客户端二进制保留原厂权利；见 [第三方说明](THIRD_PARTY_NOTICES.txt)。

## GitHub Pages

本仓库使用 `main` 分支的根目录发布，保留 `.nojekyll`，使签名索引和二进制按原字节提供。
Pages 地址：https://prophetmikup.github.io/onekvm-nodebaby-feed/ 。
如果还未开启，进入 Settings → Pages → Deploy from a branch，选择 main 与 /(root)。

仓库只包含公开材料。签名私钥、口令和撤销证书保留在发布者本地，不应提交到 GitHub。
后续更新必须在本地重新生成并签署索引；不要手工修改已签署的 Packages 内容。
