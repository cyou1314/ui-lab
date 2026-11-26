# 学习笔记：Topinspo 设计词汇站（Design Vocabulary）

- 学习日期：2026-11-26（用户 2026-11-25 收藏、2026-11-26 放行学习）
- 对象：https://topinspo.design/vocabulary （词条页示例：?term=skeleton）
- 抓取方式：读该站公开页面数据（词条全量数据嵌在其站点资源中），逐条核对

## 站点结构一句话

一部专为「跟设计师和 AI 把界面说清楚」编的 UI 词典：70 个词条按 8 个分类组织，每条给一句话定义、一个可切换的前后对照演示、易混淆词条的边界判语，外加一段可直接粘给 AI 的提示词（中英双版）。

组织细节：

- 8 个分类：间距 Spacing（6）/ 排版 Typography（9）/ 颜色 Color（6）/ 形状 Shape（8）/ 层次 Depth（5）/ 动效 Motion（9）/ 布局与组件 Layout & UI（16）/ AI 界面 AI Patterns（11），合计 70 条
- 另有一套「感受」索引，不按学科、按用户的不适感找词：看着挤 Cramped / 没重点 No focus / 发飘发脏 Muddy / 动效生硬 Stiff / 常见组件 UI patterns / AI 界面 AI UI——说不出术语时先认感受、再落到词条，这个入口设计本身值得借鉴
- 每条的固定结构：英文术语＋中文名 / 一句话定义 / 对照演示（两种做法一键切换，配图注）/ 易混淆对照（confusedWith，写清与近邻词条的边界）/「Say to AI」提示词（英文＋中文各一份）

## 词条全清单（名字＋一句话中文释义，释义为站方中文版原文）

### 间距 Spacing（6）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Padding | 内边距 | 内容到容器边缘的距离，太小文字就会贴着边 |
| Gap | 条目间距 | 列表、横排或网格里，相邻两项之间的距离 |
| Line Height | 行高 | 同一段文字里，行与行之间的距离，决定读着累不累 |
| Proximity | 亲密性 | 离得近的东西会被当成一组，间距要分出主次 |
| Whitespace | 留白 | 有意留出的空白，让重要的东西被看见 |
| Divider vs. Space | 分割线与留白 | 分组先用留白，留白不够时才用线 |

### 排版 Typography（9）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Hierarchy | 视觉层级 | 用字号、字重、颜色排出先看什么、后看什么 |
| Font Weight | 字重 | 字的粗细，空间紧的时候，加粗比放大更合适 |
| Tracking | 字距 | 字母之间的整体间距，大字要收，小号大写要放 |
| Tabular Numbers | 等宽数字 | 每个数字一样宽，列能对齐，跳动的数字不抖 |
| Text Balance | 标题平衡断行 | 让短标题每行差不多长，最后一行不剩一个孤字 |
| Line Clamp | 多行截断 | 文字超过几行就截断，结尾显示省略号 |
| Baseline Alignment | 基线对齐 | 大数字和小单位对齐到同一文字基线，别做垂直居中 |
| Shortcut Hint | 快捷键徽标 | 菜单右侧用等宽键帽标出快捷键，比行内括号更易扫读 |
| Middle Truncation | 中间截断 | 长文件名从中间省略，保留开头和关键后缀方便分辨 |

### 颜色 Color（6）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Accent | 强调色 | 把颜色只留给最重要的那一个操作 |
| Contrast | 对比度 | 文字和背景能分得多清楚，用比值来衡量 |
| Muted Text | 弱化文字 | 次要信息用更浅的灰，让主要内容先被读到 |
| Semantic Color | 语义色 | 带含义的颜色：绿是成功，黄是警告，红是出错 |
| Tint & Shade | 同色明暗阶 | 用同一色相的浅底配深字，替代刺眼的纯色块 |
| Disabled State | 禁用态 | 禁用按钮退为浅灰平底并去掉投影，不让人误以为能点 |

