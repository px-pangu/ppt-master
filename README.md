# PPT Master · AI Presentation Workflow

> AI 驱动的演示文稿工作流：生成可编辑 PPTX、还原页面视觉、复用 Brand/Style/Layout 工作区、填充原生模板

![Type](https://img.shields.io/badge/type-Agent%20Skill-4a6b7c)
![Upstream](https://img.shields.io/badge/upstream-ppt-master%20v6.7.2%20-%20作者%20Hugo%20He（MIT）-8f8a80)
![License](https://img.shields.io/badge/license-见 LICENSE-b8935a)

> ⚠️ 本仓库是个人使用环境中的 Skill 归档副本，**版权归原提供方**：ppt-master v6.7.2 · 作者 Hugo He（MIT）

## 这是什么

不是「一键生成 PPT」，而是一套**带工作区的演示文稿生产流程**：先建立 Brand / Style / Layout 三层可复用资产，再产出 Deck，最后还能回头改、还原、增强。

## 核心能力

| 能力 | 说明 |
|---|---|
| 生成 Deck | 从主题、大纲、文档或数据产出可编辑的 `.pptx` |
| 页面视觉还原 | 给一张参考图，还原成可编辑的版式 |
| 工作区复用 | Brand（品牌）/ Style（风格）/ Layout（版式）三层资产 |
| 模板填充 | 把内容灌进原生 PPTX 模板，不破坏母版 |
| 成品增强 | 加旁白、加动画、生成自运行视频 |

## 强制加载顺序

`SKILL.md` 里定义了 Mandatory Load Order：先读工作区资产，再读版式规则，最后才动页面。跳序会直接导致版式漂移。

## 依赖

```bash
pip install -r requirements.txt
```

图片生成后端通过 `.env` 配置（`openai` / `gemini` / `qwen` / `zhipu` / `volcengine`），参考 `.env.example`。**本仓库不含任何真实密钥**。

## 目录结构

```
ppt-master/
├─ SKILL.md              工作流主控 + 加载顺序 + 执行纪律
├─ workflows/            各阶段流程定义
├─ references/           版式、美学、兼容性参考
├─ scripts/              生成 / 还原 / 增强脚本
├─ templates/            模板与预设资产
├─ requirements.txt
├─ .env.example          图片生成后端配置样例（全为占位符）
├─ LICENSE               MIT（原样保留）
└─ SPONSORS.md / SPONSORS_CN.md
```

## 许可

**MIT** —— 原包许可，`LICENSE` 原样保留。
Copyright (c) 2025-2026 Hugo He，详见 `NOTICE.md`。


## 安装

```bash
git clone https://github.com/px-pangu/ppt-master.git ~/.workbuddy/skills/ppt-master
# Claude Code：~/.claude/skills/ppt-master
```

> 若原包依赖 CLI（如 `kdocs`、`ima`、`wecom`、`pdfkit`），需先按 `SKILL.md` 的安装与认证段落配置本机环境。**仓库内不含任何凭据。**

