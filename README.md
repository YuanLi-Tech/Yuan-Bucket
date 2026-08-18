# Yuan-Bucket

YuanLi-Tech 的 [Scoop](https://scoop.sh) 软件桶。

## 用法

```powershell
scoop bucket add Yuan-Bucket https://github.com/YuanLi-Tech/Yuan-Bucket
scoop install android-dex
```

## 收录软件

| 应用 | 版本 | 说明 |
| --- | --- | --- |
| [Android-Dex](https://github.com/Shrey113/Android-Dex) | 1.0.1 | scrcpy 驱动的 Android 无线投屏桌面应用（免 root，Flutter，无线 ADB） |

## 自动更新

[Excavator](.github/workflows/excavator.yml) 每 4 小时运行一次 checkver，发现新版本自动提交 PR。

## 开发

- 新增 manifest：放入 `bucket/` 目录
- 本地验证：`$env:SCOOP_HOME=<Scoop 克隆路径>; pwsh bin\test.ps1`（需 BuildHelpers 2.0.1 + Pester 5.2.0）
- CI：push / PR 时运行 [ci.yml](.github/workflows/ci.yml) 全量校验（语法、样式、schema）
