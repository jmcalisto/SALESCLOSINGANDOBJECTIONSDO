# Jill's Solution & Closing — Role-play

A single self-contained HTML training activity (the "Solution, Closing & Objections — Do section"
role-play) for Wall Street English sales training. No build step, no dependencies beyond Google
Fonts — open `jills_solution_and_closing.html` directly in a browser to preview or deliver it.

## What it is

A photo-based consultation role-play that picks up where the Needs Analysis ends: Jill (the
prospective student) has shared her situation, and the learner — playing the consultant — must
present the solution, state the investment, and close. At each of the seven phases the learner
picks a response and watches a "warmth" relationship meter react to the choice. It ends with a
recap/transcript screen and a completion code.

The seven phases follow the closing sequence taught in the module:

1. Say it back (partial close)
2. Give a choice (two options)
3. Present the price (and stay quiet)
4. The guarantee
5. Ask to start (alternative close)
6. Treat the objection (Three Magic Steps)
7. Buying signal

## Localization

Everything a learner sees lives in two JavaScript objects near the top of the `<script>` block:

- `UI` — interface labels, phase names, buttons, and the recap bullets
- `SCENARIO` — the conversation itself, as an ordered array of phases, each with its lines,
  situation text, prompt, teaching tag, and multiple-choice options with feedback

To produce a new language version, translate the string values inside these two objects and
re-host the file. Nothing else needs to change.

Each spoken line also has an `audio` field (an id such as `j0` / `y2`). Point it at a path such as
`audio/en/j0.mp3` to auto-play a per-language ElevenLabs voice clip for that line; leaving the
audio unwired keeps the activity text-only.

## Design system

This activity follows the shared "Do section" visual/interaction style used across Wall Street
English sales training activities (see the companion style-guide repo for the full design
tokens, component inventory, and a blank template for building new activities in the same
style). It is the direct counterpart to the "Show section" comic in the
`SALESCLOSINGANDOBJECTIONSSHOW` repo.
