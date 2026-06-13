---
name: engineering-setup
description: 任何工程/项目的标配文件体系。含接入手则(ENTRY.md)、工作记录(work_log.md)、踩坑记录(pitfalls.md)、任务清单(tasks.md)、操作规范(standards.md)。新工程初始化时自动生成。
version: 1.0.0
author: Hermes 整理 · 老板 定稿
platforms: [macos, linux, windows]
tags: [工程模板, 项目管理, 多agent协作, 规范]
---

# Engineering Setup — 工程标配文件体系

每个工程/项目必须包含以下 6 个标配文件（放在工程根目录）：

```
工程根目录/
├── ENTRY.md       ← 🚪 接入手则：新人/新Agent的第一站
├── work_log.md    ← 📋 工作记录：按时间线推进，谁做了什么
├── tasks.md       ← 📌 任务清单：待办/进行中/已完成
├── pitfalls.md    ← 💥 踩坑记录：所有踩过的坑
├── standards.md   ← 📐 操作规范：数据库读写、命名等约定
└── README.md      ← 📖 工程概述：一句话+目录树+架构
```

## 快速使用

```bash
# 1. 新建工程时，把模板文件复制过去
cp -r templates/* 你的工程目录/

# 2. 替换模板中的 {占位符}
# 3. 开始干活
```

## 初始化步骤

```bash
mkdir -p {工程名}/data/{raw,processed,knowledge}
mkdir -p {工程名}/src {工程名}/scripts
mkdir -p {工程名}/models {工程名}/outputs {工程名}/docs
```

然后逐文件填入模板内容（见 `templates/` 目录）。

## 规则

1. **先看 ENTRY.md** — 新 Agent/新人接入的第一站
2. **推进必记 work_log.md** — 不事后补，每步做完立刻写
3. **遇坑必记 pitfalls.md** — 现象+根因+解决+预防，缺一不可
4. **任务清单可追踪** — tasks.md 标记状态，完成才勾
5. **standards.md 强制执行** — 不管谁来都得遵守
6. **README 只给概览** — 详细内容分散到其他文件，不堆在一处

## 参考案例

- `/Volumes/book/comfy-master-engine/` — ComfyUI 主模型工程，完整示范了这套文件体系
