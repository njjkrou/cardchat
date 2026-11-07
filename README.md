<div align="center">

# 🌸 藏春阁 CardChat

**AI 角色扮演聊天平台 · 兼容整个酒馆生态**

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md)

在线体验 → **https://ccg.officechat.com.cn**

</div>

---

<p align="center">
  <img src="docs/images/chat.jpg" alt="聊天界面" width="49%">
  <img src="docs/images/discover.jpg" alt="发现页" width="49%">
</p>

藏春阁是一套完整的 AI 角色聊天平台：角色卡、世界书、预设、长期记忆、群聊、图片生成、订阅计费、管理后台，
开箱即用。它不止能聊天——它把「酒馆」那套生态完整搬到了网页上，而且做得更省心。

---

## 一、全面兼容酒馆生态

支持 **SillyTavern 角色卡（v1 / v2）**、**Chub.ai**、**JanitorAI** 格式，PNG 卡和 JSON 卡都能直接导入。
导入后角色的人设、开场白、示例对话、内嵌世界书全部保留。

<p align="center">
  <img src="docs/images/characters.jpg" alt="角色卡管理" width="72%">
</p>

**角色卡可直接读取、直接编辑。** 不用转格式，不用重新录入——点开就能改人设、改开场白、换头像、调标签。

<p align="center">
  <img src="docs/images/character.jpg" alt="角色卡详情" width="72%">
</p>

## 二、一键生成角色卡

不想写人设？用一句话描述你想要的角色，AI 自动填好名称、简介、性格、开场白和标签，
选个风格（恋爱 / 奇幻 / 校园 / 职场 / 悬疑 / 治愈…）就能生成，生成完还能继续改。

<p align="center">
  <img src="docs/images/create.jpg" alt="一键生成角色卡" width="72%">
</p>

## 三、单聊与群聊

**单聊**：流式回复、多分支（Swipe）、重新生成、编辑重发、引用回复、消息导出。

<p align="center">
  <img src="docs/images/chat.jpg" alt="单聊" width="72%">
</p>

**群聊**：一张对话里可以放多个角色，用 `@` 指定谁来说话，被点到的角色单独回复。
角色之间也会互相接话，群像感是单聊给不了的。

<p align="center">
  <img src="docs/images/chat-group.jpg" alt="群聊" width="72%">
</p>

## 四、图片上传与联网搜索

- 支持发送图片，多模态模型可以看图说话
- 支持联网搜索，需要实时信息时把搜索结果并入上下文
- 图片 / 视频生成已接入

## 五、一键导入破限文件

以前破限要手动拼 prompt、调各种参数，还容易被模型识破。
现在直接把酒馆的破限预设（JSON）导入即可，系统会按条目拆开、按开关生效，还能给不同对话绑不同预设。

<p align="center">
  <img src="docs/images/presets.jpg" alt="预设与破限" width="72%">
</p>

预设里还能直接调 **Temperature、Top P、Top K、Min P、Frequency Penalty、Presence Penalty、Repetition Penalty** 等生成参数——
**模型参数完全自由设置**，不用改代码。

## 六、世界书

三层世界书：全局、角色内嵌、对话内临时。支持导入 SillyTavern 世界书、手动编辑条目、关键词触发注入。
写设定、补背景、控世界观，都靠它。

<p align="center">
  <img src="docs/images/worldbook.jpg" alt="世界书" width="72%">
</p>

## 七、用户人设与个人设置

每个人都可以有自己的人设：头像、昵称、性格、简介。聊天时随时切换，
角色会用你设定的人设和你对话，而不是干巴巴的「用户」。

<p align="center">
  <img src="docs/images/profile.jpg" alt="个人中心" width="49%">
  <img src="docs/images/settings.jpg" alt="设置" width="49%">
</p>

设置页里还能选**平台 API**（按官方价扣爱心）或者填**自己的 API Key**（不扣爱心），
地址、模型都可以自己指定。

## 八、奖励体系

- **每日签到**：每天一次，固定爱心
- **创作奖励**：发布角色卡得爱心，被赞、被下载还有额外奖励
- **邀请注册**：邀请码注册，双方都有奖励
- **首充特惠 / 订阅方案**：充值和会员两条路径

<p align="center">
  <img src="docs/images/subscription.jpg" alt="订阅与充值" width="72%">
</p>

---

## 更多功能

