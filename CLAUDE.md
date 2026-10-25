# CLAUDE.md — Suggest What to Cook project rules

## Who you're working with
I'm a PM learning to build for the first time. This project is as much about me
UNDERSTANDING every layer as it is about shipping. Treat me as smart but new:
no unexplained jargon, ever. The first time any technical term or tool comes up
(API, environment variable, framework name, deploy, whatever), define it in one
or two plain sentences before using it.

## How to work with me
- Explain every technical decision BEFORE making it: what the thing is, why
  this choice over the obvious alternative, and what it does for us underneath.
  If a decision would normally be made silently by a solo developer, surface it.
- Go step by step. One thing at a time. When you finish a chunk, stop and tell
  me in plain language what now exists and what changed, before moving on.
- I get overwhelmed by big dumps of code or options. Prefer the smallest change
  that works. Never refactor or "improve" things I didn't ask about.
- When something breaks, explain what broke and why in plain words first, then fix it.

## What we're building
TBD — scope not decided yet. Do not assume any particular approach (recipe
data, AI generation, features, etc.) until we've talked it through and agreed.

## Technical ground rules
- Web app. Start with the simplest thing that works (plain HTML/CSS/JS is fine
  to begin). Do not introduce a framework, database, or service without first
  explaining what it is, why now, and what the alternative was — then wait for
  my go-ahead.
- Keep secrets (API keys) out of committed code. Explain what an environment
  variable is the first time we need one.

## Habits to enforce every session
- Commit after every real chunk of progress with a clear message. No giant
  end-of-day commits. Tell me what you're committing and why.
- Maintain a file called TRADEOFFS.md in the repo root. Every time we make a
  meaningful choice (framework or not, data shape, model choice, etc.), append
  one line: what we picked, over what, and why. This file becomes the
  "Tradeoffs" section of the README later — the most important section for
  my goals.
- The README is built incrementally, not at the end. Structure:
  Problem · Solution & how it works · Tradeoffs considered · Evals · What I
  learned / what broke / what's next.

## Tone
Patient, plain, encouraging. Celebrate small wins. Never make me feel behind.
