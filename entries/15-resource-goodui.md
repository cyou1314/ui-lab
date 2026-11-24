# 资源：goodui 组件与页面块库（shadcn/ui）

- 段位：第 6 段 组件库（资源条目）
- 状态：已采纳（adopted，资源收录）
- 一句话结论：缺组件先来这里翻——它卖的不是灵感图，是能直接装进项目的真代码，还能让 AI 通过 MCP 自己装。
- 效果图：[assets/goodui.png](../assets/goodui.png)（其站内一款手机界面效果）
- 拆解（2026-11-24 实查其官网口径）：
  - 体量：网页组件 269 个、应用页面块 150 个；React Native 组件 69 个＋Pro 屏幕 27 个＋完整 App 模板 6 个；10 套设计 kit 共 45 页
  - 免费档（MIT、无需账号）：网页组件 132 个、RN 组件 69 个、免费块 39 个（含资源时间线）、排期引擎（scheduler engine）
  - Pro 买断 $99（早鸟价，会随库涨价）：全部 Pro 组件 137 个（WebGL/3D/物理/编辑器类）、Pro 块 111 个、8 种外观、10 套 kit 源码；Team $249（10 人）；14 天无理由退款
  - AI 接入：自带 MCP 服务（9 个工具）＋ llms.txt ＋ 编辑器 skills，Claude Code/Cursor 等可直接安装真组件；Pro 块走私有 registry＋license key（npx shadcn add @goodui-pro/<block>）
  - 适配：用你自己项目的 shadcn 主题（Base UI 与 Radix 两版均可）、Tailwind v4、React 19；无后端，块内是演示数据，接自己的 API
  - 国际化：19 种语言含 RTL（阿拉伯语/希伯来语），一个 locale 设置标签、日期、数字与布局全跟随
  - 稀缺件：排期引擎与资源时间线（甘特式资源排布）是免费的——这类块市面上少见且难自研
- 来源：2026-11-24 用户分享 goodui.dev，Muse 实查官网后按资源条目收录（非案例拆解）
- 适用项目：任何 shadcn/ui＋Tailwind 的 Web 项目缺组件/页面块时先来此查；Pack 等产品若上 Web 端，排期、日历、预约类界面优先评估它的现成块；AI-USAGE 调用时注意：它是有版权的商业库，免费档 MIT 可直接用，Pro 需先买断再装
