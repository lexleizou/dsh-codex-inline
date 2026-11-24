# dsh-codex-inline · Codex 风格行内引用

A DeepSeek Harness community plugin inspired by the way Codex shows references in the composer. Set a display name and icon for each Skill, and see site icons alongside supported links as you draft a message.

参考 Codex 的输入框展示方式，在 DSH 草稿里显示 Skill 名称、Skill 图标和网址的站点图标。

![A typed URL with its site icon in the DSH composer](docs/taobao.png)

## Install

Compatible with DSH `0.2.2-rc.5+` (macOS Desktop verified). Install from npm (or directly via DSH Plugin Hub):

```sh
dsh plugin --profile desktop add dsh-codex-inline
```

For a self-hosted DSH Web profile:

```sh
dsh plugin --profile web add dsh-codex-inline
```

You can also install from GitHub: `dsh plugin --profile desktop add github:lexleizou/dsh-codex-inline#v1.0.2`.

Use the profile that runs your DSH instance. Reload the desktop window or web page after installation. If you have the earlier public package `dsh-inline-references`, disable or remove it before installing `dsh-codex-inline`. Saved Skill settings remain available in the same client. Disable any local build of this plugin before enabling the public package.

## 使用

- **技能**。输入 `/` 并选择 Skill。在 **插件 → Codex 风格行内引用** 中可以为每项 Skill 设置显示名称和图标，支持文字图标或不超过 64 KB 的 PNG、JPEG、WebP。复制和发送仍用原始 Skill 标识。
- **网址**。手动输入受支持的网址，按空格生成行内链接，也可以单独粘贴。例如 `www.taobao.com`。点击无协议链接时使用 HTTPS，发送时保留输入的写法。
- **站点**。内置 47 个站点品牌图标，覆盖 165 个公开主机名，包括 GitHub、Hugging Face、ChatGPT、Claude、DeepSeek、Gmail、Outlook、淘宝、小红书、钉钉、飞书、哔哩哔哩等。完整匹配清单见 [源码](client.js)。

## 数据和权限

自定义名称和图标保存在当前客户端的本地存储里。图标随包提供，识别站点时无需联网。点击链接会打开对应网站。停用插件前，可先发送或移除草稿中的行内网页引用。

## License

Plugin code is available under the [MIT License](LICENSE). Site marks are covered by the [third-party notices](THIRD-PARTY-NOTICES.md).
