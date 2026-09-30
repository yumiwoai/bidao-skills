# 毕导双技能：写作方法论 + 短视频方法论

从 UP 主「毕导」的公开内容中，用 [cangjie-skill](https://github.com/kangarooking/cangjie-skill) 五阶段蒸馏流水线（语料理解 → 五提取器并行提取 → 三重验证 → RIA++ 能力卡 → Zettelkasten 互链 → 盲测 → 编译）产出的两个**互相独立**的技能。

两个技能分别蒸馏自不同媒介的语料，能力卡零重叠、互不引用，各自回答各自领域的问题。

## 技能一览

| | bidao-writing | bidao-video |
|---|---|---|
| 语料 | 140 篇公众号文章 | 40 个科普短视频（ASR 转写） |
| 能力卡 | 22 张 | 42 张 |
| 适用场景 | 公众号/新媒体文章写作：选题、标题、结构、幽默语言、结尾、留言互动、软广植入 | 科普短视频：口播稿、脚本、分镜、开场钩子、结尾设计、实验演示、弹幕互动 |
| 不适用 | 学术论文、公文、新闻通稿、纯文学创作 | 公众号文章（走 bidao-writing）、纪录片旁白、严肃科教片、纯文学剧本 |
| 盲测 | 10/10 通过 | 10/10 通过（含跨界请求正确路由/拒绝用例） |

### bidao-writing 核心原则（速览）

1. 形式越庄严、内容越荒唐，落差即笑点；一切知识都是小学二年级，用最低姿态处理最学术的材料
2. 真做实验、真调查，笨功夫即内容壁垒，数据可回溯、局限声明前置
3. 先坏后好：教完坏招必须正能量兜底，升华之后必亲手消解煽情
4. 选题翻日历不翻灵感；标题自己先成一个包袱（承诺 + 拆台）
5. 互动装置与广告都要从正文梗里长出来，奖品本身就是全文最后一个包袱

### bidao-video 核心原则（速览）

1. 前 15 秒反常识钩子，禁铺垫
2. 能动手绝不只讲文献，翻车也是内容
3. 庄谐落差必须落到知识点
4. 结构递进明示编号，可报位
5. 结尾三拍收束，钩子拴未解子问题
6. 不确定性明说，n 与前提在结论之前

## 目录结构

```
bidao-skills/
├── bidao-writing/          # 技能 1：公众号写作方法论（22 能力卡）
│   ├── SKILL.md            # 入口：触发条件、核心原则、能力路由表
│   ├── BUILD_MANIFEST.json
│   └── references/
│       ├── capabilities/   # 22 张 RIA++ 能力卡
│       ├── capability-index.md
│       ├── cheatsheet.md
│       ├── glossary.md
│       └── overview.md
├── bidao-video/            # 技能 2：科普短视频方法论（42 能力卡 · 115 条互链）
│   ├── SKILL.md
│   ├── BUILD_MANIFEST.json
│   └── references/
│       ├── capabilities/   # 42 张 RIA++ 能力卡
│       ├── capability-index.md
│       ├── cheatsheet.md
│       ├── glossary.md
│       └── overview.md
└── docs/
    ├── 毕导写作方法论精华-DIGEST.md    # 文章版蒸馏全文纪要
    └── 毕导短视频方法论精华-DIGEST.md  # 视频版蒸馏全文纪要
```

## 安装

技能遵循标准 SKILL.md 格式（frontmatter 含 name / description），可被支持 Skills 机制的 agent 加载。

```bash
# Claude Code / 兼容 agent
git clone https://github.com/yumiwoai/bidao-skills.git
cp -r bidao-skills/bidao-writing bidao-skills/bidao-video ~/.claude/skills/
```

TRAE 用户可复制到本机技能目录后重启会话生效。

## 蒸馏方法

两套语料各自走完 cangjie-skill 全流水线：

- 阶段 0：Adler 式通读理解，建立能力域地图
- 阶段 1：原则/案例/框架/反例/术语五提取器并行提取（视频版产出 153 张候选卡）
- 阶段 1.5：三重验证 + 晋级门，收敛为定稿能力卡（视频版 153 → 42）
- 阶段 2：RIA++ 能力卡（识别 → 理解 → 应用 → 反例 → 失效边界）
- 阶段 3：Zettelkasten 互链（视频版 115 条，构成可组合的方法网络）
- 阶段 4：盲测压力测试（各 10 用例，含正例/反例/边界，全部通过）
- 阶段 5：编译为单入口技能包

## 边界与诚实声明

- 语料为单一创作者的公开内容，方法论带有强烈的个人风格，不适配所有账号定位
- 视频版语料为 ASR 转写，口语噪声已在提取阶段清洗，但少量转写误差可能残留
- 能力卡中的全部数据与案例均锚定原文，未做外推或虚构
