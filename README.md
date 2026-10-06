# Coze Video Workflows

> 基于 Coze 平台搭建的多模态视频生成应用工作流合集，包含图片生成、视频生成、成片合成等完整流程。

[![Coze](https://img.shields.io/badge/Coze-Workflow-blue)](https://www.coze.cn/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## ✨ 特性

- 🎨 **AI 图片生成**：基于文本描述生成高质量图片
- 🎬 **AI 视频生成**：图片/文本生成视频片段
- 🎞️ **成片合成**：多片段合成完整视频
- 🔄 **全流程自动化**：从文本到成片一键生成
- 🧩 **模块化工作流**：每个环节独立工作流，可自由组合

---

## 🏗️ 工作流总览

```
文本描述
   │
   ▼
┌─────────────────────┐
│ create_image-draft   │  生成关键帧图片
└──────────┬──────────┘
           │
   ┌───────▼────────┐
   │ create_video    │  图片生成视频片段
   │  -draft         │
   └───────┬────────┘
           │
   ┌───────▼────────┐
   │ produce-draft   │  多片段合成成片
   └───────┬────────┘
           │
   ┌───────▼────────┐
   │ get_produce     │  获取成片结果
   │  -draft         │
   └───────┬────────┘
           │
           ▼
        最终视频
```

---

## 📁 工作流清单

| 工作流文件 | 功能 |
|-----------|------|
| `workflows/Workflow-create_image-draft-1329/` | 图片生成草稿 |
| `workflows/Workflow-create_video-draft-1324/` | 视频生成草稿 |
| `workflows/Workflow-produce-draft-1308/` | 成片合成 |
| `workflows/Workflow-get_produce-draft-1319/` | 获取成片状态 |
| `workflows/Workflow-get_video-draft-1314/` | 获取视频草稿状态 |

---

---

## 📁 项目结构

```
.
└── workflows/                      # Coze 工作流合集
    ├── Workflow-create_image-draft-1329/   # 图片生成草稿
    ├── Workflow-create_video-draft-1324/   # 视频生成草稿
    ├── Workflow-produce-draft-1308/        # 成片合成
    ├── Workflow-get_produce-draft-1319/    # 获取成片状态
    └── Workflow-get_video-draft-1314/      # 获取视频草稿状态
```


## 🚀 快速开始

### 导入步骤

1. 登录 [Coze 平台](https://www.coze.cn/)
2. 进入「工作流」→「导入工作流」
3. 选择对应目录下的 `MANIFEST.yml` 导入
4. 配置大模型插件（图片生成、视频生成等）
5. 保存并发布

### 使用方式

方式一：单独使用各工作流
- 调用 `create_image-draft` 生成图片
- 调用 `create_video-draft` 生成视频
- 调用 `produce-draft` 合成成片

方式二：编排为 Bot
- 将多个工作流串联到一个 Bot 中
- 用户输入文本描述，自动完成全流程

---

## 📚 相关课程

- 📖 课程文档：[飞书知识库](https://scnxinvxtnbo.feishu.cn/wiki/Dk3zwHXXSi87xDkgcyOcoOHVnHg)
- 🎥 视频教程：[课程链接](#)（待补充）

---

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.
