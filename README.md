<h1 align="center">abyss</h1>

<p align="center">
    <span>English</span> |
    <a href="README.zh-CN.md">简体中文</a>
</p>

> [!IMPORTANT]
>
> This is a **personally maintained mirror** of the [abyss](https://abyss.abgox.com) Scoop bucket. The original repository (`abgox/abyss`) and other repositories of the original author have been deleted, so this fork is used to keep the bucket usable.
>
> The original documentation site ([abyss.abgox.com](https://abyss.abgox.com)) is still online and describes most of the bucket features and conventions.

## Add the bucket

> [!WARNING]
>
> The bucket name **must** be `abyss`. The built-in util scripts and manifest validation require it.

```shell
scoop bucket add abyss https://github.com/Rockflow/abyss_new
```

```shell
scoop search <app>
scoop install abyss/<app>
```

## Changes compared to the original bucket

- Removed **85** manifests that depended on the original author's now-deleted repositories:
  - `abgox.*` apps (`abgox.InputTip`, `abgox.PSCompletions`, `abgox.scoop-i18n`, `abgox.SpaceKey`, `abgox.scoop-install`, `abgox.scoop-update`, `abgox.ConvertFrom-JsonAsHashtable`, `abgox.InputTip-zip`)
  - `subframe7536.Maple-Mono.*` builds hosted on the deleted `abgox/maple-font` fork (48 manifests; the ones pointing to the upstream `subframe7536/maple-font` are kept)
  - Placeholder manifests (`pending` / `renamed` / `deprecated` / `virtual`) whose download URL pointed to the deleted bucket's releases
- The shared persistence directory `@abgox.abyss` was renamed to `@abyss`.
- Auto-update (Excavator) now uses the official [ScoopInstaller/GitHubActions](https://github.com/ScoopInstaller/GitHubActions) and runs **daily**.

## Known limitations

> [!NOTE]
>
> The original author maintained a personal fork of Scoop that extended `checkver` with extra sources (`winget`, `psgallery`, `from_installer`). That fork is gone, and official Scoop does not support these sources.

- About **200** manifests using those `checkver` sources still **install fine** at their pinned versions, but they cannot be auto-updated by this bucket's CI.
- All other manifests (roughly **900**, based on `github` / `url` / `commit` / `sourceforge` checkver) auto-update daily.

## License

[MIT](./LICENSE) © [abgox](https://me.abgox.com)
