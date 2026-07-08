# Music Agent Desktop

<p align="center">
  <h1 align="center">🎵 Music Agent Desktop</h1>
  <p align="center">基于 <b>小米 MiMo</b> 的 AI 编曲工作站 - 桌面版</p>
  <p align="center">用自然语言驱动作曲、编曲、配音与混音的一体化音乐创作工具。</p>
</p>

![Platform](https://img.shields.io/badge/platform-Windows%20x64-blue)
![Python](https://img.shields.io/badge/python-3.8+-3776ab)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 📖 项目简介

**Music Agent Desktop** 是 [Music Agent](https://github.com/bauerelizabeth07139/music-agent) 的桌面打包版本，以 **小米 MiMo 系列模型** 为核心，面向音乐创作场景，提供 AI 编曲、文本转语音（TTS）、声音克隆与多轨混音能力。

它将 MiMo 的生成能力与前端可视化编排体验结合，帮助创作者用一句话完成从创意到可播放 Demo 的流程。

---

## ✨ 核心特性

| 功能 | 说明 |
|------|------|
| 🎼 **自然语言编曲** | 用中文/英文描述音乐风格与结构，AI 自动生成多轨方案 |
| 🎙️ **TTS 语音合成** | 文本转语音，支持多种角色声线（冰糖、茉莉、苏打等） |
| 🧬 **声音克隆** | 上传/拖拽音频样本，快速构建个性化语音合成 |
| 🎹 **10 种乐器** | 钢琴、吉他、贝斯、鼓、小提琴、大提琴、长笛、小号、合成铺底、合成领奏 |
| 🎛️ **混音与试听** | 分轨播放、音量控制、快速导出整体 Demo |
| 🌓 **暗色/亮色主题** | Codex 风格 UI，支持日间/夜间模式切换 |

---

## 🚀 快速开始

### 前置条件

- [Python 3.8+](https://python.org)
- [MiMo API Key](https://mimo.mi.com)（免费注册即可获取）

### 使用步骤

1. **下载** 最新 Release 并解压
2. **配置** API Key：编辑 `.env` 文件，填入你的 MiMo API Key
3. **运行** `start.bat`（Windows 双击即可）
4. **访问** http://localhost:5173 开始创作

```bash
# 或者手动启动
pip install -r requirements.txt
cd server
python -m uvicorn app:app --host 127.0.0.1 --port 8000
```

---

## ⚙️ 配置说明

### 环境变量 (.env)

```env
MIMO_API_KEY=your-api-key-here
MIMO_BASE_URL=https://api.xiaomimimo.com
MIMO_MODEL=mimo-v2.5
MIMO_TTS_MODEL=mimo-v2.5-tts
```

也可以在应用侧边栏中实时配置 API 参数。

### MiMo 预设配置

| 预设名称 | Base URL | 模型 |
|----------|----------|------|
| MiMo 按量付费（API） | https://api.xiaomimimo.com | mimo-v2.5-pro |
| MiMo Token Plan 国内集群 | https://token-plan-cn.xiaomimimo.com | mimo-v2.5-pro |
| MiMo Token Plan 新加坡集群 | https://token-plan-sg.xiaomimimo.com | mimo-v2.5-pro |
| MiMo V2.5（全模态） | https://api.xiaomimimo.com | mimo-v2.5 |
| MiMo V2 Flash（轻量） | https://api.xiaomimimo.com | mimo-v2-flash |

---

## 🔑 MiMo API Key 测试结果

| 模型 | 状态 | 说明 |
|------|------|------|
| mimo-v2.5 | ✅ 可用 | 全模态模型，用于编曲生成 |
| mimo-v2.5-pro | ✅ 可用 | 推理旗舰模型 |
| mimo-v2.5-tts | ✅ 可用 | 文本转语音，用于歌声合成 |

---

## 📁 目录结构

```
music-agent-desktop/
├── server/               # 后端服务
│   ├── app.py            # FastAPI 主应用
│   ├── config.py         # 配置与预设
│   ├── llm_client.py     # LLM/TTS 客户端
│   └── skills/           # 后端技能
├── skills/               # 音乐与乐器 Skill
│   ├── instruments/      # 乐器技能
│   └── music-search/     # 音乐搜索
├── frontend-dist/        # 前端构建产物
├── .env.example          # 环境变量模板
├── requirements.txt      # Python 依赖
├── start.bat             # Windows 启动脚本
└── README.md
```

---

## 🛠️ 技术栈

- **后端**: Python 3.8+, FastAPI, Uvicorn
- **前端**: React 18, Vite, TypeScript
- **AI 模型**: 小米 MiMo v2.5 系列
- **音频处理**: NumPy, SoundFile

---

## 📄 许可证

[MIT License](LICENSE)

---

## 🔗 相关链接

- **源码仓库**: [music-agent](https://github.com/bauerelizabeth07139/music-agent)
- **MiMo 官网**: [mimo.mi.com](https://mimo.mi.com)
- **MiMo API 文档**: [platform.xiaomimimo.com](https://platform.xiaomimimo.com)