### 形状 Shape（8）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Border Radius | 圆角 | 边角有多圆，小一点、统一一点会更利落 |
| Concentric Radius | 同心圆角 | 内层圆角等于外层圆角减去两者之间的间距 |
| Nested Cards | 卡片套娃 | 卡片里套卡片，每多一层就多一圈边框、阴影和浪费的空间 |
| Hairline Border | 极细描边 | 很细、很淡的边框，勾出轮廓又不显得重 |
| Optical Alignment | 视觉对齐 | 把图形挪一点点，让它看起来居中，而不只是数值上居中 |
| Avatar Stack | 叠加头像组 | 多人头像负间距叠放并加白边切割，省空间又不粘连 |
| Icon Container | 图标容器 | 把形状各异的图标装进统一圆角底托，左侧纵轴整齐稳重 |
| Badge Counter | 数字角标 | 数字角标超 99 封顶且自适应撑开，数量为 0 直接隐藏 |

### 层次 Depth（5）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Layered Shadow | 多层阴影 | 几层很淡的阴影叠在一起，浮起来但不发脏 |
| Scrim | 遮罩层 | 弹窗背后盖一层半透明深色遮罩，压暗页面让视线聚焦 |
| Edge Fade | 边缘渐隐 | 用渐隐遮罩柔化滚动边缘，既不截断文字又提示可滑动 |
| Sticky Header | 吸顶层级 | 列表滚动时顶栏固定在顶部，用细边和轻投影压住内容 |
| Floating Bar | 悬浮操作栏 | 多选时在底部浮起操作胶囊，就近批处理又不挤占顶栏 |

### 动效 Motion（9）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Easing | 缓动曲线 | 动画速度怎么变化，进场要快起步、慢收尾 |
| Directional Motion | 方向过渡 | 进子页从右滑入、返回向右滑出，让页面层级一目了然 |
| Spring | 弹簧动效 | 按物理规律运动，落点带一点回弹，更有生气 |
| Stagger | 错峰出场 | 列表每项依次错开几十毫秒出场，更有呼吸节奏 |
| Press State | 按压反馈 | 按下去的瞬间给出反应，让人知道点到了 |
| Shared Element | 共享元素过渡 | 同一个元素从上一页变到下一页，视线不会断 |
| Origin-Aware Motion | 原点缩放 | 浮层从触发按钮的角落展开，别从屏幕正中硬弹 |
| Hover Reveal | 悬停显现 | 列表操作按钮平时隐藏，悬停到当前行再轻柔浮现 |
| Loading Button | 加载态按钮 | 提交加载时锁死按钮宽度并原地切加载环，不顶歪旁边按钮 |

### 布局与组件 Layout & UI（16）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Button Hierarchy | 按钮主次 | 一个区域只有一个主按钮，次要操作退成描边或文字链接 |
| Touch Target | 点击热区 | 保持图标纤细，但把周围的可点击区域扩大到至少 40px |
| Empty State | 空状态 | 还没有数据时的页面，说清这是什么、怎么开始 |
| Inline Validation | 即时校验 | 报错直接出现在对应输入框下面，不用回头找 |
| Skeleton | 骨架屏 | 加载时先按内容的形状显示灰色占位 |
| Popover vs. Tooltip | 浮层与提示 | 提示只放一句说明，能点的东西放进浮层 |
| Modal vs. Drawer | 弹窗与抽屉 | 弹窗会打断一切，抽屉从侧边滑出，页面还看得见 |
| Tabs vs. Segmented | 标签页与分段器 | 标签页切换不同页面，分段器切换同一份数据的视图 |
| Switch vs. Checkbox | 开关与复选框 | 开关立刻生效，复选框要等提交才生效 |
| Command Palette | 命令面板 | 按 ⌘K 打开，可以搜索所有操作的列表 |
| Bento Grid | 便当盒布局 | 大小不一的方块网格，越重要的格子越大 |
| Progressive Disclosure | 渐进式披露 | 首屏只留常用项，把低频高级选项收进折叠入口 |
| Combobox | 可搜下拉框 | 把搜索框放进下拉菜单顶部，选项再多也能打字秒找 |
| Input Affix | 输入框前后缀 | 在输入框内固定协议或单位前后缀，只填核心内容不猜格式 |
| Split Button | 组合按钮 | 保留常用次级操作，把多余的同组变体收进主按钮下拉 |
| Breadcrumb | 面包屑导航 | 用轻量的层级路径标清当前位置，深层页面能一键退回上级 |