| 功能 | 说明 |
|---|---|
| 发现与推荐 | 选标签（恋爱 / 治愈 / 职场 / 奇幻 / 恐怖…）后进入刷卡流，喜欢或跳过，越用越准 |
| 长期记忆 | 分层压缩 + 事实抽取 + 混合检索，聊几十轮还记得你（见下方技术架构） |
| 定时联系 | 角色可以按间隔主动给你发消息，像真的会想起你 |
| 排行榜 | 创作者榜单，按作品、获赞、被使用量排名 |
| 通知中心 | 点赞、评论、审核结果、系统公告 |
| 正则脚本 | 显示层正则替换，去 AI 味、清洗格式 |
| 聊天导出 | 导出为文本或 JSON |
| 关注创作者 | 关注后能看到作者的新作品 |
| 多语言 | 简体中文、English、日本語、한국어、Français、Español |
| 移动端 | 完整适配，手机浏览器直接用 |

<p align="center">
  <img src="docs/images/discover-prefs.jpg" alt="选择标签" width="24%">
  <img src="docs/images/discover-tags.jpg" alt="已选标签" width="24%">
  <img src="docs/images/leaderboard.jpg" alt="排行榜" width="24%">
  <img src="docs/images/notifications.jpg" alt="通知中心" width="24%">
</p>

<p align="center">
  <img src="docs/images/chat-mobile.jpg" alt="移动端聊天" width="26%">
  <img src="docs/images/discover-mobile.jpg" alt="移动端发现页" width="26%">
  <img src="docs/images/auto.jpg" alt="定时联系" width="26%">
</p>

---

## 管理后台

所有运营动作都在后台完成：审核、封禁、调余额、看订单、改价格、发公告、配模型。

<p align="center">
  <img src="docs/images/admin-dashboard.jpg" alt="仪表盘" width="72%">
</p>

<p align="center">
  <img src="docs/images/admin-users.jpg" alt="用户管理" width="49%">
  <img src="docs/images/admin-characters.jpg" alt="角色卡审核" width="49%">
</p>

<p align="center">
  <img src="docs/images/admin-orders.jpg" alt="订单管理" width="49%">
  <img src="docs/images/admin-ledger.jpg" alt="爱心流水" width="49%">
</p>

<p align="center">
  <img src="docs/images/admin-platform.jpg" alt="平台配置" width="72%">
</p>

<p align="center">
  <img src="docs/images/admin-subscriptions.jpg" alt="订阅方案" width="49%">
  <img src="docs/images/admin-comments.jpg" alt="评论审核" width="49%">
</p>

---

## 技术架构

<p align="center">
  <img src="docs/architecture.svg" alt="系统架构图" width="100%">
</p>

| 层 | 选型 |
|---|---|
| 前端 | Vue 3 · TypeScript · Vite · SSE 流式渲染 |
| 后端 | Node.js（22/24）· Express · TypeScript |
| 数据库 | SQLite（WAL）· FTS5 全文检索 |
| 模型接入 | 任意 OpenAI 兼容网关，流式 / 非流式自动回退 |
| 部署 | Docker Compose · Nginx 反向代理 |

### 长期记忆是怎么做的

角色聊得越久，上下文越贵。系统把「记住什么」拆成三层，在固定 token 预算内尽可能多记：

| 层 | 做什么 | 成本 |
|---|---|---|
| **L1 工作记忆** | 按预算切出最近若干条原文 | 每轮固定 |
| **L2 分段摘要** | 每 30 条或 6000 字生成一段摘要，写完不重算 | 每段一次 |
| **L3 事实卡** | 从摘要抽取身份 / 偏好 / 关系 / 事件，去重合并 | 随 L2 |
| **检索注入** | 按当前输入检索相关往事，命中才注入 | 每轮一次本地查询 |

实测：真实长对话中 **prompt token 降低约 35%**，被挤出窗口的事实仍能被准确召回。

---

## 目录结构

```
.
├── README.md                 # 中文（默认）
├── README.en.md              # English
├── README.ja.md              # 日本語
├── docs/
│   ├── architecture.svg      # 架构图
│   └── images/               # 界面截图
├── web/                      # 前端站点，可直接静态托管
└── LICENSE
```

`web/` 是标准单页应用产物，Nginx 部署时把未知路径回退到 `index.html`
（`try_files $uri /index.html`）。

---

## 许可

**保留所有权利（All Rights Reserved）**。详见 [LICENSE](LICENSE)。

<div align="center">
<sub>Made with 🌸</sub>
</div>
