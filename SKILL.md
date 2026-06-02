---
name: qstheory-research-bridge
description: Translate fresh Qiushi/Qstheory policy signals into researcher-readable scientific problems, NSFC/funding directions, SCI paper angles, and daily policy-research watch reports. Use when a user mentions 求是网, 求是, qstheory.cn, 国自然选题, SCI选题, 国家真实需求, 政策风向, 科技自立自强, 新质生产力, 未来产业, or asks to connect a research direction with Chinese national strategy and leadership-policy signals.
---

# Qstheory Research Bridge

Portable AI-agent skill for translating Qiushi/Qstheory policy signals into researcher-readable scientific questions, NSFC/funding angles, SCI paper opportunities, and daily policy-research watch reports.

This instruction file is platform-neutral. OpenAI Codex, Claude Code, OpenCode, OpenHands, local LLM agents, and other Markdown-capable agents can use it directly. Platform-specific files such as `agents/openai.yaml`, `AGENTS.md`, or `CLAUDE.md` are optional entrypoints; `SKILL.md` remains the canonical workflow.

## Core Rule

Browse current Qstheory/Qiushi sources on every run unless the user explicitly provides article text. Treat Qstheory as the primary source, cite exact article titles, dates, and URLs, and clearly separate:

- 原文证据: what the article says.
- 科研转译: what this may imply for scientific questions.
- 资助判断: cautious inference about likely funding attention, never a guarantee.

Default output language is Chinese.

## Workflow

1. Parse the research direction. Extract domain, object, method, scenario, bottleneck, disease/material/system/population, and likely funding category. If the direction is broad, proceed with explicit assumptions rather than stopping.
2. Collect fresh sources. Read `references/source-map.md` when source selection matters. Start from Qstheory homepage and relevant channels, especially 科教, 求是专区, 社论评论, 学习问答, 求是专访, 深度调研, 专家学者, and current issue pages. Use site search queries combining the user's field with policy terms.
3. Rank candidates. Prefer sources in this order:
   - 习近平重要文章 or central-level policy interpretation in 《求是》.
   - 《求是》杂志编辑部、评论员、社论评论、学习问答.
   - 求是专访、深度调研、专家学者.
   - Qstheory转载的人民日报、新华社、光明日报、经济日报、科技日报等 articles.
4. Extract policy signals. For each strong source, identify the core strategic phrase, named domain, unresolved bottleneck, target population/industry/system, and implied evaluation metric.
5. Translate with Feynman language. Explain as if speaking to a capable labmate outside the policy field: concrete nouns, causal chains, examples, no empty slogan repetition.
6. Generate research outputs. Use `references/output-templates.md` for daily scans, deep reads, NSFC translation, and SCI angle generation.
7. State evidence limits. If no strong current source matches, say so and widen to adjacent policy signals; do not force a connection.

## Search Strategy

Build three query layers:

- Field terms: user-provided keywords plus synonyms, English abbreviations translated into Chinese, and adjacent disciplines.
- Policy terms: 国家战略需求, 科技创新, 科技自立自强, 新质生产力, 未来产业, 关键核心技术, 卡脖子, 基础研究, 原始创新, 产业链供应链, 绿色低碳, 健康中国, 数字中国, 人工智能, 数据要素, 安全治理, 教育科技人才.
- Funding terms: 国家自然科学基金, 基础研究, 重大专项, 青年人才, 交叉学科, 产学研, 成果转化, 标准, 评价体系.

For daily watch, default to the newest 1-7 days. If there are fewer than 3 relevant items, widen to the newest issue/month and say the window was expanded.

## Translation Rubric

Convert policy language into research language through these moves:

- 宏大判断 -> 可观察变量: "高质量发展" becomes efficiency, resilience, equity, safety, or sustainability metrics.
- 战略方向 -> 机制问题: "人工智能赋能" becomes where AI changes discovery, diagnosis, control, prediction, or coordination mechanisms.
- 产业瓶颈 -> 科学问题: "卡脖子" becomes unresolved principles, material constraints, algorithmic limits, measurement gaps, or system-integration failure modes.
- 治理目标 -> 评价框架: "安全可控" becomes risk metrics, robustness, explainability, compliance, and monitoring systems.
- 需求牵引 -> 项目设计: "产业出题、科技答题" becomes a research question with scenario, mechanism, method, validation data, and expected boundary conditions.

## Output Quality Bar

- Include source links and publication dates in every substantive answer.
- Quote only short fragments when necessary; paraphrase most policy text.
- Do not say "国家领导人的真实意图是..." Say "从该文可见的政策信号是..." or "可以谨慎推断的资助关注点是..."
- Give actionable project language: candidate title, central hypothesis, key scientific question, methods, data/sample needs, expected contribution, and risk.
- For NSFC suggestions, distinguish 基础科学问题 from 应用示范 and policy rhetoric.
- For SCI suggestions, identify the international conversation: mechanism novelty, method novelty, dataset/resource novelty, or China-specific but globally relevant scenario.
- End with a compact watchlist of keywords the user should track next.

## Recurring Watch

If the user explicitly asks for a daily reminder, monitor, or recurring push, use the host agent's available scheduling, reminder, cron, automation, or background-task feature if present. The recurring task prompt should ask the future agent to use this skill, browse Qstheory fresh sources, and produce the daily scan template.
