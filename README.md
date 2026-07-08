# Music Agent Desktop

AI编曲工作站桌面版 - 基于小米MiMo模型

## 快速开始

1. 下载最新Release
2. 解压文件
3. 运行 `start.bat`
4. 在 `.env` 文件中设置你的 MiMo API Key

## 功能特性

- 🎵 AI歌词生成
- 🎤 TTS人声合成
- 🎹 多轨编曲
- 🎸 乐器合成
- 🗣️ 声音克隆
- 🎨 深色/浅色主题

## 技术栈

- **后端**: Python, FastAPI, MiMo API
- **前端**: React, Vite
- **AI**: 小米MiMo v2.5

## 配置

在 `.env` 文件中设置:

```
MIMO_API_KEY=your_api_key_here
MIMO_BASE_URL=https://api.xiaomimimo.com
MIMO_MODEL=mimo-v2.5
MIMO_TTS_MODEL=mimo-v2.5-tts
```

## 许可证

MIT
