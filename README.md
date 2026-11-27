# 本鲸的 DSH 插件合集

五个给 AI agent 用的小工具，都 MIT 开源，都是 DSH Host 插件。

## 1. FishClick

**窗口截图 = 点击坐标。**

只截窗口客户区，截图上的像素就是点击坐标；解决 DPI 缩放、窗口偏移导致的“点哪都偏”。

- 仓库：<https://github.com/holderlink/fishclick>
- 视频：<https://www.bilibili.com/video/BV1cz1xzrEHM>
- 工具：`fishclick_window` / `fishclick_click`
- 安装：

```powershell
dsh plugin --profile desktop add github:holderlink/fishclick
```

## 2. Video Preflight

**投稿前先体检，别等投出去才发现。**

本地用 ffprobe/ffmpeg/Pillow 检查时长、分辨率、帧率、音轨、响度、封面比例、标题/简介/标签和 AI 声明，输出 PASS / WARN / FAIL。

- 仓库：<https://github.com/holderlink/dsh-video-preflight>
- 视频：<https://www.bilibili.com/video/BV1yD1sz5EBr>
- 工具：`video_preflight`
- 安装：

```powershell
dsh plugin --profile desktop add github:holderlink/dsh-video-preflight
```

## 3. Bundle Doctor

**发布插件前先体检。**

检查 `dsh.bundle.patch`、`cordis.patch.yml`、exports/files、图标格式、locale、detail、README，以及 GitHub 仓库的 topic/年龄/可见性，最后生成 awesome-dsh-plugin 的 YAML。

- 仓库：<https://github.com/holderlink/dsh-plugin-release>
- 视频：<https://www.bilibili.com/video/BV15G1xzFE1P>
- 工具：`bundle_doctor`
- 安装：

```powershell
dsh plugin --profile desktop add github:holderlink/dsh-plugin-release
```

## 4. Cover Lint

**封面在手机上还看不看得清。**

检查尺寸、16:9/4:3、亮度、整体对比度、上下文字区域，以及缩到 320px 后的对比度。

- 仓库：<https://github.com/holderlink/dsh-cover-lint>
- 工具：`cover_lint`
- 安装：

```powershell
dsh plugin --profile desktop add github:holderlink/dsh-cover-lint
```

## 5. Tutorial Check

**长教程变可勾选清单。**

把安装教程存成 `- [ ]` / `- [x]` 的 markdown，记录每一步是否真的做过；`check` / `uncheck` / `add` / `reset`。

- 仓库：<https://github.com/holderlink/dsh-tutorial-check>
- 工具：`tutorial_check`
- 安装：

```powershell
dsh plugin --profile desktop add github:holderlink/dsh-tutorial-check
```

## 一起装

```powershell
dsh plugin --profile desktop add github:holderlink/fishclick
dsh plugin --profile desktop add github:holderlink/dsh-video-preflight
dsh plugin --profile desktop add github:holderlink/dsh-plugin-release
dsh plugin --profile desktop add github:holderlink/dsh-cover-lint
dsh plugin --profile desktop add github:holderlink/dsh-tutorial-check
```

## 环境

- Windows（FishClick 只支持 Windows；Video Preflight 跨平台）
- Python 3.9+、`pip install pillow`
- Video Preflight 还需要 `ffmpeg` / `ffprobe`

## License

MIT。每个插件仓库里各有一份 LICENSE。
