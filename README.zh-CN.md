<h1 align="center">abyss</h1>

<p align="center">
    <a href="README.md">English</a> |
    <span>简体中文</span>
</p>

> [!IMPORTANT]
>
> 这是 [abyss](https://abyss.abgox.com) Scoop bucket 的**个人维护镜像**。原仓库（`abgox/abyss`）及原作者的其他仓库已被删除，因此使用此 fork 继续维持 bucket 可用。
>
> 原文档站（[abyss.abgox.com](https://abyss.abgox.com)）仍然在线，其中记录了本 bucket 的大部分特性与约定。

## 添加 bucket

> [!WARNING]
>
> bucket 名称**必须**为 `abyss`，内置 util 脚本与清单校验依赖该名称。

```shell
scoop bucket add abyss https://github.com/Rockflow/abyss_new
```

```shell
scoop search <应用名>
scoop install abyss/<应用名>
```

## 与原 bucket 的差异

- 删除了 **85** 个依赖原作者已删除仓库的清单：
  - `abgox.*` 应用（`abgox.InputTip`、`abgox.PSCompletions`、`abgox.scoop-i18n`、`abgox.SpaceKey`、`abgox.scoop-install`、`abgox.scoop-update`、`abgox.ConvertFrom-JsonAsHashtable`、`abgox.InputTip-zip`）
  - 托管在已删除的 `abgox/maple-font` fork 上的 `subframe7536.Maple-Mono.*` 构建版本（48 个；指向上游 `subframe7536/maple-font` 的已保留）
  - 下载 URL 指向原 bucket Releases 的占位清单（`pending` / `renamed` / `deprecated` / `virtual` 状态）
- 共享持久化目录 `@abgox.abyss` 已更名为 `@abyss`。
- 自动更新（Excavator）改用官方 [ScoopInstaller/GitHubActions](https://github.com/ScoopInstaller/GitHubActions)，**每天**运行一次。

## 已知限制

> [!NOTE]
>
> 原作者维护了一个 Scoop 的个人 fork，为 `checkver` 扩展了额外来源（`winget`、`psgallery`、`from_installer`）。该 fork 已删除，官方 Scoop 不支持这些来源。

- 使用这些 `checkver` 来源的约 **200** 个清单仍可**正常安装**（锁定在当前版本），但无法被本 bucket 的 CI 自动更新。
- 其余清单（约 **900** 个，基于 `github` / `url` / `commit` / `sourceforge` checkver）每天自动更新。

## 许可证

[MIT](./LICENSE) © [abgox](https://me.abgox.com)
