# IINA Desktop Music

[中文](#chinese) · [English](#english)

<a name="chinese"></a>
## 中文

面向桌面曲库的 IINA 1.5.1 定制补丁。在启动页和迷你音乐窗口加入 **搜索歌曲、顺序播放、随机播放**。

- 搜索匹配文件名和本机 FLAC 的标题、歌手标签。回车保留结果，双击或点「播放所选」才播放。
- 从启动页选歌会载入完整曲库，从所选曲目开始。在已有歌单中搜歌会保留列表顺序。
- 顺序和随机按钮每次都重新读取桌面 `歌` 文件夹。可创建这个目录并放入自己的音频文件。

## 从源码构建

先按 [IINA v1.5.1 的构建说明](https://github.com/iina/iina/tree/v1.5.1#building) 准备完整 Xcode 和依赖。将本仓库的补丁复制或放在上游源码旁，执行：

```sh
git clone --depth 1 --branch v1.5.1 https://github.com/iina/iina.git upstream-iina
git -C upstream-iina apply --check ../desktop-music.patch
git -C upstream-iina apply ../desktop-music.patch
open upstream-iina/iina.xcodeproj
```

在 Xcode 构建 `iina` scheme。补丁使用独立的应用标识和设置目录，采用本地构建的签名配置。仓库提供源码补丁和许可证。

上游项目为 [IINA](https://github.com/iina/iina)，补丁沿用 GPL-3.0。IINA 和其图标属于上游项目。

---

<a name="english"></a>
## English

A patch for IINA 1.5.1 that adds **song search, sequential playback, and shuffle** to the welcome screen and mini music player for a desktop music library.

- Search matches filenames and local FLAC title and artist tags. Return keeps the results on screen; double-click a result or choose **Play Selected** to play it.
- Choosing a song from the welcome screen loads the whole library starting at that track. Searching an existing playlist preserves its order.
- Sequential and shuffle actions rescan the desktop folder named `歌` each time. Create it and add your own audio files.

### Build from source

Install the full Xcode distribution and dependencies following the [IINA 1.5.1 build guide](https://github.com/iina/iina/tree/v1.5.1#building). From a directory containing `desktop-music.patch`, run:

```sh
git clone --depth 1 --branch v1.5.1 https://github.com/iina/iina.git upstream-iina
git -C upstream-iina apply --check ../desktop-music.patch
git -C upstream-iina apply ../desktop-music.patch
open upstream-iina/iina.xcodeproj
```

Build the `iina` scheme in Xcode. The patch uses a separate app identifier and settings directory, with signing configured for local builds. This repository contains the patch and license. The patch follows GPL-3.0; [IINA](https://github.com/iina/iina) and its icons belong to the upstream project.
