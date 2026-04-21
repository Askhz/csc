# csc 项目 UI 文案可直接替换清单

- 目的：筛选出**只需要替换展示文案**、即可让 UI 页面显示 `CoStrict` 而不是 `Claude` / `Claude Code` / `Anthropic` 的内容。
- 筛选原则：
  1. 仅保留用户可见文案，例如 `title`、`subtitle`、`message`、`placeholder`、`label`、`aria-label`、`<Text>` 文本。
  2. 不纳入命令、包名、环境变量、URL、路径、主题 token、埋点名、注释说明。
  3. 对账号体系、订阅体系、Desktop/Chrome 集成等文案，标记为“**可替换但需谨慎**”。

---

## 一、高置信：可直接文本替换的 UI 文案

这部分基本都属于纯展示文本，直接替换后主要影响界面显示，不会直接触发命令、配置或协议变更。

| 文件 | 行号 | 原文 | 建议替换为 |
| --- | ---: | --- | --- |
| `packages/remote-control-server/web/index.html` | L6 | `Remote Control — Claude Code` | `Remote Control — CoStrict` |
| `packages/remote-control-server/web/automation.js` | L280 | `Claude Code is in proactive mode and currently sleeping until the next wake-up or user message.` | `CoStrict is in proactive mode and currently sleeping until the next wake-up or user message.` |
| `packages/remote-control-server/web/automation.js` | L290 | `Claude Code is in proactive mode and waiting for the next scheduled check-in.` | `CoStrict is in proactive mode and waiting for the next scheduled check-in.` |
| `packages/remote-control-server/web/automation.js` | L299 / L309 | `Claude Code is in proactive mode and may continue working between user messages.` | `CoStrict is in proactive mode and may continue working between user messages.` |
| `packages/remote-control-server/web/automation.js` | L319 | `Claude Code is processing an automatic background trigger.` | `CoStrict is processing an automatic background trigger.` |
| `packages/remote-control-server/web/automation.js` | L361 | `aria-label="Claude Code status"` | `aria-label="CoStrict status"` |
| `packages/@ant/ink/src/theme/LoadingState.tsx` | L45 | `Fetching your Claude Code sessions...` | `Fetching your CoStrict sessions...` |
| `src/components/FeedbackSurvey/FeedbackSurveyView.tsx` | L26 | `How is Claude doing this session? (optional)` | `How is CoStrict doing this session? (optional)` |
| `src/components/FeedbackSurvey/TranscriptSharePrompt.tsx` | L43 | `Can Anthropic look at your session transcript to help us improve` | `Can CoStrict look at your session transcript to help us improve` |
| `src/components/CostThresholdDialog.tsx` | L12 | `You've spent $5 on the Anthropic API this session.` | `You've spent $5 on the CoStrict API this session.` |
| `src/components/agents/new-agent-creation/wizard-steps/DescriptionStep.tsx` | L47 | `Description (tell Claude when to use this agent)` | `Description (tell CoStrict when to use this agent)` |
| `src/components/agents/new-agent-creation/wizard-steps/DescriptionStep.tsx` | L68 | `When should Claude use this agent?` | `When should CoStrict use this agent?` |
