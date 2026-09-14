---
name: huminazer
description: >
  Rewrite the user's own text to strip out telltale signs of AI-generated writing
  while preserving 100% of the original meaning and facts. Use this skill whenever
  the user asks to "humanize" text, "make this sound less AI", "remove AI tells",
  or pastes a draft and says something like "run this through huminazer" — even if
  they don't use those exact words. This is a pure rewrite task: never add new
  claims, facts, examples, or analysis that wasn't in the original.
---

# Huminazer

Rewrites text to remove the stylistic fingerprints of LLM output — without changing what it says.

## Ground rules

1. **Never add new content.** No new facts, examples, statistics, hedges, or claims. If the original is thin, the output stays thin. Do not "improve" or "flesh out" the argument.
2. **Never delete real content.** Every fact, number, and claim in the input must survive in the output. You're changing *how* it's said, not *what* is said.
3. **Match the user's own voice where evident.** If they gave you a preference for short sentences, informal tone, directness, etc., lean into that. Otherwise default to plain, contraction-friendly, unpolished-but-competent human prose — the way an actual person writes an email or a doc, not a press release.
4. Output only the rewritten text (plus a one-line note on anything ambiguous you had to guess at), unless the user asked for a diff or explanation.

## What to strip out

Work through this checklist on every pass. These patterns are drawn from documented AI-writing tells — treat them as a checklist, not decoration.

**Vocabulary to kill on sight** (swap for plain synonyms or cut entirely):
delve, boast/boasts, crucial, pivotal, robust, tapestry, testament, underscore(s), showcase, foster/fostering, bolster, garner, intricate/intricacies, landscape (abstract), key (as filler adjective), align with, enhance, meticulous(ly), vibrant, interplay, leverage (as verb), navigate (abstract), realm, journey (metaphorical), unlock, seamless(ly), holistic, cutting-edge, game-changer/game-changing, in today's [X] world, at the end of the day.

**Sentence patterns to rewrite:**
- Copula avoidance — "serves as / stands as / functions as / represents" → just use "is". "features / offers / boasts" → just use "has".
- Vague connection words — "in connection with," "associated with," "in relation to" → use a direct verb or preposition (of, for, by, causes, uses).
- Negative parallelism — "not just X, but Y," "it's not X, it's Y," "no X, just Y" → say the one true thing plainly.
- Rule-of-three padding — forced triads ("clarity, consistency, and confidence") where the original only implied one or two points → collapse to what's actually there.
- Present-participle tack-ons at sentence ends ("...cementing its role as," "...highlighting the importance of," "...ensuring long-term success") → cut unless the user's original made that claim.
- Undue "significance" framing — "marks a pivotal moment," "represents a significant shift," "plays a crucial role" → replace with the plain, specific fact, or cut if there isn't one.
- Vague attribution — "experts say," "industry reports suggest," "many believe" when no specific source was given → flag it, don't invent a source; either cut the claim or make clear it's the writer's own view.
- Canned "Challenges and Future Outlook" arc, "In summary / In conclusion" wrap-ups, collaborative-assistant leftovers ("I hope this helps," "let me know if...") → delete, this is chat scaffolding, not content.
- Overly hedged intensifiers used as filler ("very," "quite," "arguably," "in many ways") → cut unless the user actually meant to hedge.

**Formatting to strip:**
- Excess em dashes used as punchy pauses → replace with commas, periods, or parentheses. Keep an em dash only if it's doing real work and the user's own writing uses them.
- Curly/smart quotes and apostrophes (" " ' ') → straight quotes (" ') unless the destination is a context (like Word) where curly is standard.
- Mechanical bolding of key phrases, inline-header bullet lists ("- **Point:** explanation") where prose would read naturally → convert to plain prose or plain lists without bold headers.
- Title Case Section Headings → sentence case.
- Rule-of-three bullet lists manufactured to look thorough → merge into sentences if that's how a person would actually write it.

## Process

1. Read the input once fully before touching anything — get the actual facts and structure straight.
2. Rewrite sentence by sentence, applying the checklist above. Prioritize sounding like one specific person talked, not "an AI trying to sound human." Vary sentence length naturally — real writers don't smooth every sentence to the same tidy length. Small imperfections (a fragment, a starting "And," a mildly repeated word) are fine and often more human than eliminating every repetition.
3. Do a final read against the original: confirm nothing was added, nothing factual was dropped, and the structure/order of ideas still matches unless reordering was needed to remove a canned pattern (e.g., cutting a tacked-on "Conclusion" section).
4. Output the result.

If the input is long (multi-page), work through it in order rather than summarizing — this is a rewrite, not a compression.

## Example

**Input:**
> In today's fast-paced digital landscape, our platform serves as a robust solution that boasts seamless integration capabilities. By leveraging cutting-edge technology, we're able to foster meaningful connections and unlock new opportunities for growth. Not just a tool, but a true partner in your journey — ensuring long-term success every step of the way.

**Output:**
> Our platform integrates easily with the tools you already use. It's built on solid, current tech, and it's meant to help you actually grow, not just say the word "growth" at you.
