# 完整案例：Open Bot Avatar（动态 agent 头像）

- 段位：第 10 段 完整案例与模式（兼第 8 段 头像）
- 状态：已采纳（adopted，案例收录）
- 一句话结论：一个 agent 头像只需要「一条轮廓线＋眼睛位置」——剩下的立体感、表情和状态动画全交给渲染器，头像从此是活的、能报状态的。
- 效果图：[assets/open-bot-avatar.png](../assets/open-bot-avatar.png)（官方横幅：上排扁平、下排毛茸茸的物件头像）
- 拆解数值（出自其公开规范与 README，2026-11-24 实查）：
  - 定义格式：一段 JSON——body 是一条 0 0 100 100 画布内的 SVG path；eyes 只给四个数：x、y（眼睛中心）、spacing（眼距）、scale（大小）
  - 立体原理：渲染器把轮廓按横截面堆叠推断体积，逐帧投到 canvas 绘制；depth 体积深度 0（全平）–14，默认 6
  - 状态机：state 六档——idle / thinking / working / waiting / blocked / done；mood 两档——neutral / happy，只改眼睛形状，可与任何 state 叠加
  - 视线：followPointer 眼睛跟随鼠标/手指；lookAt 固定方向（-1..1）优先级更高；holdGaze 保持当前视线
  - 材质：flat 扁平 / fluffy 毛茸茸两选；still 可冻结成静态图；reducedMotion 跟随系统减动效
  - 产出：活头像挂 DOM（mountAvatar）；静态走 renderAvatarSvg 输出 SVG 字符串，不需要 DOM
  - 生成流程：编辑器里写一句描述 → 把官方 system prompt 交给任意大模型/agent 吐 JSON → 粘回 Import 即成头像；仓库自带 generate-avatar skill
  - 工程：渲染包零依赖、MIT 开源；validateAvatar 校验外来定义（ok/errors）
- 来源：2026-11-24 用户分享三件套（仓库 github.com/DominikScholz/open-bot-avatar、在线编辑器、开发文档），Muse 实查 README 与规范后收录；仓库 2026-11-02 建、约 800 星
- 适用项目：Pack 等多 agent 产品的成员头像（状态一眼可见：谁在思考、谁卡住了）；任何需要「会报状态的头像」的 agent 界面；自研头像系统时先按此规范对齐再动手
