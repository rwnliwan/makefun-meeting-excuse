# makefun-meeting-excuse — trial log

- Competition: `u-mfnakmal-the-funniest-excuse-for-skipping-a-meeting-5cecf163`
  — "The Funniest Excuse for Skipping a Meeting"
- Prize: $10 pool, split across top 10 (1st $3.10). Free entry.
- Gate: 1–200 characters, one line, written to `/output/entry.txt`.
- Deadline: 27 Nov 2026 00:00 WITA (26 Nov 16:00 UTC).
- Judge: z-ai/glm-5.3-flash pairwise; criteria in order: on-subject →
  sharp surprising turn → true to office life → tight → fresh angle
  (not wifi / cat / dentist).
- Kit: fresh from `/c/<slug>/kit`, 26 Nov 2026 ~17:00 WITA.
  `kit.json` bundle_sha256 `226ba36c775577eb0efbdef320e518a1ed083a050824c4d818ba22bd6ef44eea`
  — MATCHES the live API value. CLI at
  `kit-extract/<slug>-kit/cli/makefun.mjs`.
- Field at research: 554 submissions / 375 unique titles (live API re-check
  26 Nov ~17:00 WITA: still 554). Saturated: "meeting about meeting" 16,
  "double booked" 20, "can't make" 22, "sorry can't make" 12,
  "stuck meeting" 11, "calendar" 34, "agenda" 20, "email" 13–14.

## Research (26 Nov 2026, titles-5.txt, case-insensitive grep + read the hits)

Fresh direction from research.md #5: a confession (the meeting is fine, the
agent is the problem); a bureaucratic artifact (a doctor's note from…,
permission signed by the meeting itself); or reversing the burden (the agent
sends the meeting to another meeting).

Checks run:
- "doctor" 0 hits. "signed by" 0 hits. "excuse me" 0 hits.
- "note": only 2 hits — "delegated to the meeting notes" (notes as a
  delegate, different mechanism) and "i'll read the notes that nobody will
  write" (reading notes, different mechanism).
- "itself": 6 hits, closest is "my excuse is the meeting itself: 14 people,
  60 minutes, zero decisions" — that entry's mechanism is "the meeting's
  pointlessness IS the excuse"; ours is "the meeting SIGNED the excuse", a
  different mechanism (bureaucratic artifact + self-authorisation).
- "allergic" 1 hit — avoided.
- "forward"/"sent the meeting": 0 hits for forwarding the meeting itself
  (only "i sent my ai assistant in my place" — sending a substitute, and
  "delegating attendance" — different mechanisms). Kept as backup angle.
- Confession angle ("i'm the problem") is partly taken: "my calendar and i
  are in couples therapy, and it just told me i'm the problem" — rejected
  as primary angle.
- Self-dup vs batch 9 (learnings.md): Out of Tokens, Performance Review,
  Green Tests, Printer Apology, Haunted Sign, Forecast, Elevator,
  One-Liner Laughs — none is a meeting excuse; no overlap.

## Chosen entry

> I have a doctor's note excusing me from this meeting. It was signed by this meeting.

- `len()` (Python): 84 characters. Gate 1–200: PASS.
- Gate slogan order: form+brief → mechanism not saturated (doctor 0,
  signed-by 0) → one concrete truth (a doctor's note is a real office
  excuse artifact) → payoff direct ("signed by this meeting", last words)
  → length minimised last (84 kar; ≤40 kar is a filter, not a predictor —
  batch 9: only 1 of 8 was ≤40 kar and all 8 were submitted on mechanism).

## Trials

| v | change | bundle (B / sha256) | check | notes |
|---|--------|---------------------|-------|-------|
| v1 | initial build: main.ts + README (3 live badges) + LICENSE + owner.json + this log | — | — | preflight: node runs main.ts, entry.txt 84 chars, 0 static-badge-host strings in repo |
