# product-research-to-design

[![中文](https://img.shields.io/badge/%E4%B8%AD%E6%96%87-red.svg)](README.md) [![English](https://img.shields.io/badge/English-blue.svg)](README.en.md)

> GitHub 仓库：<https://github.com/Tonya0411/product-research-to-design>

产品 / 工业设计项目「调研 → 设计落地」通用技能：把用户与行业调研一路推进到 PRD 与设计任务书。

## 这是什么

一个可复用的调研工作流技能，内置两套方法论 + 一份项目基线空白模板。它是一条为大多数产品 / 工业设计项目能套用的标准流程。

## 目录结构

```
product-research-to-design/
├── SKILL.md                  # 技能主文件：触发条件 + 七步流程 + 三条铁律
├── README.md / README.en.md  # 本说明（中 / 英）
└── references/
    ├── methodology/
    │   ├── Survey_method.md        # 问卷设计方法论
    │   └── Investgation_method.md  # 设计调研方法论（PSTP、一二手结合）
    └── templates/
        └── 项目基线空白模板.md       # 新建项目第一步要填的基线
```

## 适用场景

- 给新产品做用户需求调研或问卷设计
- 做一二手调研、交叉分析、提炼洞察与机会点
- 写调研综合报告、PRD、设计任务书
- 想要一套标准化的"调研 → 设计"流程与产出物格式

## 快速开始（三步上手）

1. **填基线**：复制 `references/templates/项目基线空白模板.md` 到你的项目目录，填好产品、目标用户、商业约束、保密约束、调研目标。
2. **跑流程**：按 `SKILL.md` 的七步流程推进——问卷设计 → 二手调研 → 一手调研 → 交叉分析 → 设计任务书 → PRD。
3. **出成果**：产出 6 份交付物（问卷、二手执行清单、一手数据整理、综合报告、设计任务书、PRD）。

## 具体使用方法（七步流程）

| 步骤 | 你要做什么 | 关键要点 | 产出物 |
|---|---|---|---|
| 0 项目基线 | 填 `项目基线空白模板.md` | 锁定产品/用户/价格/保密/调研目标 | 项目基线 |
| 1 问卷设计 | 按问卷方法论出题 | ≤20 题、封闭为主、漏斗排序、不剧透、注意力检验 | 可导入问卷星的 .txt |
| 2 二手调研 | PSTP 五抽屉查资料 | 先立 D1-D4 目标再检索；A/B/C/D 分层可信度 | 行业认知 + 执行清单 |
| 3 一手调研 | 回收问卷、整理数据 | 核对样本量、注意力通过率、交叉表 | 一手数据整理 |
| 4 交叉分析 | 一手×二手三角验证 | 洞察带双源支撑、机会点分级 | 综合报告 |
| 5 设计任务书 | 画像/场景/功能/约束/禁忌/验收 | 功能分必选/可选 | 设计任务书 |
| 6 PRD 落地 | 按 pm-skills 框架写 PRD | 模型产出必写 AI Behavior 与评测 | PRD |

## 三条铁律

1. **不虚构数据**：量化数据必须来自调研文档，没有的一律标【资料无记录】。
2. **不剧透设计概念**：对外调研材料用中性表述，不暴露目标形态/品牌/概念。
3. **数据溯源**：结论和图表都标注来源（【一手 Q几】/【二手】）。

## 安装方法

### 方式一：DSH 技能目录

把整个 `product-research-to-design` 目录复制到用户级技能目录：

```powershell
# Windows PowerShell
Copy-Item -Recurse -Force `
  "C:\路径\到\product-research-to-design" `
  "C:\Users\<你的用户名>\.agents\skills\product-research-to-design"
```

安装后，DSH 的可用技能列表会出现 `product-research-to-design`。

### 方式二：skills CLI（跨工具 / 可分享到 GitHub）

已托管在 GitHub，用 skills 生态安装：

```bash
npx skills add Tonya0411/product-research-to-design -g -y
```

## 在 DSH 里怎么调用

新建项目时，对助手说：

> 用 product-research-to-design 技能，帮我做 [某产品] 的用户调研和 PRD。

助手会先让你填项目基线，再按七步流程推进。

## 与 pm-skills 的关系

本技能的 PRD 落地遵循 GitHub [`product-on-purpose/pm-skills`](https://github.com/product-on-purpose/pm-skills) 的 `deliver-prd` 技能框架（v3.0.0）。若产品输出来自大模型，PRD 必须包含「AI Behavior and Evaluation」章节（拒绝 / 克制 / 隐私独立成行 + 阈值）。

## 常见问题

**Q：能跳过问卷，直接做二手调研吗？**
A：可以。七步是推荐顺序，若已有二手资料可先做二手（步骤 2），一手（步骤 1、3）按需后置。

**Q：非智能硬件（无大模型）项目能用吗？**
A：能。步骤 6 的「AI Behavior」一节按 pm-skills 约定可跳过，其余步骤完全适用。

**Q：保密约束怎么填？**
A：若产品形态需保密，对外材料用中性词（如"桌面智能陪伴产品"），并把需隐藏的概念写进模板「保密约束」栏。
