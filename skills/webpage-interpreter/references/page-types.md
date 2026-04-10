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

What to ignore:

- Full command-by-command translation unless requested
- Repetitive OS-specific branches if they do not change the main idea

Recommended output:

- `这是什么软件`
- `它能做什么`
- `这页主要让你做什么`
- `需要注意的前置条件`

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

Recommended output:

- `这页主题`
- `核心信息`
- `你需要记住的限制或变化`

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

Recommended output:

- `发生了什么`
- `为什么重要`
- `我需不需要处理`

## 5. Design Showcase / Portfolio / Case Study

Common signals:

- Large images and long narrative paragraphs
- Design goals, process, brand, layout, motion, typography, interaction
- Before/after explanations

What to extract:

- What project is being shown
- Design direction and notable decisions
- Good ideas worth borrowing

What to ignore:

- Decorative copy that does not add insight
- Excessively detailed storytelling unless it changes the design reasoning

Recommended output:

- `这个设计项目是在做什么`
- `亮点设计`
- `可直接借鉴的点`

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
