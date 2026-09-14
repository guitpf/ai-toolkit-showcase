# AI Toolkit Showcase

**Live demo:** https://guitpf.github.io/ai-toolkit-showcase/ (a page you can open and click through — no setup needed)

## What this is

I'm Gui, a digital/growth marketing manager. Over the past year I've built a set of custom "skills" — reusable instruction sets — for Claude, Anthropic's AI assistant, to handle specific tasks I run into constantly at work and in daily life: rewriting text so it doesn't read as AI-generated, evaluating whether a job posting is actually worth applying to, rewriting a message in five different tones before I send it, and drafting customer-service replies in German.

This repo is proof that I don't just *use* AI chat — I configure and build tools with it that do real, specific, repeatable work. Each skill here is one I actually use, not a demo built for this portfolio.

## Why this matters for a marketing role

Every one of these skills solves a problem that shows up directly in growth/performance marketing work: brand voice consistency, candidate/opportunity evaluation, message testing across tones, and customer support at scale. Building tools like this is the same skill as building a working prompt library, an internal AI workflow, or a lightweight automation for a marketing team — just proven on my own problems first.

## The skills

| Skill | What it does |
|---|---|
| [`huminazer`](skills/huminazer/SKILL.md) | Rewrites AI-sounding English text to read as human-written, without changing the meaning or adding content |
| [`huminazer-german`](skills/huminazer-german/SKILL.md) | The German-language version — same idea, tuned to German-specific AI writing tells |
| [`career-fit-analyzer`](skills/career-fit-analyzer/SKILL.md) | Scores a job posting against my actual background: hard skill match, culture fit, top differentiators to lead with, and honest gap analysis with reframing language |
| [`tone-alternatives`](skills/tone-alternatives/SKILL.md) | Rewrites a message I'm about to send in 5 different tones, so I can pick the right one before hitting send |
| [`whatsapp-kundenservice`](skills/whatsapp-kundenservice/SKILL.md) | Drafts short, warm, on-brand WhatsApp customer service replies in German — including handling a frustrated customer, not just FAQs |

Each skill folder has the exact instruction file ("SKILL.md") that configures Claude's behavior — the same format Anthropic uses for its own skills system. The live demo page shows each one in action with a real before/after example.

## A note on the examples

The before/after examples on the demo page and in each skill file are illustrative, not pulled from real customer or company data — nothing here reproduces confidential business information from any employer.
