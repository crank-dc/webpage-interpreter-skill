---
name: webpage-interpreter
description: Read and explain webpages in simple Chinese for users who are not comfortable reading English. Use when the user shares a URL, asks what a page/site is about, wants a long article or design website summarized, wants installation/setup docs reduced to the essential meaning, wants to know whether a page is worth reading deeply, or asks what action to take next from English web content without translation-heavy detail.
---

# Webpage Interpreter

Read the target page first, identify what kind of page it is, then explain it in concise Chinese with as little cognitive load as possible.

## Core Goal

Help the user answer three questions quickly: "This page is mainly saying what, what do I actually need to care about, and should I keep reading?"

Default to explanation and summarization, not sentence-by-sentence translation.

## Workflow

1. Open the target page or source the user provided.
2. Ignore navigation, cookie banners, repeated footer text, and marketing filler unless they are necessary to understand the page.
3. Identify the page type before summarizing. Use `references/page-types.md` when needed.
4. Extract only the information that matters for the detected page type.
5. Explain everything in natural Chinese first. Keep English terms only when they are product names, commands, API names, or terms that are hard to translate accurately.
6. Judge whether the page is worth deep reading for the user's likely goal.
7. If the page implies an action, tell the user the next step in simple Chinese.
8. If the page is too long, start with a short executive summary, then give the most useful details.

## Output Rules

- Always start with a one-line answer to "这个网页主要是在讲什么".
- Prefer short sections and short bullets.
- Do not dump a full translation unless the user explicitly asks for it.
- Always include a short judgment on whether the page is worth reading deeply unless the user asks for raw summary only.
- If the page is actionable, include `下一步建议` with 1 to 3 practical actions.
- If the page is obviously a tutorial, explain the software/product first, then explain the steps only at a high level.
- If the page is an information page or long article, summarize the main points and conclusions.
- If the page is a design/portfolio/case-study page, explain the design theme, notable decisions, and what is worth learning from it.
- If important information is missing because the page could not be fully accessed, say that briefly.

## Page-Specific Behavior

### Installation or setup page

Answer in this order:

1. This is what software/tool/service it is.
2. This is what it is used for.
3. The installation page is mainly asking you to do what.
4. Only mention prerequisites, version constraints, or risky steps if they are important.
5. Tell the user the next step they should take if they actually want to proceed.

Do not expand every command unless the user asks.

### Information page, docs page, or announcement

Answer in this order:

1. What the page is about.
2. The most important facts.
3. What changed, why it matters, or what the user should remember.
4. Whether the page is worth reading in full or whether the summary is enough.

### Long design page, portfolio, or case study

Answer in this order:

1. What project or design topic this page is showing.
2. The core design ideas.
3. The most useful takeaways the user can borrow.
4. Whether the page is worth reading in detail for inspiration.

Prefer synthesis over detail overload.

## Default Response Template

Use this template unless the page type clearly needs a tighter version:

### 这页在讲什么

- One or two sentences in plain Chinese.

### 关键信息

- 3 to 6 bullets with the most useful points only.

### 值不值得继续读

- A short judgment such as `值得细读 / 只看摘要就够 / 只需要看某几段`.

### 下一步建议

- 1 to 3 practical next actions when applicable.

### 你现在最需要知道的

- A very short practical takeaway for the user.

## Compression Heuristics

- Compress aggressively when the page is long.
- Remove repeated examples unless they change the meaning.
- Keep commands, filenames, version numbers, and warnings intact.
- Translate concepts, not just words.
- If the page mixes product intro and tutorial, separate "它是什么" from "怎么做".
- If the page is low value for the user's likely goal, say so clearly and early.
- If only a few sections matter, name those sections explicitly.

## When The User Seems Overwhelmed

Prefer a softer, simpler output:

- `一句话说明`
- `3个重点`
- `要不要继续读`
- `下一步做什么`

If useful, explicitly tell the user whether the page is worth deep reading.

## Resource

- For classification and output shape, read [references/page-types.md](references/page-types.md) when the page type is ambiguous or mixed.
