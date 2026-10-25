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

## What we're building (v1 — DRAFT SCOPE, confirm with me before locking)
An AI "what should I cook" app for people staring at their fridge/pantry with no plan.
1. User types what they have or feel like eating in plain language
   (e.g. "chicken thighs, half a bag of spinach, and I'm tired")
2. App suggests a short list of meals to cook — the AI SELECTS from a curated
   recipe library file. It must NEVER free-generate a recipe outside that
   library. This is a core safety + evaluability decision (same reasoning as
   the exercise library in the fitness coach project).
3. User marks what they actually cooked, saved permanently
4. App gives variety nudges based on cooking history
   (e.g. "you've made this 3 times this month — here's something different
   using similar ingredients")
5. Every suggested recipe shows a short plain-language "why this fits" and
   links to the full recipe/instructions

## Explicitly OUT of v1 scope — refuse and remind me if I ask mid-build
- Grocery delivery / ordering integrations
- Calorie or nutrition tracking
- Photo-based ingredient recognition (snap a pic of your fridge)
- Auto-generated grocery lists (v2 — parked deliberately)
- Full weekly meal planning calendar (v2)
- Social features (sharing, following, ratings from other users)
If I ask for any of these, remind me it's parked in the v2 list and ask if I
really want to reopen scope. Default answer is no.

## Technical ground rules
- Web app. Start with the simplest thing that works (plain HTML/CSS/JS is fine
  to begin). Do not introduce a framework, database, or service without first
  explaining what it is, why now, and what the alternative was — then wait for
  my go-ahead.
- The recipe library is a structured data file (e.g. JSON) checked into the
  repo. It is reviewed by a human (me) before the app uses it.
- AI calls must be constrained to selecting from the library. Prompt design
  should make it structurally hard for the model to invent recipes.
- Keep secrets (API keys) out of committed code. Explain what an environment
  variable is the first time we need one.

## Habits to enforce every session
- Commit after every real chunk of progress with a clear message. No giant
  end-of-day commits. Tell me what you're committing and why.
- Maintain a file called TRADEOFFS.md in the repo root. Every time we make a
  meaningful choice (library vs free generation, framework or not, data shape,
  model choice), append one line: what we picked, over what, and why. This file
  becomes the "Tradeoffs" section of the README later — the most important
  section for my goals.
- The README is built incrementally, not at the end. Structure:
  Problem · Solution & how it works · Tradeoffs considered · Evals · What I
  learned / what broke / what's next.

## Evals matter here
Later steps include a real eval pass: generating several suggestion outputs,
labeling them good/bad against simple criteria, fixing the top failure mode,
re-measuring. Build with this in mind — outputs should be easy to capture and
compare.

## Tone
Patient, plain, encouraging. Celebrate small wins. Never make me feel behind.
