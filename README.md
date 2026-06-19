# Voice Skill — write LinkedIn posts in *your* voice, not the AI's

A [Claude Code](https://docs.claude.com/en/docs/claude-code) skill that turns a rough thought
into a LinkedIn post that sounds like you — and never invents content. You give it your raw
notes; it arranges and phrases what *you* supplied, and when something's missing it **asks**
instead of making it up.

The first time you run it, it interviews you to build your own voice profile. After that, it
drafts.

---

## What it does

- Give it a rough thought (a few messy sentences) → it hands back a LinkedIn post in your voice.
- Give it bullets instead → it hands back a plan (angle, gaps, an order for your points), no draft.
- It never fills a gap with a guess. If it doesn't know, it asks you. Every line traces back to
  something you actually said.

## How it works

Eight steps, and you confirm each one: it works out what you need → names the post type →
builds a hook from your words → sets the format → asks what's missing (it never makes anything
up) → writes the draft → checks every line → hands it back. The whole time it writes in your
voice, not the AI's.

![How the voice skill works](Voice%20Skill.png)

## What's under the hood

A few plain files, each with one job. The skill file holds only the steps; everything it can
look up lives in its own file (a bloated skill file confuses the AI).

![Folder structure](Skill%20File%20Structure.png)

| File | Job |
|---|---|
| `SKILL.md` | the step-by-step instructions — the brain |
| `onboarding.md` | first-run setup (samples + interview) that builds your `voice.md` |
| `voice.md` | how *you* actually write (you build this on first run) |
| `guardrails.md` | what the AI must never do |
| `linkedin.md` | platform rules + best practices |
| `post-types-and-hooks.md` | which hooks fit which content |
| `anti-patterns.md` + `inspiration.md` | examples of what to avoid + what you like |

---

## Install

1. Copy this folder into your Claude Code skills directory, renamed `voice-skill`:
   - **Personal (all projects):** `~/.claude/skills/voice-skill/`
   - **One project only:** `<your-project>/.claude/skills/voice-skill/`
2. That's it — Claude Code discovers it automatically from `SKILL.md`.

## Use

- **First run:** the skill sees your `voice.md` is empty and runs a short interview — it asks
  for a few samples of your real writing, walks you through the interview questions in
  `onboarding.md`, then builds your `voice.md`.
- **After that:** just paste a rough thought and ask for a LinkedIn post. It drafts in your
  voice.

## Credit

The interview questions in this repo are original. The idea behind them — a plain text file
that captures how *you* write, so an AI can sound like you instead of like itself — is inspired
by Ruben's essay
[*I am just a text file*](https://ruben.substack.com/p/i-am-just-a-text-file). None of his
wording is reproduced here; the essay is well worth reading for the why.

## Status

This is **v1**. The voice gets better the more real writing you feed it — after you publish a
few posts, paste them back so it can tighten the "how you write" section.

Feedback welcome: open an issue with what worked, what didn't, and what v2 should improve.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, make it yours.
