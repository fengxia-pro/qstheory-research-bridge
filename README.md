# Qstheory Research Bridge / 慢老师的求是科研转译

**Qstheory Research Bridge** is a portable AI-agent skill that translates fresh Qiushi/Qstheory policy signals into researcher-readable scientific problems, NSFC/funding directions, SCI paper angles, and daily policy-research watch reports.

**求是科研转译** 是一个可跨智能体使用的技能包，用来把求是网/《求是》中的政策信号，转译成科研工作者能理解和使用的科学问题、国自然选题方向、SCI 论文切口和每日政策科研风向。

## Who Can Use It / 适用智能体

This package is not limited to OpenAI Codex. Any AI agent that can read Markdown instructions can use it, including:

- OpenAI Codex / ChatGPT-style agents
- Claude Code
- OpenCode / OpenHands / other coding agents
- Local or cloud LLM agents with browsing capability

这个技能包不只服务于 Codex。只要智能体能读取 Markdown 指令，并能联网检索求是网内容，就可以使用。

## Files / 文件结构

```text
qstheory-research-bridge/
  SKILL.md                         # Canonical cross-agent workflow / 核心跨平台技能说明
  AGENTS.md                        # Generic agent entrypoint / 通用智能体入口
  CLAUDE.md                        # Claude Code entrypoint / Claude Code 入口
  README.md                        # GitHub bilingual introduction / GitHub 中英文说明
  agents/openai.yaml               # Optional OpenAI/Codex metadata / 可选 OpenAI 元数据
  references/output-templates.md   # Output templates / 输出模板
  references/source-map.md         # Qstheory source map / 求是网信源地图
```

## How To Use / 使用方式

Tell your agent:

```text
Use the qstheory-research-bridge skill. My research direction is: [your field].
Browse current Qstheory/Qiushi sources and translate the policy signals into scientific questions, NSFC angles, and SCI paper opportunities.
```

中文提示词：

```text
请使用 qstheory-research-bridge 技能。我的研究方向是：[你的方向]。
请浏览最新求是网/《求是》内容，把政策信号转译成科学问题、国自然选题方向和 SCI 论文切口。
```

## Daily Watch / 每日推送

For recurring daily scans, ask your host agent to schedule this skill at your preferred time. Example:

```text
Every day at 04:30 Beijing time, use qstheory-research-bridge to browse current Qstheory/Qiushi sources and produce a Chinese policy-research scan for researchers.
```

每日推送可设置为：

```text
每天北京时间 04:30，使用 qstheory-research-bridge 浏览最新求是网/《求是》内容，生成面向科研工作者的中文政策科研风向解读。
```

## Output Focus / 输出重点

- Original policy evidence / 政策原文证据
- Feynman-style explanation / 费曼式解释
- Scientific questions / 科学问题
- NSFC and funding angles / 国自然与资助方向
- SCI paper angles / SCI 论文切口
- Keyword watchlist / 后续追踪关键词

Funding judgments should always be cautious and evidence-based. This skill helps interpret policy signals; it does not guarantee funding outcomes.

资助判断必须谨慎、基于证据。这个技能用于解读政策信号，不承诺任何项目一定获得资助。