### AI 界面 AI Patterns（11）

| 词条 | 中文名 | 一句话释义 |
|---|---|---|
| Prompt Composer | AI 输入框 | 多行输入，附件、模型选择和发送按钮都在框里 |
| Streaming Text | 流式输出 | 边生成边显示回答，而不是等全部写完 |
| Thinking Disclosure | 折叠思考过程 | 把推理过程折成一行「思考了 4 秒」，想看再展开 |
| Citation Pill | 引用标注 | 正文里的小编号，把每句话和来源连起来 |
| Slash Command | 斜杠指令 | 在编辑器里输入 /，就地弹出操作菜单 |
| Diff View | 行内对比 | 把 AI 的修改标在原文里：删掉的划红线，新加的标绿 |
| Undo Toast | 可撤销提示 | 直接执行操作，再给一个撤销，而不是先问「确定吗」 |
| Suggested Prompts | 推荐提问 | 空白对话先给几个现成提问，不用对着输入框发呆 |
| Tool Call Steps | 工具调用步骤 | 把 Agent 正在做的事列成几步，每步带状态 |
| Context Chips | 上下文标签 | 把引用的文件收成输入框上方的可删胶囊，不挤占指令正文 |
| Approval Gate | 人工确认节点 | 高危操作前弹出结构化确认卡，由人点确认再让 AI 执行 |

## Skeleton 词条深读（与条目 16 对照）

词条页本体：https://topinspo.design/vocabulary?term=skeleton

- 定义（英文原文）：Gray placeholders in the shape of the content while it loads.（加载时先按内容的形状显示灰色占位）——与条目 16 的结论完全一致
- 演示对照：同一个帖子卡片，两种做法一键切换——「转圈：空卡片里转圈」vs「骨架屏：按最终布局占位（头像、名字、两行正文）」，与条目 16 演示的「骨架 / 转圈并排对比」是同一个口径
- 「Say to AI」提示词（中文版原文）：「内容加载时按最终布局显示灰色占位（头像、名字、两行正文），不要在空卡片里转圈，加载完原位替换」——与条目 16 的 1:1 占位、不跳位口径一致，无新增数值
- 真正的新增信息是它「易混淆对照」里的两条边界判语，条目 16 原先没写明：
  1. 骨架屏 ≠ 空状态：骨架屏表示「正在加载」，空状态表示「这里本来就没有」（Skeleton means "loading"; empty state means "nothing here yet."）
  2. 骨架屏 ≠ 流式输出：流式是真内容正在到达，骨架是先把形状摆出来（Streaming shows real content arriving; a skeleton shows its shape first.）
- 处置：两条判语已补记进条目 16（见该条「Topinspo 词条对照」节）；定义、数值、演示口径均无变化，不重复堆料

## 缺口清单（70 词条 × TAXONOMY 现有 147 子项对照）

只列清单，不新建条目，等用户点名。

### A. 分类里完全没有的格子（真缺口）

