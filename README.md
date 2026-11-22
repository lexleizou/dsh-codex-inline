# DSH Inline References · 行内引用

A community plugin that adds Skill names and website icons to the DeepSeek Harness message composer. You can set a display name and icon for each Skill. Supported URLs show their site icon as you draft a message.

![A typed URL with its site icon in the DSH composer](docs/taobao.png)

## Install

Compatible with DSH `0.2.2-rc.5` (macOS Desktop verified). For DSH Desktop:

```sh
dsh plugin --profile desktop add github:lexleizou/dsh-inline-references#v1.0.0
```

For a self-hosted DSH Web profile:

```sh
dsh plugin --profile web add github:lexleizou/dsh-inline-references#v1.0.0
```

Use the profile that runs your DSH instance. Reload the desktop window or web page after installation. If you have a local build of the same plugin, disable that build before using the public package.

## 使用

- **技能**。输入 `/` 并选择 Skill。在 **插件 → 行内引用** 中可以为每项 Skill 设置显示名称和图标，支持文字图标或不超过 64 KB 的 PNG、JPEG、WebP。复制和发送仍用原始 Skill 标识。
- **网址**。手动输入受支持的网址，按空格生成行内链接，也可以单独粘贴。例如 `www.taobao.com`。点击无协议链接时使用 HTTPS，发送时保留输入的写法。
- **站点**。内置 46 个站点品牌图标，覆盖 157 个公开主机名，包括 GitHub、ChatGPT、Claude、DeepSeek、Gmail、Outlook、淘宝、小红书、钉钉、飞书、哔哩哔哩等。完整匹配清单见 [源码](client.js)。

## 数据和权限

自定义名称和图标保存在当前客户端的本地存储里。图标随包提供，识别站点时无需联网。点击链接会打开对应网站。停用插件前，可先发送或移除草稿中的行内网页引用。

## License

Plugin code is available under the [MIT License](LICENSE). Site marks are covered by the [third-party notices](THIRD-PARTY-NOTICES.md).
