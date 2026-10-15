# AI 协作档案工具（体验版） / AI Collaboration Archive Tool (Trial)

> 填一份问卷，生成两条指令；粘贴给你常用的 AI，让它为你建立并长期维护一套**跨会话、跨工具**的协作档案。
> Fill in one questionnaire, get two prompts, paste them into any AI you already use, and let it build and maintain a **cross-session, cross-tool** collaboration archive for you.

**在线体验 Live demo**：
[中文版 Chinese](https://randomggo.github.io/ai-collab-archive/zh/) ｜
[English](https://randomggo.github.io/ai-collab-archive/en/) ｜
[语言选择 Choose language](https://randomggo.github.io/ai-collab-archive/)

**离线使用 Offline**：下载 `zh/index.html` 或 `en/index.html`，双击用浏览器打开即可（无需安装、不联网）。
Download `zh/index.html` or `en/index.html` and open it in your browser — no install, no network.

**许可 License**：[PolyForm Noncommercial License 1.0.0](#许可-license) —— 个人与非商业用途免费；**商业用途需另行授权**。

---

# 中文

## 一、它解决什么问题

每次换一个 AI、换一个会话、隔几天再回来，都要重新讲一遍"我是谁、在做什么、上次做到哪、有哪些决定"。信息一遍遍重讲，AI 的产出也一遍遍飘。

本工具把这件事固定下来：

1. 你用几分钟填写一份问卷（愿意填多少填多少，不设必填）；
2. 工具生成**两条指令**：第一条用于建立档案，第二条在第一条执行后交给**同一个** AI 做复查与修复；
3. 你把它们依次粘贴给你常用的任意 AI（对话式 AI、IDE 内的编码助手都可以）；
4. AI 按指令在你电脑上创建一套**多文件协作档案**（不是一个长文档）；
5. 此后换 AI、换会话、换工具，新 AI 读取同一套档案即可接续，不必再写交接说明。

## 二、30 秒上手

1. 打开在线体验地址，或下载 `zh/index.html` 双击打开；
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

**英文版生成的是英文档案结构**（目录与文件名全部为英文）：

```text
AI-Collab-Archive/
├─ README.md
├─ 00-entry/
│  ├─ 00-start-here.md
│  ├─ 01-ai-quick-context.md
│  └─ 02-task-index.md
├─ 01-profile/
│  ├─ 00-profile-entry.md
│  ├─ 01-background.md
│  └─ 02-ai-collaboration-preferences.md
├─ 02-tasks/
│  └─ (one folder per task)/
│     ├─ 00-task-entry.md
│     ├─ 01-task-background-and-goals.md
│     ├─ 02-current-status.md
│     ├─ 03-confirmed-decisions.md
│     └─ 04-execution-log.md
└─ 03-general-rules/
   ├─ 00-rules-entry.md
   ├─ 01-ai-execution-and-delivery-rules.md
   └─ 02-archive-maintenance-rules.md
```

## 四、本仓库结构

```text
ai-collab-archive/
├─ index.html      # 语言选择页（GitHub Pages 入口）
├─ zh/
│  └─ index.html   # 中文版体验页（单文件，可离线双击打开）
├─ en/
│  └─ index.html   # 英文版体验页（单文件，可离线双击打开）
├─ README.md
└─ LICENSE         # PolyForm Noncommercial License 1.0.0
```

两个版本各自是**一个自包含的 HTML 文件**：样式、脚本、指令模板全部内嵌，没有构建步骤、没有依赖、不加载任何外部资源。

## 五、本仓库与付费版本的关系

| | 本仓库（体验版） | 付费版本 |
|---|---|---|
| 获取方式 | 免费（非商业许可） | 单独购买 |
| 问卷范围 | 基础问卷 + 一个真实任务 | 完整问卷 + 更多信息类别 |
| 维护入口 | 无 | 含「继续已有任务」「更新任务进度」 |
| 适用场景 | 先跑通一遍完整流程 | 日常长期使用 / 多任务管理 |

体验版与付费版本共用同一套档案结构与安全底线，**体验版足以把完整流程跑通一遍**。

## 六、隐私

- 单文件、纯本地运行（`file://` 直接打开即可）；
- **不发起任何网络请求**，不接入统计或追踪；
- 不收集、不上传任何填写内容；
- 内置本地敏感信息提醒（如密码、验证码、证件号、银行卡号）。提醒不等于全量识别，发送前请自行确认；
- 把内容粘贴给外部 AI 后，由你所选的 AI 工具处理，请留意其隐私政策。

## 七、许可 License

**PolyForm Noncommercial License 1.0.0**（全文见 [LICENSE](LICENSE)）

| | 说明 |
|---|---|
| ✅ 允许 | 个人使用、学习研究、业余爱好项目；慈善组织、教育机构、公共研究机构、公共安全/卫生机构、环保组织与政府机构使用；修改、再分发（须保留许可条款） |
| ❌ 不允许 | 任何商业用途，包括出售本工具、收费提供访问、打包进收费产品等 |
| 💬 商业授权 | 如需商业使用，请通过 [Issues](https://github.com/randomGGo/ai-collab-archive/issues) 联系作者 |

> 本仓库于 2026-10-15 由 MIT 变更为 PolyForm Noncommercial 1.0.0（体验版首版发布次日）。变更前已获取副本者，其 MIT 授权不受影响。完整条款以英文原文为准。

## 八、反馈

欢迎通过 [Issues](https://github.com/randomGGo/ai-collab-archive/issues) 提出问题或建议（不承诺响应时效）。

---

# English

> Fill in one questionnaire, get two prompts, paste them into any AI you already use — and let it build and maintain a **cross-session, cross-tool** collaboration archive for you.

**Live demo**: [English](https://randomggo.github.io/ai-collab-archive/en/) ｜
[Chinese](https://randomggo.github.io/ai-collab-archive/zh/) ｜
[Choose language](https://randomggo.github.io/ai-collab-archive/)

**Offline**: download `en/index.html` and open it in your browser — no install, no network required.

**License**: [PolyForm Noncommercial License 1.0.0](#license) — free for personal and noncommercial use; **commercial use requires a separate licence**.

## 1. What problem does it solve

Every time you switch to a new AI, start a new session, or come back after a few days, you have to explain all over again who you are, what you are working on, where you left off, and which decisions were made. The context is re-told again and again, and the output drifts with it.

This tool fixes that:

1. You spend a few minutes filling in a questionnaire (answer as much or as little as you like — nothing is required);
2. The tool generates **two prompts**: the first builds the archive; the second is handed to the **same** AI afterwards to review and repair the result;
3. You paste them, in order, into any AI you already use (chat AI, or a coding assistant inside your IDE);
4. The AI creates a **multi-file collaboration archive** on your computer (not one long document);
5. From then on, a new AI can pick up where you left off by reading the same archive — no handover document needed.

## 2. Quick start (30 seconds)

1. Open the live demo, or download `en/index.html` and open it in your browser;
2. Fill in the questionnaire (everything is optional; skipping does not block generation);
3. Click "Generate and copy to AI" to get the two prompts;
4. Send the **first** prompt to your usual AI and let it build the archive;
5. Send the **second** prompt to the **same** AI to review and repair.

## 3. What the generated archive looks like

The English edition produces an **English archive structure** — folder and file names included:

```text
AI-Collab-Archive/
├─ README.md
├─ 00-entry/
│  ├─ 00-start-here.md
│  ├─ 01-ai-quick-context.md
│  └─ 02-task-index.md
├─ 01-profile/
│  ├─ 00-profile-entry.md
│  ├─ 01-background.md
│  └─ 02-ai-collaboration-preferences.md
├─ 02-tasks/
│  └─ (one folder per task)/
│     ├─ 00-task-entry.md
│     ├─ 01-task-background-and-goals.md
│     ├─ 02-current-status.md
│     ├─ 03-confirmed-decisions.md
│     └─ 04-execution-log.md
└─ 03-general-rules/
   ├─ 00-rules-entry.md
   ├─ 01-ai-execution-and-delivery-rules.md
   └─ 02-archive-maintenance-rules.md
```

Design principles: personal long-term information, general rules, current task status and history are stored separately; one task gets one independent folder; every fact has exactly one authoritative location; anything uncertain must be marked `[To be confirmed]` — the AI is not allowed to invent it. The archive is plain Markdown with relative links, so it is not tied to any AI vendor.

(The Chinese edition generates the same structure with Chinese folder and file names.)

## 4. Repository structure

```text
ai-collab-archive/
├─ index.html      # Language selector (GitHub Pages entry point)
├─ zh/
│  └─ index.html   # Chinese edition — single file, works offline
├─ en/
│  └─ index.html   # English edition — single file, works offline
├─ README.md
└─ LICENSE         # PolyForm Noncommercial License 1.0.0
```

Each edition is **one self-contained HTML file**: styles, scripts and the instruction templates are all inlined. There is no build step, no dependency, and no external resource is loaded.

## 5. This repo vs. the paid editions

| | This repo (Trial) | Paid editions |
|---|---|---|
| How to get it | Free (noncommercial licence) | Purchased separately |
| Questionnaire | Basic + one real task | Full questionnaire + more categories |
| Maintenance entries | — | "Continue an existing task", "Update task progress" |
| Best for | Running the whole flow once | Daily long-term use / multi-task management |

The trial and the paid editions share the same archive structure and safety rules. The trial is enough to run the complete flow end to end.

## 6. Privacy

- Single file, runs entirely locally (open it directly via `file://`);
- **No network requests at all** — no analytics, no tracking;
- Does not collect or upload anything you type;
- Includes a local sensitive-information reminder (passwords, verification codes, ID numbers, bank cards). A reminder is not full detection — please double-check before sending;
- Once you paste content into an external AI, it is handled by that AI tool; check its privacy policy.

## 7. License

**PolyForm Noncommercial License 1.0.0** (full text in [LICENSE](LICENSE))

| | |
|---|---|
| ✅ Permitted | Personal use, study and research, hobby projects; use by charities, educational institutions, public research organisations, public safety or health organisations, environmental protection organisations and government institutions; changes and redistribution (with the licence terms kept) |
| ❌ Not permitted | Any commercial use — selling the tool, charging for access, bundling it into a paid product, and so on |
| 💬 Commercial licence | For commercial use, please contact the author through [Issues](https://github.com/randomGGo/ai-collab-archive/issues) |

> This repository changed from MIT to PolyForm Noncommercial 1.0.0 on 2026-10-15, one day after the initial trial release. Anyone who obtained a copy before that change keeps their MIT rights. The English licence text is authoritative.

## 8. Feedback

Issues and suggestions are welcome (no response-time commitment).
