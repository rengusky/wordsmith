# Wordsmith

A Claude skill that suggests changes to your writing without rewriting it.

Paste a paragraph and type `/wordsmith`. Your text comes back exactly as you wrote it, with only the words and phrases worth changing marked up, a one-line reason for each, and a clean version you can copy. Your voice and structure stay yours.

## Example

**You write:**

> Retaining the insert slide button even while editing is not something that is required. Insert slide if one off event which one done will be done again only if required. Retaining the button also create distraction to the slide while editing.

**Wordsmith returns:**

> **Suggestions** (6 changes)
>
> Retaining the insert slide button even while editing ~~is not something that is required~~ **is unnecessary**[1]. Insert slide ~~if~~ **is a**[2] ~~one off~~ **one-off**[3] event ~~which one done~~ **which, once done,**[4] will be done again only if required. ~~Retaining~~ **Keeping**[5] the button also ~~create distraction to~~ **distracts from**[6] the slide while editing.
>
> 1. Phrase → word: five words say "unnecessary".
> 2. Grammar: "if" should be "is a".
> 3. Spelling: "one-off" is hyphenated.
> 4. Typo: "once", with commas around the aside.
> 5. Repeat of "Retaining", so use a variant.
> 6. Grammar and tightening: singular verb, one word.

It finishes with the clean text in a code block, ready to copy.

## What it checks

- **Grammar and spelling.** Agreement, articles, punctuation, typos. It follows the spelling your text already uses (US or British/Indian), or the one you ask for: `/wordsmith US`.
- **Phrase → one word.** "in order to" → "to", "make a decision" → "decide".
- **Word swaps.** Vague, weak or repeated words, and filler like "basically" and "just".
- **Tone and clarity flags.** Passive voice, hedging and long sentences are marked in *italics ⚑* but not rewritten. Restructuring is your call.

If a paragraph is already clean, it says so instead of inventing suggestions.

## Install

1. Download [`wordsmith.skill`](wordsmith.skill) from this repo.
2. Upload it to Claude from the Skills section of Claude's settings.
3. In any chat, on desktop or mobile, paste your text and type `/wordsmith`.

To apply only some changes, reply "apply 1, 3, 5" or "skip 2".

## Files

- `wordsmith/SKILL.md`: the skill instructions. Edit them to make the skill your own.
- `wordsmith.skill`: the packaged skill, ready to install.

## License

MIT
