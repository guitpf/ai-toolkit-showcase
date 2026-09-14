---
name: huminazer-german
description: Rewrite German text to remove all telltale signs of AI/LLM writing (ChatGPT-style phrasing, formatting, and tone) while keeping the original meaning, facts, and length roughly intact. Use this skill whenever the user gives German text and asks to "humanize" it, "entlarven"/remove AI-Merkmale, make it sound less like ChatGPT, or references "huminazer". Do NOT use for translation, summarization, or content generation tasks — only for rewriting existing German text to sound human-written. Never add new facts, claims, or content that wasn't in the original.
---

# Huminazer (German)

Rewrite German text so it no longer reads as AI-generated, based on the community-documented indicators German Wikipedia editors use to detect LLM writing (see `references/ai_indicators_de.md` for the full source list).

## Core rule

**Only remove/rewrite. Never add.** Don't invent new facts, claims, sources, or elaborations. The rewritten text must carry exactly the same meaning and information as the input — shorter is fine, richer is not. If something is factually ambiguous in the original, keep it ambiguous; don't resolve it with invented specifics.

## Workflow

1. Read the input German text fully.
2. Read `references/ai_indicators_de.md` if you need the detailed reasoning behind any pattern below — most of the time the checklist here is enough.
3. Rewrite applying the checklist below.
4. Do a final pass specifically hunting for anything you personally would have written if generating this text from scratch — that's the strongest signal of what to cut, since you already know your own tics.
5. Output only the rewritten text (no explanation, no meta-commentary, no "Hier ist die humanisierte Version"), unless the user asked for a comparison or explanation.

## Checklist: what to strip or rewrite

### Formatting (usually the fastest wins)
- Remove all Markdown: no `**bold**`, no `#`/`##` headers, no `---` dividers, no bullet lists with `-`/`•` unless the original human context clearly called for a list (Wikipedia articles, formal docs rarely need bullets for prose).
- Convert Halbgeviertstriche (–) used as parenthetical dashes back to normal punctuation (commas, parentheses, or Punkt) unless clearly intentional/stylistic in context.
- Remove emojis entirely.
- Remove any fake/placeholder template syntax, broken references, or bracketed placeholders like `[Datum]`, `[Name einfügen]` — either fill with what's actually known from context or drop the clause.

### Sentence & paragraph structure
- Break up long, symmetrical, over-explained sentences into shorter, more clipped ones — real human writing (especially informal German) is uneven, not uniformly polished.
- Kill obligatory closing "Zusammenfassung" or "Fazit" sentences/paragraphs that just restate what was already said. Human writing usually just stops.
- Remove "Herausforderungen und Zukunftsaussichten"-style boilerplate closers (e.g. "Trotz dieser Erfolge steht X jedoch vor mehreren Herausforderungen...").
- Break up mechanical "nicht nur..., sondern auch..." parallelisms — rewrite as a plain statement.
- Break up rule-of-three (Trikolon) constructions ("sowohl X als auch Y und Z", "A, B und C" adjective/phrase triplets) when they feel inserted for rhetorical effect rather than natural listing.

### Word- and phrase-level tells
Cut or replace these when they appear (this is not exhaustive — use judgment, the underlying pattern matters more than the exact word):
- Overblown significance language: "spielt eine wichtige/bedeutende Rolle", "unterstreicht seine Bedeutung", "fasziniert weiterhin", "hinterlässt einen bleibenden Eindruck", "Wendepunkt", "Schlüsselmoment", "tief verwurzelt", "unerschütterliche Hingabe", "steht als Zeugnis für", "festigt".
- Marketing/travel-brochure language: "reiches kulturelles Erbe", "reiche Geschichte", "atemberaubend", "unbedingt besuchen/sehen", "beeindruckende natürliche Schönheit", "bleibendes Vermächtnis", "eingebettet in", "im Herzen von".
- Editorializing filler: "es ist wichtig zu erwähnen/bedenken/beachten", "es ist bemerkenswert, dass", "keine Diskussion wäre vollständig ohne".
- Overused mechanical connectors when used stiffly/repeatedly: "darüber hinaus", "zusätzlich", "außerdem", "ferner" — vary or cut, don't chain them formulaically.
- Vague-authority hedges ("Weasel wording"): "Branchenberichte zeigen", "Beobachter haben festgestellt", "einige Kritiker argumentieren" — either name the actual source or cut the claim.
- Participial "surface analysis" tack-ons: "...gewährleistend", "...hervorhebend", "...betonend", "...widerspiegelnd" at the end of clauses.
- False-range listing: "von X bis Y" used loosely to gesture at a set of examples rather than a real range.
- Knowledge-gap disclaimers, if present from a prior AI pass: "Stand [Datum]", "bis zu meinem letzten Wissensstand", "in den verfügbaren Quellen/Suchergebnissen", "basierend auf verfügbaren Informationen" — remove entirely, they have no place in human writing.
- Collaborative-chatbot leftovers, if present: "Ich hoffe, das hilft", "Natürlich!", "Lassen Sie mich wissen, falls...", "hier ist eine detaillierte Aufschlüsselung".
- Letter-style openers/closers if this isn't actually a letter: "Ich schreibe, um...", "Vielen Dank für Ihre Zeit/Überlegung", subject-line-style "Betreff:" headers.

### Tone
- Flatten excessive politeness/formality that doesn't match the context (e.g. informal chat vs. formal letter — match the register the user's original text was already in, don't upgrade it).
- Remove redundant editorial hedging/qualifying that piles up ("könnte möglicherweise unter Umständen..." → pick one hedge or none).
- If the original text has some rough edges, minor informality, or inconsistency, it's fine to leave a bit of that in — perfectly smooth, evenly-paced prose across an entire long text is itself an AI tell. Don't over-polish.

## What NOT to change
- Facts, numbers, names, dates, claims — never alter meaning.
- Direct quotes.
- Legitimate references/citations that are correctly formatted — don't break real sources while hunting for fake ones.
- The user's own voice/quirks if this is clearly their personal writing rather than a formal piece (e.g. WhatsApp messages, personal notes) — humanizing should preserve *their* idiosyncrasies, not impose a generic "human" style.

## Output

Return just the rewritten German text. If the user explicitly asks what was changed, follow up with a brief bullet list of the categories of edits made (not a full diff) — but only if asked.
