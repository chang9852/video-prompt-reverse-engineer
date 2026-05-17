# 🎬 Auto Video Prompt Reverse Engineer v3.1

> 上传视频 → 自动拆解分镜 → 逆向生成 AI Prompt → 一键复刻视频风格

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://clawhub.ai)
[![Version](https://img.shields.io/badge/version-3.1.0-brightgreen)](https://github.com)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

## 📖 简介

**视频提示词逆向分析专家（Video Prompt Reverse Engineer）** 是一个 OpenClaw Skill，专为 AI 视频创作者设计。输入视频链接、截图或描述，自动输出：

- 🔍 **分镜拆解** — 逐镜头分析景别、运镜、构图、光影、色彩
- 🎨 **风格识别** — 导演风格、电影类型、动画/CG/广告风格、AI 痕迹检测
- 🧠 **Prompt 逆向** — Positive/Negative/Camera/Style/Lighting 结构化 Prompt
- 🛠 **模型适配** — 支持 Kling、Seedance、Runway、Veo、Sora、Pika、SVD、HappyHorse 等 10+ 模型
- 📋 **复刻工作流** — 关键帧生成 → 视频生成 → 调色 → 增强 → 合成，完整 8 步

## 🎯 适用场景

- 📹 看到一个酷炫的 AI 视频，想复刻它的风格
- 🎓 学习 AI 视频创作的分镜和 Prompt 技巧
- 🚀 快速生成同风格视频的 Prompt 模板
- 📚 研究 AI 视频模型的视觉特征和参数配置

## 📦 安装

### 方式一：ClawdHub 安装

`ash
npx skills install jacky1n7/video-prompt-reverse-engineer
`

### 方式二：GitHub 克隆

`ash
# 克隆到 OpenClaw skills 目录
git clone https://github.com/jacky1n7/video-prompt-reverse-engineer.git \
  ~/.openclaw-autoclaw/skills/video-prompt-reverse-engineer
`

### 方式三：手动安装

1. 下载 .skill 文件
2. 放到 ~/.openclaw-autoclaw/skills/ 目录下
3. 重启 OpenClaw

## 🚀 快速使用

### 1. 分析视频链接

`
分析这个视频：https://www.bilibili.com/video/BV1FFRQB2Eqw/
`

### 2. 分析截图

发送视频截图，Skill 会自动识别风格并逆向生成 Prompt。

### 3. 分析文字描述

`
分析这种风格：末世废土+机器人牛仔+原子朋克+电影感光影
`

## 📂 文件结构

`
video-prompt-reverse-engineer/
├── SKILL.md                       # 核心 Skill 文件（分析规则+输出格式+Prompt模板）
└── references/
    └── model_params.md            # 模型参数速查表（10+模型+镜头焦段+调色+LUT+胶片模拟+导演风格+HappyHorse适配）
`

## 🎨 支持的模型

| 模型 | 强项 | Prompt 特点 |
|------|------|------------|
| **Seedance 2.0** | 沉浸式短片、音画同步 | 场景参考图 + 角色图 + 文字指令 |
| **Kling (可灵)** | 多角度生成、质感好 | 中文 Prompt 优化，支持关键帧 |
| **HappyHorse (快马)** | 广告/科技风格、带配音 | 广告公式、音频标注符号 |
| **Runway Gen-3** | 摄影机运镜控制 | Pan/Zoom/Roll 控制词 |
| **Veo** | 长叙事、高级电影语言 | 摄影级自然语言 |
| **Sora** | 复杂物理、长镜头 | 叙事型 Prompt |
| **Pika** | 快速迭代 | 短 Prompt + motion 参数 |
| **SVD** | 图生视频 | motion_bucket_id 控制 |

## 🔧 输出示例

每次分析输出结构化报告：

`
# 视频整体风格分析
## 视频类型 / 整体风格 / 导演参考 / 剪辑节奏 / 模型推测

# 分镜拆解（每个镜头）
## Shot 01
- 景别/运镜/构图/光影/色彩/主体动作/材质质感
- Prompt / Negative Prompt / Camera Prompt / Style Prompt / Lighting Prompt

# 参数推测
- 宽高比 / FPS / 镜头焦段 / LUT风格 / 色温 / 景深 / 快门感 / 胶片感

# 复刻工作流
1. MJ/Flux 生成关键帧
2. Kling/Seedance/HappyHorse 视频生成
3. DaVinci 调色
4. Topaz 增强
5. Premiere 合成
`

## 🧑‍💻 创作者方法论

> "好的提示词更像导演台本，而不是命令式指令。角色为什么移动、为什么停顿、为什么有情绪，这些因果逻辑会直接影响 AI 最终生成的状态。" —《丧尸清道夫》创作者

**Skill 内置的创作原则：**

- ✅ 告诉 AI「角色为什么做」，而非只写「做什么」
- ✅ 用 Prompt 替代分镜图：场景参考图 + 角色图 + 文字指令
- ✅ 保留 AI 生成的意外惊喜，融入叙事
- ✅ 片尾标注所有使用的 AI 模型

## 📄 License

MIT License

## 🤝 贡献

欢迎提交 Issue 和 PR！

- 🐛 报告 Bug
- 💡 提议新功能
- 📚 补充模型参数
- 🎬 分享你用它分析的案例

---

**用 AI 复制 AI 视频风格，从逆向 Prompt 开始** 🎬