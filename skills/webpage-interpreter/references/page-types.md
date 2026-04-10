# Page Types

Use this reference only when the page type is mixed, noisy, or unclear.

## 1. Installation / Setup / Quickstart

Common signals:

- Headings like `Install`, `Setup`, `Getting Started`, `Quickstart`
- Command snippets such as `npm install`, `pip install`, `brew install`
- Environment requirements, versions, prerequisites

What to extract:

- Product or tool name
- What it does
- What the page is asking the user to install or configure
- Important prerequisites or risky steps
- The immediate next step if the user wants to continue

What to ignore:

- Full command-by-command translation unless requested
- Repetitive OS-specific branches if they do not change the main idea

Recommended output:

- `这是什么软件`
- `它能做什么`
- `这页主要让你做什么`
- `需要注意的前置条件`
- `下一步做什么`

## 2. Product / Marketing / Landing Page

Common signals:

- Big hero headline
- Feature blocks
- Social proof
- CTA buttons like `Start free`, `Book a demo`

What to extract:

- What the product is
- Who it is for
- Main capabilities
- Whether the page is mostly marketing or contains actionable information
- Whether it is worth reading deeply or just skimming

Recommended output:

- `它是什么`
- `面向谁`
- `核心卖点`
- `值不值得细看`

## 3. Docs / Reference / Information Page

Common signals:

- Structured headings
- API names, options, parameters, configuration sections
- Dense explanatory text

What to extract:

- Topic and scope
- Key facts or concepts
- Any important caveats, versions, or constraints
- Whether the page needs full reading or whether a summary is enough

Recommended output:

- `这页主题`
- `核心信息`
- `你需要记住的限制或变化`
- `值不值得继续读`

## 4. News / Changelog / Announcement

Common signals:

- Publish dates
- Release notes
- New feature lists
- "What's new" style sections

What to extract:

- What changed
- Why it matters
- Who is affected
- Whether the user needs to take action
- The next action if the announcement requires follow-up

Recommended output:

- `发生了什么`
- `为什么重要`
- `我需不需要处理`
- `下一步做什么`

## 5. Design Showcase / Portfolio / Case Study

Common signals:

- Large images and long narrative paragraphs
- Design goals, process, brand, layout, motion, typography, interaction
- Before/after explanations

What to extract:

- What project is being shown
- Design direction and notable decisions
- Good ideas worth borrowing
- Whether the page is worth deep reading for inspiration or only worth skimming

What to ignore:

- Decorative copy that does not add insight
- Excessively detailed storytelling unless it changes the design reasoning

Recommended output:

- `这个设计项目是在做什么`
- `亮点设计`
- `可直接借鉴的点`
- `值不值得细读`

## 6. Mixed Pages

When a page mixes several modes, choose the dominant one and add one short note for the secondary mode.

Examples:

- Product intro + install docs:
  Explain `它是什么` first, then `如何开始`.
- Design case study + agency marketing:
  Explain the case study first, then note that the rest is agency self-promotion.

## Default Reading Priority

When time or page length is a problem, read in this order:

1. Title and subtitle
2. Section headings
3. Intro paragraph
4. Summary/conclusion blocks
5. Commands, warnings, version notes, dates
6. Body details only if still needed

## Reading Verdict Heuristic

Use a simple Chinese verdict whenever useful:

- `值得细读`: The page contains important decisions, high-signal detail, or directly relevant steps.
- `先看摘要就够`: The page is mostly informational and the main idea can be compressed safely.
- `只看这几段`: Only a few sections matter; name them explicitly.
- `不用细读`: The page is mostly marketing filler, duplicated information, or low-value detail for the user's likely goal.
