# RVC Dynamic F0 | RTX 40-series downloads

中文版在前，English instructions below. 这是可直接解压运行的 Windows CUDA 11.8 完整包，不是安装依赖的精简启动器。无需手动执行 PowerShell、安装 Python/pip 或训练模型；你只需要已有的 `.pth` 和对应 `.index`。

## 下载与运行

只需要下载以下三个文件，并放到同一个文件夹。这个下载仓库是公开的，不需要登录 GitHub，也不需要提供 token。

| 文件 | GitHub 直链 | GH-Proxy 加速 | ghfast 备用 |
|---|---|---|---|
| `RVC-Dynamic-F0-Open.exe`，约 2.5 MB | [下载 EXE](https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Open.exe) | [加速下载 EXE](https://gh-proxy.org/https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Open.exe) | [备用下载 EXE](https://ghfast.top/https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Open.exe) |
| `RVC-Dynamic-F0-Windows-cu118.zip.001`，约 1.89 GB | [下载第一部分](https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Windows-cu118.zip.001) | [加速下载第一部分](https://gh-proxy.org/https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Windows-cu118.zip.001) | [备用下载第一部分](https://ghfast.top/https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Windows-cu118.zip.001) |
| `RVC-Dynamic-F0-Windows-cu118.zip.002`，约 1.57 GB | [下载第二部分](https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Windows-cu118.zip.002) | [加速下载第二部分](https://gh-proxy.org/https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Windows-cu118.zip.002) | [备用下载第二部分](https://ghfast.top/https://github.com/whyhea1/rvc-dynamic-f0-downloads/releases/download/dynamic-f0-v0.1.1/RVC-Dynamic-F0-Windows-cu118.zip.002) |

双击 `RVC-Dynamic-F0-Open.exe`，选择解压位置，点击 “Extract and open RVC”。程序会检查两个分卷的 SHA-256、拼接、解压并打开变声器；以后直接打开 `RVC-Dynamic-F0-Ready/RVC-Dynamic-F0/RVC-Dynamic-F0.exe`。

三个文件必须来自同一次公开 Release，不要混用之前私有版下载的 EXE 或分卷。公开版本经过重新构建，校验值可能不同；`.build` 文件夹只是发布流程的重建输入，不是正常使用的下载入口。

三个文件总共约 3.46 GB，解压后约 6.52 GB，解压过程中还需要临时拼接空间。若下载文件和解压位置在同一个盘，建议开始下载前预留至少 15 GB 空间，并保留原版安装用于对照。

打开后选择已有的 `.pth`、对应 `.index`、麦克风和输出设备。启用 “Dynamic F0”，打开 “Edit curve” 自定义曲线；动态曲线中的数值是最终变调半音数，不会再叠加固定的 +12。

首次打开可能需要等待初始化。EXE 未进行代码签名，Windows 可能显示 SmartScreen 提示；本程序不会关闭安全功能，下载自第三方加速服务的文件也应与这里发布的校验值一致。

## 加速服务与隐私

上面的加速链接仅指向这里公开的安装包，不携带登录凭据。GH-Proxy 的前缀用法来自其[使用说明](https://gh-proxy.com/docs/quick-start)，ghfast 的使用方式见 [GPUHome 指引](https://docs.gpuhome.cc/docs/best-practices/github.html)；这些是第三方服务，不保证每个网络都能访问或更快。

加速服务不可用时，换另一列或使用 GitHub 直链。不要向加速网站提供 GitHub token、cookie 或私有仓库的临时下载地址；此公开仓库不包含购买的声音模型、个人设备配置、私有仓库的 Git 历史或访问凭据。

## English: download and open

Download the EXE and both archive parts from the table above, then place them together in one folder. This is a fully bundled CUDA 11.8 Windows app for RTX 40-series users, not a dependency installer; Python, Torch, HuBERT and RMVPE are included.

Double-click `RVC-Dynamic-F0-Open.exe`, choose an extraction location, and click “Extract and open RVC”. It verifies both parts, joins and extracts the app, and launches it; afterwards use `RVC-Dynamic-F0.exe` inside the extracted app folder.

Use all three files from this same public release, without mixing in the earlier private-release EXE or archive parts. The public package is rebuilt and has its own checksums; repository files under `.build` are build inputs, not the recommended app download.

Select your own voice `.pth` and matching `.index`, microphone, and output device. Enable “Dynamic F0” and open “Edit curve” to tune the pitch-dependent semitone shift, presets, smoothing and optional pitch ceiling; disable it to compare with the original fixed shift.

The downloads total about 3.46 GB and the extracted app is about 6.52 GB. Allow at least 15 GB free before downloading if downloads, temporary extraction data and the app will share one drive; no training or manual PowerShell/Python/pip setup is required.

The public downloads require no GitHub login. The third-party accelerator links above are convenience alternatives, not official GitHub mirrors or a guarantee of speed; never give them your GitHub token or cookies.

## Scope, checksums and redistribution

This is a prerelease for the desktop realtime GUI. Dynamic F0 does not repair microphone clipping, driver dropouts, octave-detection errors, or every model artifact, and it does not modify training, offline WebUI, or VST behavior.

The source build passed its Windows archive, runtime-import, GUI smoke and 39 unit tests. Those checks do not establish naturalness, actual microphone latency or GPU stability on your own PC; keep the original installation for comparison.

See [SHA256SUMS.txt](SHA256SUMS.txt), [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md), and the optional `RVC-Dynamic-F0-Licenses-and-Sources.zip` release asset. The source/notices archive is provided for redistribution transparency, not as another installation step; the application source is also present in the GPU payload, without Git history.

This repository contains download documentation, redistribution notices and self-contained release-build inputs, not development history. It is derived from [upstream RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI); the separate development repository remains private, and no purchased voice models are included.
