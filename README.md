# Webpage Interpreter

中文网页解读器。  
A Codex skill for reading English webpages and explaining them in simple Chinese.

## 简介 | Overview

`Webpage Interpreter` 是一个面向中文用户的 Codex skill，用来降低阅读英文网页的门槛。

它特别适合这些场景：

- 需要经常看 GitHub、官方文档、产品页、博客文章
- 英文基础一般，不想逐句硬翻
- 设计网站、案例研究、长文章太长，想先快速知道重点
- 希望先判断“这页到底讲什么，值不值得继续读”

`Webpage Interpreter` helps Chinese-speaking users quickly understand English webpages without requiring full translation.

It is especially useful when:

- you often read GitHub, docs sites, product pages, or blog posts
- you do not want to read long English pages line by line
- design case studies and long-form articles feel too dense
- you want a fast answer to: "What is this page about, and should I keep reading?"

## 主要功能 | What This Skill Does

- 用中文快速说明一个网页主要在讲什么
- 把安装页、教程页解释成更容易理解的中文重点
- 总结长文档、信息页、博客和公告页
- 提炼设计展示页和案例研究里的有用观点
- 默认优先“解释和总结”，而不是整页逐字翻译

- explains what a webpage is mainly about in Chinese
- simplifies install pages and setup docs into practical takeaways
- summarizes long docs, information pages, blogs, and announcements
- extracts useful takeaways from design showcases and case studies
- prioritizes explanation and summarization over full translation

## 安装 | Install

你可以通过下面的命令安装这个 skill：

Install this skill with:

```bash
npx skills add https://github.com/crank-dc/webpage-interpreter-skill --skill webpage-interpreter
```

## 使用示例 | Usage

你可以这样调用它：

You can use it like this:

```text
Use $webpage-interpreter to explain this webpage in Chinese.
Use $webpage-interpreter to summarize this long design article.
Use $webpage-interpreter to tell me what this install page is for.
Use $webpage-interpreter to tell me whether this page is worth reading deeply.
```

也可以直接用更自然的中文表达：

You can also use more natural Chinese prompts:

```text
用 $webpage-interpreter 帮我看这个网页，告诉我它主要讲什么。
用 $webpage-interpreter 总结这个长文章的重点。
用 $webpage-interpreter 告诉我这个安装页面是在做什么。
用 $webpage-interpreter 判断这个设计案例值不值得细读。
```

## 输出风格 | Output Style

这个 skill 默认不会把网页整页翻译出来，而是优先回答这几个问题：

This skill does not default to full-page translation. Instead, it tries to answer:

1. 这个网页主要在讲什么？  
   What is this page mainly about?
2. 最重要的信息是什么？  
   What are the key points?
3. 我值不值得继续读？  
   Is it worth reading more deeply?

### 对安装页 | For Install Pages

优先说明：

- 这是什么软件或服务
- 它能做什么
- 这页主要让你做什么
- 有哪些前置条件或风险点

It prioritizes:

- what the software or service is
- what it does
- what the page is asking you to do
- important prerequisites or risky steps

### 对信息页、文档页、公告页 | For Docs, Info Pages, and Announcements

优先说明：

- 页面主题
- 关键事实
- 有什么变化、限制或结论

It prioritizes:

- the page topic
- the key facts
- changes, constraints, or conclusions

### 对设计站点和案例页 | For Design Sites and Case Studies

优先说明：

- 这个项目在做什么
- 设计亮点是什么
- 哪些想法值得借鉴

It prioritizes:

- what the project is about
- the main design highlights
- what is worth borrowing or learning from

## 仓库结构 | Repository Structure

```text
webpage-interpreter-skill/
├── README.md
├── LICENSE
├── .gitignore
└── skills/
    └── webpage-interpreter/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            └── page-types.md
```

## 适合谁使用 | Who This Is For

这个 skill 特别适合：

- 英文阅读有压力的中文用户
- 经常需要快速查看国外工具、文档和网站的人
- 想减少信息负担、先抓重点的人

This skill is a good fit for:

- Chinese-speaking users who find English pages tiring to read
- people who frequently browse international tools, docs, and websites
- anyone who wants the key information first before reading in depth

## 发布说明 | Publishing Notes

- skill 本体放在 `skills/webpage-interpreter/`
- 仓库级说明放在 `README.md`
- `agents/openai.yaml` 用于 UI 展示与默认提示
- `references/page-types.md` 用于页面类型判断和输出策略

- the skill itself lives in `skills/webpage-interpreter/`
- repository-level instructions belong in `README.md`
- `agents/openai.yaml` provides UI metadata and a default prompt
- `references/page-types.md` supports page-type detection and output strategy

## License

MIT
