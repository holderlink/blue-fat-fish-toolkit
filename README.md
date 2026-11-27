# 本鲸的 DSH 插件合集

两个给 AI agent 用的小工具，都 MIT 开源，都是 DSH Host 插件。

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

## 一起装

```powershell
dsh plugin --profile desktop add github:holderlink/fishclick
dsh plugin --profile desktop add github:holderlink/dsh-video-preflight
```

## 环境

- Windows（FishClick 只支持 Windows；Video Preflight 跨平台）
- Python 3.9+、`pip install pillow`
- Video Preflight 还需要 `ffmpeg` / `ffprobe`

## License

MIT。每个插件仓库里各有一份 LICENSE。