| # | 词条 | 缺什么 | 建议归段 |
|---|---|---|---|
| A1 | Proximity 亲密性 | 「距离即分组」的格式塔原则无格；审美七条草稿里有「组内紧组间松」，但未进分类正本 | 第 2 段（间距栅格旁立原则项） |
| A2 | Whitespace 留白 | 只有间距刻度，没有留白纪律（留多少、留给谁） | 第 2 段 |
| A3 | Divider vs. Space 分隔手法 | 「先留白、后发丝线、再色块」的分隔选型无格 | 第 2 段（与 A2 相邻） |
| A4 | Text Balance 标题平衡断行 | 排版格里没有均衡断行（text-wrap: balance 一类） | 第 2 段 字体排版 |
| A5 | Baseline Alignment 基线对齐 | 数字与单位、图标与文字的基线对齐无格 | 第 2 段 字体排版（第 8 段引用） |
| A6 | Nested Cards 卡片套娃 | 嵌套容器每深一层的处理（去边、降影、换底色）无格 | 第 6 段 容器类 |
| A7 | Optical Alignment 视觉对齐 | 图标视觉重心修正（播放三角右移等）无格；刚装的 better-ui 技能里有此条 | 第 8 段 图标风格 |
| A8 | Edge Fade 边缘渐隐 | 滚动行为里有吸顶/回弹/进度，独缺边缘渐隐提示可滚 | 第 7 段 滚动行为 |
| A9 | Stagger 错峰出场 | 列表逐项延迟入场无格 | 第 7 段（转场与微交互之间） |
| A10 | Shared Element 共享元素过渡 | 转场只有页面/面板级，没有元素级接续转场 | 第 7 段 转场 |
| A11 | Bento Grid 便当盒布局 | 首页/工作台的格子布局模式无格 | 第 4 段 主界面/工作台 |
| A12 | Progressive Disclosure 渐进式披露 | 「常用先行、低频收起」的组织模式无独立格，多处界面都在用却没名分 | 第 4 段（界面组织模式；亦可升横切层） |
| A13 | Combobox 可搜下拉框 | 选择类只有普通下拉，缺可输入搜索的组合框 | 第 6 段 选择类 |
| A14 | Split Button 组合按钮 | 动作类有按钮组，缺主按钮带下拉的分裂按钮 | 第 6 段 动作类 |
| A15 | Prompt Composer AI 输入框 | 聊天界面只有一个大格，输入台（多行/附件/模型/发送钮状态）没拆 | 第 4 段 聊天界面（AI 组） |
| A16 | Tool Call Steps 工具调用步骤 | Agent 执行过程的步骤条呈现，全库空白 | 第 4 段（AI 组） |
| A17 | Context Chips 上下文标签 | 输入框上方已选上下文胶囊，无格（与 A15 一组） | 第 4 段（AI 组） |
| A18 | Thinking Disclosure 折叠思考过程 | 第 7 段有「思考状态」，但思考过程折叠/展开的呈现没细化 | 第 4 段（AI 组）或第 7 段 流式与进行时 |
| A19 | Citation Pill 引用标注 | 内容呈现里没有行内引用标记 | 第 4 段 内容呈现 |
| A20 | Slash Command 斜杠指令 | 命令面板在第 5 段搜索格里，输入框内「/」就地菜单无格 | 第 4 段 聊天/编辑器输入 |
| A21 | Diff View 行内对比 | 编辑器界面没有差异视图（AI 改稿红绿标） | 第 4 段 画布与编辑器界面 |
| A22 | Suggested Prompts 推荐提问 | 空态对话的推荐问句 chips 无格 | 第 4 段 聊天界面 |

### B. 有格子、但没细化到词条这一步（细化缺口）

