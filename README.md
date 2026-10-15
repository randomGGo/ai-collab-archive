# AI 协作档案工具（体验版）

> 填一份问卷，生成两条指令；粘贴给你常用的 AI，让它为你建立并长期维护一套跨会话、跨工具的协作档案。

**在线体验**：<https://randomGGo.github.io/ai-collab-archive/> ｜ **离线使用**：下载本仓库的 `index.html`，双击用浏览器打开即可（无需安装、不联网）。

---

## 一、它解决什么问题

每次换一个 AI、换一个会话、隔几天再回来，都要重新讲一遍"我是谁、在做什么、上次做到哪、有哪些决定"。信息一遍遍重讲，AI 的产出也一遍遍飘。

本工具把这件事固定下来：

1. 你用几分钟填写一份问卷（愿意填多少填多少，不设必填）；
2. 工具生成**两条指令**：第一条用于建立档案，第二条在第一条执行后交给**同一个** AI 做复查与修复；
3. 你把它们依次粘贴给你常用的任意 AI（对话式 AI、IDE 内的编码助手都可以）；
4. AI 按指令在你电脑上创建一套**多文件协作档案**（不是一个长文档）；
5. 此后换 AI、换会话、换工具，新 AI 读取同一套档案即可接续，不必再写交接说明。

## 二、30 秒上手

1. 打开在线体验地址，或下载 `index.html` 双击打开；
2. 按问卷选择 / 填写信息（全部可选，跳过不影响生成）；
3. 点「生成并复制给 AI」，得到两条指令；
4. 把**第一条**发给你常用的 AI，等它完成建档；
5. 再把**第二条**发给**同一个** AI，让它复查并修复。

## 三、它会生成什么样的档案

```text
AI协作档案/
├─ README.md
├─ 00-入口/
│  ├─ 00-开始这里.md
│  ├─ 01-AI快速上下文.md
│  └─ 02-任务索引.md
├─ 01-个人档案/
│  ├─ 00-个人档案入口.md
│  ├─ 01-个人背景.md
│  └─ 02-AI协作偏好.md
├─ 02-任务档案/
│  └─ <一个任务一个独立目录>/
│     ├─ 00-任务入口.md
│     ├─ 01-任务背景与目标.md
│     ├─ 02-当前状态.md
│     ├─ 03-已确认决定.md
│     └─ 04-执行记录.md
└─ 03-通用规则/
   ├─ 00-通用规则入口.md
   ├─ 01-AI执行与交付规则.md
   └─ 02-档案维护规则.md
```

设计原则：个人长期信息 / 通用规则 / 当前任务状态 / 历史记录分开存放；一个任务一套独立档案，不混写；同一事实只维护一个权威位置；不确定的信息一律标记【待确认】，不允许 AI 编造补全。

## 四、本仓库与付费版本的关系

| | 本仓库（体验版） | 付费版本 |
|---|---|---|
| 获取方式 | 免费开源（MIT） | 单独购买 |
| 问卷范围 | 基础问卷 + 一个真实任务 | 完整问卷 + 更多信息类别 |
| 维护入口 | 无 | 含「继续已有任务」「更新任务进度」 |
| 适用场景 | 先跑通一遍完整流程 | 日常长期使用 / 多任务管理 |

体验版与付费版本共用同一套档案结构与安全底线，**体验版足以把完整流程跑通一遍**。

## 五、隐私

- 单文件、纯本地运行（`file://` 直接打开即可）；
- **不发起任何网络请求**，不接入统计或追踪；
- 不收集、不上传任何填写内容；
- 内置本地敏感信息提醒（如密码、验证码、证件号、银行卡号）。提醒不等于全量识别，发送前请自行确认；
- 把内容粘贴给外部 AI 后，由你所选的 AI 工具处理，请留意其隐私政策。

## 六、目录结构

```text
.
├─ index.html   # 体验版（单文件，可直接打开；也是在线体验版入口）
├─ README.md
└─ LICENSE
```

## 七、许可

MIT License © 2026 randomGGo

## 八、反馈

欢迎通过 Issues 提出问题或建议（不承诺响应时效）。

---

# AI Collaboration Archive Tool (Trial)

> Fill in one questionnaire, get two prompts, paste them into any AI you already use — and let it build and maintain a cross-session, cross-tool collaboration archive for you.

**Live demo**: <https://randomGGo.github.io/ai-collab-archive/> ｜ **Offline**: download `index.html` and open it in your browser (no install, no network required).

## 1. What problem does it solve

Every time you switch to a new AI, start a new session, or come back after a few days, you have to explain all over again who you are, what you are working on, where you left off, and which decisions were made. The context is re-told again and again, and the output drifts with it.

This tool fixes that:

1. You spend a few minutes filling in a questionnaire (answer as much or as little as you like — nothing is required);
2. The tool generates **two prompts**: the first builds the archive; the second is handed to the **same** AI afterwards to review and repair the result;
3. You paste them, in order, into any AI you already use (chat AI, or a coding assistant inside your IDE);
4. The AI creates a **multi-file collaboration archive** on your computer (not one long document);
5. From then on, a new AI can pick up where you left off by reading the same archive — no handover document needed.

## 2. Quick start (30 seconds)

1. Open the live demo, or download `index.html` and open it in your browser;
2. Fill in the questionnaire (everything is optional; skipping does not block generation);
3. Click “Generate and copy to AI” to get the two prompts;
4. Send the **first** prompt to your usual AI and let it build the archive;
5. Send the **second** prompt to the **same** AI to review and repair.

## 3. What the generated archive looks like

The AI creates a small archive library with separated concerns: personal profile, general rules, current task status, and execution history. One task gets one independent folder. Facts that cannot be verified must be marked `[待确认] / [To be confirmed]` — the AI is not allowed to invent them.

## 4. This repo vs. the paid editions

| | This repo (Trial) | Paid editions |
|---|---|---|
| How to get it | Free and open source (MIT) | Purchased separately |
| Questionnaire | Basic + one real task | Full questionnaire + more categories |
| Maintenance entries | — | “Continue an existing task”, “Update task progress” |
| Best for | Running the whole flow once | Daily long-term use / multi-task management |

The trial and the paid editions share the same archive structure and safety rules. The trial is enough to run the complete flow end to end.

## 5. Privacy

- Single file, runs entirely locally (open it directly via `file://`);
- **No network requests at all** — no analytics, no tracking;
- Does not collect or upload anything you type;
- Includes a local sensitive-information reminder (passwords, verification codes, ID numbers, bank cards). A reminder is not full detection — please double-check before sending;
- Once you paste content into an external AI, it is handled by that AI tool; check its privacy policy.

## 6. License

MIT License © 2026 randomGGo

## 7. Feedback

Issues and suggestions are welcome (no response-time commitment).
