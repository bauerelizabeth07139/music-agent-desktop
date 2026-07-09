# 🎵 Music Agent Desktop

AI 音乐工作站 — 基于 MiMo API 的一站式音乐创作工具

## 功能

- 🎤 **AI 歌词生成** — 输入主题，自动生成中文歌词
- 🎙️ **TTS 人声合成** — MiMo TTS 演唱，支持多种音色
- 🎹 **智能编曲** — AI 自动设计音轨结构（钢琴、吉他、贝斯、鼓、弦乐等）
- 🎵 **音符生成** — LLM 为每个乐器生成专业音符序列
- 🔊 **多轨渲染** — 合成引擎渲染所有乐器 + 人声混合
- 🎧 **在线试听** — 内置播放器，支持下载 master/multitrack/单轨

## 快速开始

### 方式一：运行 start.bat（推荐）

1. 下载 music-agent-desktop.zip
2. 解压到任意目录
3. 编辑 .env 文件，填入你的 MiMo API Key
4. 双击 start.bat 启动

### 方式二：手动启动

`ash
pip install -r requirements.txt
python launch_window.py
`

## 配置

编辑 .env 文件：

`
MIMO_API_KEY=你的MiMo API密钥
MIMO_BASE_URL=https://api.xiaomimimo.com
MIMO_MODEL=mimo-v2.5
MIMO_TTS_MODEL=mimo-v2.5-tts
`

## 技术栈

- **前端**: React + Vite
- **后端**: Python FastAPI
- **AI**: MiMo LLM (歌词/编曲/音符) + MiMo TTS (人声合成)
- **音频**: NumPy + SoundFile 合成引擎

## 系统要求

- Windows 10/11
- Python 3.8+
- 2GB+ 磁盘空间