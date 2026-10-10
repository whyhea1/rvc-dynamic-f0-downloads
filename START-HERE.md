# RVC Dynamic F0: ready-to-run RTX 40-series app

This is the complete CUDA 11.8 Windows GPU app, not a minimal installer. Python, Torch, HuBERT and RMVPE are bundled; you do not need PowerShell commands, pip installation, model training or a separate CUDA toolkit.

## Download and open

Open the [public download repository](https://github.com/whyhea1/rvc-dynamic-f0-downloads#readme) for direct and China-friendly accelerator links. Download just these three files and put them in the same folder:

- **RVC-Dynamic-F0-Open.exe**: native click-to-extract opener.
- **RVC-Dynamic-F0-Windows-cu118.zip.001**: first part of the complete app.
- **RVC-Dynamic-F0-Windows-cu118.zip.002**: second part of the complete app.

Double-click the EXE, choose the extraction folder, and click “Extract and open RVC”. It verifies, joins and extracts the payload, then opens the app; next time use `RVC-Dynamic-F0.exe` inside `RVC-Dynamic-F0-Ready/RVC-Dynamic-F0`.

Allow at least 15 GB free before downloading if the downloads and extracted app will share one drive. The EXE is unsigned, so Windows may show a SmartScreen warning; nothing in this package disables Windows security.

## Select your model and tune the curve

Select your existing `.pth` and matching `.index`, microphone, and output device. Your purchased models are not bundled, uploaded, modified or retrained.

Enable “Dynamic F0” and open “Edit curve” to adjust control points, presets, attack/release smoothing, and the optional pitch ceiling. The curve replaces the fixed pitch shift rather than stacking on top of it; disable Dynamic F0 for comparison.

Numerical, archive and interface checks are not a guarantee of naturalness or microphone/GPU latency on your own PC. Input clipping, pitch-detector errors and driver dropouts may still require separate troubleshooting.

## 中文说明

这是可以直接解压运行的完整 RTX 40 系列 GPU 版，不是需要安装依赖的精简启动器。无需手动执行 PowerShell、安装 Python/pip、另装 CUDA Toolkit 或训练声音模型。

打开[公开下载页](https://github.com/whyhea1/rvc-dynamic-f0-downloads#readme)，选择 GitHub 直链或表格中的加速链接。下载 EXE 和 `.zip.001`、`.zip.002`，放到同一个文件夹；双击 EXE，选择解压位置，点击 “Extract and open RVC”。

选择已有的 `.pth`、对应 `.index`、麦克风和输出设备即可，购买的模型不会被上传或改动。启用 “Dynamic F0” 后打开 “Edit curve” 调整曲线；动态曲线直接决定最终增加的半音数，不会再叠加固定变调。

此公开下载页不需要登录或 token，开发仓库依然保持私有。两个分卷会在解压时进行 SHA-256 检查；若显示校验失败，请重新下载对应分卷，不要关闭校验。
