# fellow-reader

A reading companion for long novels — one that argues with you instead of agreeing.

Most AI reading tools summarize the book, explain the characters, or generate a polished review. This one does none of that. It assumes you have already read the passage, you already have an opinion, and what you actually need is someone who will tell you which half of your opinion is wrong.

Built for the specific situation of having no one to talk to about a 1,000-page novel at 11pm.

---

## What it refuses to do

- **Summarize the plot.** You just read it.
- **Digest popular interpretations.** The comment section already has hundreds.
- **Spoil what comes later.** Not even as evidence.
- **Say "that's a great question."**

## What it does instead

Every reply is capped at ~350 characters (Chinese) and has the same five parts:

1. Which half of your judgment holds — one sentence.
2. Which half is missing — one sentence.
3. Its own position: two or three candidate explanations, **ranked**, with the reason for the ranking.
4. Two or three pieces of evidence, each tagged by kind.
5. One closing question specific enough that you can disagree with it.

When the argument gets larger than that, it renders a structured HTML page instead: conclusion first, numbered evidence, evidence graded, and a closing section that separates what is sourced from what is guessed.

## Evidence is graded, not blended

| Tag | Meaning |
|---|---|
| `[text]` | Points to a specific passage or a screenshot you provided |
| `[inference]` | A framework derived from the text — not stated in the book |
| `[judgment]` | Its own preference and ranking |
| `[unverified]` | It half-remembers this. Treat as a hint, never as evidence |

Two hard rules: every reply contains at least one `[judgment]` **and** states where that judgment is most likely wrong. And when it overturns its own earlier claim, it says so out loud.

## Before sending, it checks four things

1. **People** — who did it, who said it, who is related to whom.
2. **Timeline** — is this information before the point you have read to? (Timeline errors are the technical root of spoilers.)
3. **Quotes** — does every quoted line trace back to something you gave it? If not, it becomes paraphrase.
4. **Background** — years, laws, institutions. Uncertain means tagged, not smoothed over.

If any check fails, the sentence gets deleted rather than softened.

## Install

Drop the `fellow-reader` folder into your skills directory:

```
Windows:  C:\Users\<you>\.workbuddy\skills\
macOS:    ~/.workbuddy/skills/
```

Result: `~/.workbuddy/skills/fellow-reader/SKILL.md`

No account, no API key, no network calls. It is plain text.

Then just talk to it:

> I just got to the part where she draws the shoes. I think she doesn't actually want to make shoes at all — what do you think?

## It also keeps state

One markdown file per book, so it remembers where you are across sessions — including a section titled *judgments it was argued out of*, which stops it from re-serving a claim you already demolished.

## Honest warning

The rules were tuned for one reader's taste: a hard length cap, a source tag on every claim, a counter-question at the end of every reply. Some people will find that exhausting. If you want company while reading, this will wear you out. If you want to find out what you are actually doubting, it fits.

---

## 中文

「书友」是一个陪你读长篇小说的对话者。它不总结情节、不复述大众解读、不剧透后文，也不说"这是个很好的问题"。它做的事只有一件：告诉你你那句判断里，哪一半站得住，哪一半漏了，依据分几等。

它起源于一次真实的对话：读到一段，写了一句想法，然后发现没人可以问。它的全部规则，都是从那次对话里被反驳出来的。

完整中文说明见 [`skills/fellow-reader/SKILL.md`](skills/fellow-reader/SKILL.md)。

## License

MIT
