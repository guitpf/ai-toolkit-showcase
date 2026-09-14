---
name: tone-alternatives
description: Generate 5 rewritten versions of a message in different tones and styles. Use this skill whenever the user wants to rephrase, rewrite, or get alternative versions of a message they're writing — even if they just say "give me options", "how else could I say this", "rewrite this", "other ways to say", or pastes a message and asks for alternatives. Trigger for any message type: WhatsApp, work chat, social media captions, emails, or anything else. Always apply this skill when the user shares a piece of text and wants variations.
---

# Tone Alternatives Skill

When the user shares a message they want to rewrite, generate **5 alternative versions** in different tones and styles.

## Core rules

- **Language**: Use whatever language the user specifies (or match the language of their message if they haven't said). Never switch languages unless asked.
- **Formality in German**: Always use **"du"** form. Never use "Sie" or any formal address.
- **Tone selection**: Don't use a fixed set — read the context of the message and pick the 5 most useful tones for *that specific message*. A work Slack message and a WhatsApp breakup text need very different options.
- **No fluff**: Don't explain what you're doing. Just show the 5 versions.
- **Keep the meaning**: All 5 versions should convey the same core intent as the original.

## Output format

For each version, show:
- A short label naming the tone (e.g. **Casual & warm**, **Direct**, **Playful**, **Professional**, **Empathetic**)
- The rewritten message

No introductory sentence. No closing commentary. Just the 5 labeled versions.

## Tone palette to draw from (pick what fits)

Casual & warm · Direct & confident · Playful / witty · Empathetic · Formal (but not stiff) · Hype / enthusiastic · Soft / gentle · Dry / deadpan · Urgent · Friendly but professional · Short & punchy · Elaborate & detailed · Diplomatic · Assertive · Lighthearted

## Example

**User input:**
> rewrite this in English: "Hey, just wanted to check if you're still coming to the meeting tomorrow?"

**Output:**

**Casual & warm**
Hey! Still good for tomorrow's meeting? 😊

**Direct**
Are you coming to the meeting tomorrow — yes or no?

**Playful**
Tomorrow's meeting — you in or you ghosting us? 👀

**Soft / gentle**
No pressure at all, just wanted to check — are you still planning to join tomorrow?

**Short & punchy**
Meeting tomorrow — still on?
