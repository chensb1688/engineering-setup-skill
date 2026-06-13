# Engineering Setup Skill

多agent，多智能体参与的工程，使用标配的文件体系 — 任何工程/项目的接入手则、工作记录、踩坑记录、任务清单、操作规范。可以最大限度的降低沟通token，而且有效提升效率。
无需创建任何沟通文件，一句话就可以让任何平台型的agent介入你的工程，而且随时来随时走。

## 结构

```
engineering-setup-skill/
├── SKILL.md           ← 技能描述（可被 OpenClaw 加载）
├── templates/         ← 模板文件，新建工程时直接复制
│   ├── ENTRY.md
│   ├── work_log.md
│   ├── tasks.md
│   ├── pitfalls.md
│   ├── standards.md
│   └── README.md
└── README.md          ← 本文件
```

## 使用方法

```bash
# 新建工程时
mkdir -p 你的工程名
cp -r templates/* 你的工程名/
cd 你的工程名
# 然后替换占位符 {工程名} {一句话描述} {负责人} 等
```

## 参考案例

[Comfy Master Engine](/Volumes/book/comfy-master-engine/) — 完整示范了这套文件体系的实际使用。

## 许可

可自由使用、修改、分发。
