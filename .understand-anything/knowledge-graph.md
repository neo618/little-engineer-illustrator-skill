# ian-xiaohei-illustrations — 知识图谱分析

> **分析时间**: 2026-06-19 13:35 UTC  
> **语言**: Markdown, YAML  
> **框架**: codex-skill  
> **描述**: 中文小黑怪诞正文配图生成 Skill | 16:9 白底手绘 | 少量红橙蓝批注

---

## 📊 项目文件清单（21个节点）

### 🔑 Skill 核心
| 文件 | 复杂度 | 摘要 |
|------|--------|------|
| `ian-xiaohei-illustrations/SKILL.md` | 🔴 复杂 | Skill 主文件：定义小黑配图的完整流程——分析文章、输出 shot list、逐张生图、QA 检查、保存输出 |

### 🎨 风格系统（5个文件）
| 文件 | 复杂度 | 摘要 |
|------|--------|------|
| `references/style-dna.md` | 🟡 中等 | 风格 DNA 定义：纯白背景、黑色手绘线稿、颜色系统（黑/红/橙/蓝）、禁忌列表 |
| `references/xiaohei-ip.md` | 🟡 中等 | 小黑 IP 角色定义：外形（黑实心/白点眼/细腿）、性格（认真荒诞） |
| `references/composition-patterns.md` | 🟡 中等 | 构图模式库：8 种结构类型、隐喻方法、物件库 |
| `references/prompt-template.md` | 🟡 中等 | 生图 Prompt 模板：标准/去标题/增强怪诞感三套 |
| `references/qa-checklist.md` | 🟡 中等 | QA 检查清单：12 项通过标准 + 11 类重触发 + 6 种迭代方向 |

### 📖 示例与文档（12个文件）
| 文件 | 复杂度 | 摘要 |
|------|--------|------|
| `README.md` | 🟡 中等 | 项目主页：介绍、适用场景、安装方法、使用示例 |
| `examples/prompts.md` | 🟢 简单 | 5 种典型场景的 prompt 模板 |
| `examples/images/01-two-breakpoints.png` | 🟢 简单 | 示例配图：两个断点 |
| `examples/images/02-sort-by-purpose.png` | 🟢 简单 | 示例配图：按目的分类 |
| `examples/images/03-one-fish-many-uses.png` | 🟢 简单 | 示例配图：一鱼多吃 |
| `examples/images/04-handoff-path.png` | 🟢 简单 | 示例配图：承接路径 |
| `examples/images/05-information-well.png` | 🟢 简单 | 示例配图：信息井 |
| `examples/images/06-idea-press.png` | 🟢 简单 | 示例配图：想法压榨机 |
| `examples/images/07-content-fermentation.png` | 🟢 简单 | 示例配图：内容发酵 |
| `examples/images/08-trust-bridge.png` | 🟢 简单 | 示例配图：信任桥 |
| `LICENSE` | 🟢 简单 | MIT 开源许可证 |
| `NOTICE.md` | 🟢 简单 | 版权声明和使用说明 |

### ⚙️ 配置（2个文件）
| 文件 | 复杂度 | 摘要 |
|------|--------|------|
| `agents/openai.yaml` | 🟢 简单 | OpenAI 平台的 Agent 配置 |
| `.gitignore` | 🟢 简单 | Git 忽略规则 |

### 📦 资源文件（1个）
| 文件 | 复杂度 | 摘要 |
|------|--------|------|
| `assets/ian-wechat-qr.jpg` | 🟢 简单 | 作者微信二维码图片 |

---

## 🔗 关系图谱（15条边）

### 核心依赖链（SKILL.md 出发）
```
SKILL.md
  ├── references ──→ style-dna.md          (风格指令)
  ├── references ──→ xiaohei-ip.md         (角色指令)
  ├── references ──→ composition-patterns.md (构图指令)
  ├── references ──→ prompt-template.md    (模板指令)
  ├── references ──→ qa-checklist.md       (QA 指令)
  ├── related ────→ README.md              (项目入口)
  ├── related ────→ examples/prompts.md    (使用示例)
  └── configures ──→ openai.yaml           (Agent 配置)
```

### README 关系网
```
README.md
  ├── documents ──→ SKILL.md               (安装核心)
  ├── documents ──→ examples/prompts.md    (使用示例)
  ├── related ───→ LICENSE
  └── related ───→ NOTICE.md
```

### 风格系统内部交叉引用
```
xiaohei-ip.md ──→ style-dna.md        (角色→风格)
style-dna.md  ──→ qa-checklist.md     (风格→质检)
composition-patterns.md ──→ prompt-template.md (构图→模板)
```

---

## 🗂️ 逻辑分层

| 层级 | 节点数 | 说明 |
|------|--------|------|
| **Skill 核心** | 1 | Skill 主文件及核心引用 |
| **风格系统** | 5 | 视觉风格、角色 IP、构图模式、模板、质检 |
| **示例与文档** | 12 | 使用示例、示例图片、项目文档 |
| **配置** | 2 | Agent 配置、Git 配置 |
| **资源文件** | 1 | 作者微信二维码 |

---

## 🧭 学习导览

| 步骤 | 标题 | 内容 |
|------|------|------|
| 1 | **项目概览** | 从 README 了解这个 skill：为中文文章生成小黑怪诞风格的正文配图 |
| 2 | **核心入口** | SKILL.md 是大脑——完整流程：分析→shot list→生图→QA |
| 3 | **理解风格** | style-dna.md + xiaohei-ip.md：纯白、手绘、小黑 IP、颜色系统 |
| 4 | **掌握构图** | composition-patterns.md：8 种构图模式 + 隐喻 + 反复刻规则 |
| 5 | **使用模板** | prompt-template.md：英文 Prompt 模板，每次生图填充变量 |
| 6 | **质检标准** | qa-checklist.md：12 项通过标准 + 迭代方案 |
| 7 | **看示例** | examples/prompts.md：5 种典型使用场景 |

---

## 🧬 核心洞察

这个 Skill 的设计思想是：**用严格的视觉约束（纯白 + 手绘 + 限色）+ 结构化的构图模式 + IP 角色一致性**，让 AI 生成的中文配图不会跑偏成「正经插图」或「AI 味浓」。它不是靠复杂的 prompt tricks，而是靠**层层约束叠加**来锁定风格。

工作流：**文章 → shot list（自动分析配图需求）→ 逐张生图（构图模式 + prompt 模板）→ QA 检查 → 输出**
