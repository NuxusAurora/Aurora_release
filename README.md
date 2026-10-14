# Aurora 更新发布仓库

本仓库用于发布验证通过的 Aurora 客户端更新。源码仓库为 [NuxusAurora/Aurora_agent](https://github.com/NuxusAurora/Aurora_agent)。

| 发布分支 | 平台 | 版本标签 | 更新产物 |
| --- | --- | --- | --- |
| `main` | Windows | `v<主版本>.<次版本>.<修订>` | `Aurora-win-x64.exe` |
| `mac` | Mac | `mac-v<主版本>.<次版本>.<修订>` | `Aurora-mac-arm64.zip` / `Aurora-mac-x64.zip` |

更新完成并通过对应平台验收后，在本仓库创建 GitHub Release，标签指向该平台发布分支，并上传匹配的版本产物、更新说明与 SHA-256 校验信息。Windows 和 Mac 独立构建、独立发布。

Windows 正式 Release 可标记为 Latest；Mac Release 不标记为 Latest（`make_latest=false`），Mac 更新检查按 `mac-v` 标签与对应架构产物选择版本。GitHub Releases 属于整个仓库，客户端必须核对平台、版本与产物，不能仅凭分支名称判断更新包。

当前仅初始化发布说明及分支；尚未上传更新包或创建客户端 Release。
