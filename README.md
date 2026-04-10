# Webpage Interpreter

A Codex skill that reads English webpages and explains them in simple Chinese.

It is designed for people who:

- often need to read English sites such as GitHub, docs pages, and product sites
- have limited English reading confidence
- want long design articles or case studies compressed into useful Chinese takeaways

## What This Skill Does

- tells you what a webpage is mainly about
- explains installation and setup pages in plain Chinese
- summarizes long articles, docs pages, and information pages
- extracts useful takeaways from design showcases and case studies
- reduces reading burden without forcing full translation

## Install

After publishing this repository to GitHub, install it with:

```bash
npx skills add https://github.com/<your-github-username>/webpage-interpreter-skill --skill webpage-interpreter
```

Replace `<your-github-username>` with your actual GitHub username.

## Usage

Examples:

```text
Use $webpage-interpreter to explain this webpage in Chinese.
Use $webpage-interpreter to summarize this long design article.
Use $webpage-interpreter to tell me what this install page is for.
Use $webpage-interpreter to tell me whether this page is worth reading deeply.
```

## Repository Structure

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

## Skill Behavior

This skill does not default to full translation.

Instead, it tries to answer:

1. What is this page mainly about?
2. What are the most important points?
3. Do I need to keep reading?

For install pages, it prioritizes:

1. what the software is
2. what it is used for
3. what the page is asking the user to do
4. any important prerequisites or risky steps

For long information or design pages, it prioritizes:

1. a simple Chinese explanation
2. a compressed summary
3. practical takeaways

## Publishing Checklist

- confirm the skill works locally
- create a GitHub repository
- push this folder to the repository
- replace the install URL in this README with your final repository URL
- optionally add screenshots or examples later

## Notes

- The skill is intentionally lightweight.
- The skill content belongs inside `skills/webpage-interpreter/`.
- Repository-level installation instructions belong in `README.md`, not inside `SKILL.md`.