| # | 词条 | 现状 | 建议 |
|---|---|---|---|
| B1 | Concentric Radius 同心圆角 | 第 2 段有「圆角刻度」，未写同心规则（内圆角＝外圆角－间距）；better-ui 技能已含此值 | 第 2 段 圆角刻度补一行规则 |
| B2 | Tint & Shade 同色明暗阶 | 第 2 段色彩有主色/状态色，未定「同色派生浅底深字」的色阶生成法 | 第 2 段 色彩补派生规则 |
| B3 | Middle Truncation 中间截断 | 第 2 段有「截断规则」，未分尾部截断与中间截断（文件名/哈希/路径） | 第 2 段 截断规则补分型 |
| B4 | Shortcut Hint 快捷键徽标 | 第 7 段有快捷键清单（行为），键帽的视觉样式（等宽、底托）无格 | 第 2 段 排版定样式，第 6 段 菜单落地 |
| B5 | Icon Container 图标容器 | 第 8 段图标风格未含统一底托；条目 33/34 的演示其实已经在用图标方片 | 第 8 段补图标容器规格 |
| B6 | Directional Motion 方向过渡 | 第 7 段转场未立「方向即层级语义」的纪律 | 第 7 段 转场补方向口径 |
| B7 | Origin-Aware Motion 原点缩放 | 第 7 段有「菜单缩放弹出」沾边，未成原则；审美七条有「从触发点长出」 | 第 7 段 微交互补原则 |
| B8 | 组件选型对照组：Popover vs. Tooltip / Modal vs. Drawer / Tabs vs. Segmented / Switch vs. Checkbox | 四组组件本身在第 3/6 段都有格，缺的是「何时用哪个」的选型判语（本站每组只一句话：如开关立刻生效、复选框等提交） | 第 6 段各组件旁加对照注，或在第 10 段集中立「组件选型对照」一组 |
| B9 | Undo Toast 可撤销提示 | 第 9 段有删除与撤销、条目 33 有 Toast，但「先执行、后给撤销」这个模式没被点名 | 第 9 段 删除与撤销补模式名与时限口径 |
| B10 | Spring 弹簧动效 | 条目 29/33 有个案参数，未升为第 2 段动效 Tokens 的命名曲线 | 第 2 段 动效 Tokens 补弹簧口径 |

### C. 已覆盖（对上账，不用动）

Padding / Gap / Line Height / Hierarchy / Font Weight / Tracking / Tabular Numbers（第 2 段格子齐全，其中字号层级等数值仍在条目 12 的地基缺口清单里）/ Accent / Contrast / Muted Text / Semantic Color（第 2 段色彩与文字层级）/ Disabled State（第 6 段六态）/ Border Radius / Hairline Border（条目 12 已有发丝线数值）/ Avatar Stack（第 5 段头像组叠放）/ Badge Counter（第 5 段角标纪律）/ Layered Shadow / Scrim（第 2 段阴影与遮罩）/ Sticky Header（第 7 段吸顶）/ Floating Bar（条目 2 悬浮胶囊顶栏）/ Easing（第 2 段动效 Tokens）/ Press State（六态按下）/ Hover Reveal（第 7 段悬停浮现操作）/ Loading Button（条目 32）/ Button Hierarchy / Touch Target（第 2 段 ≥44pt 口径；本站写 40px，差 4px，不改自家口径）/ Empty State（条目 17）/ Inline Validation（第 6 段表单校验）/ Skeleton（条目 16）/ Command Palette（条目 30）/ Breadcrumb（第 3 段）/ Streaming Text（条目 13）/ Approval Gate（条目 5 批准卡——本站的「人工确认节点」就是咱们的批准卡，已落地）

## 最值得先补的前 3 个（个人排序，等用户点名）

1. **A16 工具调用步骤 Tool Call Steps**——Pack 就是 agent 产品，「Agent 正在做什么、每步什么状态」是核心呈现，全库空白，且 Muse/Pack 每次画 agent 界面都要用
2. **A15 AI 输入框 Prompt Composer（连带 A17 上下文标签）**——聊天类产品的主战场，第 4 段至今只有「聊天界面」一个大格，输入台没拆过
3. **A12 渐进式披露 Progressive Disclosure**——设置页、详情页、首页都在用这个模式安排信息，分类里没名分，每个界面都得重新发明「低频选项藏哪」
