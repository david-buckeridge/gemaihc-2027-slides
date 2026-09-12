# Session 1 — Generative AI for Public and Population Health

GeMAIHc 2027 short course, Session 1 of 2. Presenter: David Buckeridge.

## Status: first draft, ready for review

46 slides across 7 sections, matching the ~90-minute outline agreed in chat.

## Viewing

This deck fetches its section files at runtime, so it needs an HTTP server, not a plain file:// open:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/`. Arrow keys / space to navigate. `#N` in the URL jumps to slide N; `#llm-foundations`, `#prompt-engineering`, `#rag`, `#beacon`, `#reliability`, `#closing` jump to the start of each section.

## Structure

- `index.html`, `style.css`, `deck.js` — shell and shared visual system
- `sections/00-opening.html` — title + agenda (new)
- `sections/01-llm-foundations.html` — adapted from the AI4PH workshop deck
- `sections/02-prompt-engineering.html` — adapted, trimmed to one worked exercise
- `sections/03-rag.html` — adapted, unchanged from source
- `sections/04-beacon-case-study.html` — new: BEACON outbreak-surveillance case study
- `sections/05-reliability-privacy-bias.html` — adapted; the two Canada-specific slides (Ontario IPC guidance, Canadian FASTER/AIA frameworks) were replaced with internationalized versions for a European/international audience
- `sections/06-closing.html` — discussion + acknowledgments (new)

## Known fix: stale content in Safari

If a slide ever shows partial or missing content in Safari after an edit (e.g. a box with no text, or content cut off partway through a slide), it's Safari's fetch cache, not a file problem: Safari's Cmd+Shift+R reload doesn't reliably clear the cache for the section files this deck loads with `fetch()`, even though it refreshes the page itself. `deck.js` now fetches every section with `{ cache: 'no-store' }`, which stops this from happening going forward. If you still see stale content once, it means a copy from before this fix is cached: open Safari's Develop menu and choose Empty Caches, or open the deck in a Private Browsing window, then reload once.

## What still needs a human pass

- The model-tier comparison slide (`01-llm-foundations.html`, "In practice: Chatbot") names specific model versions (Claude Sonnet 5, GPT-5.6, Gemini 3.1) that will likely be out of date by the 2027 conference. Worth a refresh pass closer to the date.
- The opening slide has a placeholder eyebrow ("GeMAIHc 2027 · Short Course") rather than a specific date/time — fill in once the programme is confirmed.
- Confirm whether the icebreaker ("Chatbot yourself") is worth keeping given the time budget, or should be cut if you need more room elsewhere.

## Attribution

Adapted with permission from the AI4PH workshop deck ("Introduction to Generative AI for Public Health") created by Melissa Ouellet and Yachen Li, July 2026, MIT licensed. See `LICENSE`.
