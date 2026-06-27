# Caregiver Portal — UX demo (Portal B · the family lens)

A self-contained, **mobile-first** clickable demo of the caregiver portal designed for the
**50/60+ family caregiver** — calm, plain-language, one-thing-at-a-time. It's the *family*
answer to "is everything okay?", not the operator console.

> **Two users, two lenses (don't merge them).** The dense s2 portal we have today is the
> **monitor console** — for a trained/paid operator doing live-call steering and gate
> decisions (raw counts, verbatim transcripts, Nudge/Steer/Conference). **This demo is the
> caregiver portal** — the default for Dad's daughter. Same events, two lenses: the operator
> sees "DISTRESS intent detected → decide"; the family sees "one tough moment near the end,
> we handled it."

## View it
No build, no server, no network — just open the file:
```
open demos/caregiver-portal/index.html      # or double-click it
# or: python3 -m http.server -d demos/caregiver-portal 8080  → http://localhost:8080
```
All data is **mock** (patient "Mom" / twin "Alex"). Tap the **`demo ⚙`** chip (bottom-right) to
flip between **"a tough moment happened"** and **"a calm day"**, or jump to any screen.

## What it demonstrates (our main features, in caregiver language)
| Feature (system) | Here (caregiver lens) |
|---|---|
| Home / dashboard | **"Is everything okay?"** verdict — one glance, calm or "one thing to look at" |
| Escalation / safety | **"A tough moment this morning"** → story + **"Listen to this moment"** (snippet, not the whole call) + one action + "Adjust the twin" |
| Digest / KB candidates | **"For your review"** — one card at a time, *Add / Skip / Not true*, progress `1 of 3` |
| Call history | **"Recent calls"** — narrative summaries + affect tags (calm / bright / tough) |
| Memory book (KB) | plain sections + **"Add a memory — just talk"** |
| Interview (corpus) | **"Fill a gap together"** — voice-first, one question, no right words needed |
| Tuning / prompt | folded into **"Adjust the twin"** on the moment that prompted it |
| Account / consent / forwarding | plain "how calls reach Mom" + "what you've allowed" + gentle exit |

## The principles it embodies
1. **One glance answers "is everything okay?"** — a verdict, not two alarming numbers.
2. **Important now, not everything** — the system did the triage (one hero + ≤4 rows; no 221-queue).
3. **Plain human language** — "Mom seemed unsure whether she'd eaten," never "DISTRESS intent detected."
4. **Shallow, linear navigation** — Home → card → moment → back; one axis, always a back arrow, 3-item bottom bar.
5. **Large targets, high contrast, space** — full-width cards/buttons (54px+), big serif headers, single column.
6. **Error-tolerant & reassuring** — "always growing, never 'done'. You're doing enough." (vs a debt of "67% / 221").
7. **Voice as a first-class input** — "answer however you like."
8. **The system carries the memory** — affect-tagged calls, resumable state; the caregiver never reconstructs context.

## Accessibility baked in
Semantic `<button>` controls (not clickable divs) · full keyboard path + visible focus · color **+ words**
(never color alone) · `aria-live` verdict · `role="switch"` consents · `rem`-based type that respects OS
text-scaling · `prefers-reduced-motion` honored · large tap targets.

_Demo authored 2026-06-27 from the caregiver-portal UX principles. Not production code._
