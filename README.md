# 小工 — Q版电子/软件工程师正文配图

> 把中文技术文章里的流程、架构、状态和隐喻，变成清爽、有技术气质、结构清晰的 16:9 横版正文配图。
>
> 数字 cel-shading | 小工 IP | 纯白背景 | 少量红橙蓝中文标注 | EasyClaw Skill

---

## 这是什么

小工配图是一个 EasyClaw Skill，为中文技术文章、博客、方法论内容生成正文配图。

核心思路：让文章里的关键判断、流程、结构或隐喻，由一位 Q版工程师角色「小工」站在旁边帮你讲解出来。图的主体是信息结构，小工是导游——不大不小，刚刚好。

默认视觉 IP 是「小工」：

- 深棕色短侧分 quiff 发型
- 黑色中框方眼镜（核心识别符号）
- 暖桃肤色，大圆眼，抿嘴微笑
- 深灰蓝衬衫卷袖（办公场景）/ 浅天蓝连体静电服（现场场景）
- 约 3.5 头身 Q版比例
- 干净数字 cel-shading 画风，纯色块硬边阴影

---

## 适合谁用

**适合：**

- 写技术文章，需要结构化配图的人
- 做 AI + 开发工具内容的人（Electron、Python、嵌入式、工控等）
- 想把「安装→配置→编码→打包」这类流程画清楚的人
- 想要统一视觉 IP，每篇文章配图风格一致的人

**不太适合：**

- 想要商业插画、品牌 KV 或精致矢量图的
- 想要复杂架构图、PPT 信息图的
- 想要可爱卡通、表情包风格的
- 想把大量正文塞进一张图里的

---

## 示例

![白板讲解](ian-xiaohei-illustrations/assets/reference/xiaogong-whiteboard-final.jpg)

*小工站在白板前讲解系统架构（图生图，基于参考底图）*

更多旧版小黑示例见 `examples/` 和 `ian-xiaohei-illustrations/assets/examples/`（风格校准用，不要复刻构图）。

---

## 安装

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
```

将 `ian-xiaohei-illustrations/` 目录放入 EasyClaw 的 skills 目录即可。

---

## 怎么用

### 只做配图规划

```
分析这篇文章哪里值得配图，输出 shot list。
每张图：放在哪段后、主题、核心意思、结构类型、小工做什么、服装体系、中文标注词。
```

### 直接生成配图

```
为这篇文章生成 4-6 张正文配图。16:9 横版，纯白背景，小工 IP。
```

### 切换服装体系

- 软件/办公场景 → 自动用深灰蓝衬衫（体系A）
- 工厂/硬件/现场 → 自动用浅天蓝静电服（体系B）

---

## 视觉风格

- 纯白背景，无纹理无渐变
- 数字 cel-shading：中等粗细黑色轮廓线，硬边阴影，纯色块平涂
- 结构图/流程图是画面主体，小工是旁边的讲解者（高度不超过画面 30%）
- 少量中文标注（5-8处，2-8字/处）
- 红色：重点/问题/提醒 | 橙色：流程/箭头 | 蓝色：补充说明
- 一张图只讲一个核心结构

---

## 核心文件

| 文件 | 用途 |
|------|------|
| `SKILL.md` | Skill 入口，工作流定义 |
| `references/xiaohei-ip.md` | 小工 IP 形象、服装、动作、禁止项 |
| `references/style-dna.md` | 风格 DNA、色值、约束 |
| `references/composition-patterns.md` | 构图类型与原创隐喻方法 |
| `references/prompt-template.md` | 图生图/文生图 Prompt 模板 |
| `references/qa-checklist.md` | 生成后检查清单 |
| `assets/reference/xiaogong-front.png` | 图生图参考底图 |

---

## 目录结构

```text
ian-xiaohei-illustrations/
├── SKILL.md                          # Skill 入口
├── agents/openai.yaml
├── assets/
│   ├── examples/                     # 旧版小黑示例（风格校准）
│   └── reference/                    # 小工参考底图
│       ├── xiaogong-front.png
│       ├── xiaogong-whiteboard-final.jpg
│       └── xiaogong-whiteboard-sample.jpg
└── references/
    ├── xiaohei-ip.md                 # 小工 IP 定义
    ├── style-dna.md                  # 风格 DNA
    ├── composition-patterns.md       # 构图模式
    ├── prompt-template.md            # Prompt 模板
    └── qa-checklist.md              # QA 检查清单
```

---

## 迭代历程

- **v2.0** — 从「小黑」改为「小工」：黑色怪物 → Q版工程师，手绘怪诞 → 数字 cel-shading，增加两套服装体系，图生图优先策略确保形象一致
- **v1.0** — 初版小黑：黑色实心怪物，白点眼，手绘抖动线条，怪诞产品草图风格

---

## License

MIT License. See [LICENSE](LICENSE).
