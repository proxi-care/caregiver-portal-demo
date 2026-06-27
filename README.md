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

## Navigation (shallow — 4 hubs + back)
**Home · Calls · Memory · Settings** bottom bar; everything is one or two taps from a hub,
always with a back arrow. No 14-item operator rail.

## Coverage — every apps/UX task (POR.1–POR.16) in caregiver language
| Task | System feature | In the demo (caregiver lens) |
|---|---|---|
| **POR.13** | Dashboard | Home **"Is everything okay?"** verdict (calm / one-thing) |
| **POR.11** | Escalation triage | **"Tough moments"** → story + **"Listen to this moment"** + Mark reviewed / This was fine |
| **POR.5** | Alerts config | **Alerts** — sensitivity presets, who's told (test buttons), channels + quiet hours, "emergencies always reach everyone" |
| **POR.6** | History + skim | **Recent calls** → narrative + affect tags → call detail with **chapters / jump-to / speed** + drop+callback shown as one |
| **POR.14** | Recordings | **Recordings** — per-call, audio loads only on play |
| **POR.8** | Outbound CTAs | **Call Mom now / Start the call / Just listen in** (rings you first) |
| **(copilot)** | Live steering | **Live call** — listen · gentle nudge · speak in your voice |
| **Digest** | KB candidates | **For your review** — one card, *Add / Skip / Not true*, `1 of 3` |
| **POR.4** | Interview | **Fill a gap together** — voice-first, one question, progress ring |
| **POR.7** | Voice-memo + sandbox | 🎙️ **FAB** (record → confirm) + **"Try a practice run"** sandbox |
| **POR.9** | Voice / corpus | **Voice & how ready** — quality ring, clone status, third-party acceptance, coverage bars |
| **POR.10** | Prompt sections | **How the twin talks** — sections + diff + **version history / roll back**, required change-note |
| **POR.12** | Tuning | **How it handles things** — check-in words, name pronunciations, gentle responses |
| **POR.2** | Forwarding | **Phone forwarding** — carrier, tap-to-dial activation, test, pause, "call me for help" |
| **POR.3** | Consent | **What you've allowed** — granular toggles with plain consequences |
| **POR.1** | Onboarding / readiness | **Is the twin ready?** — % + go-live checklist |
| **POR.15** | Persona switcher | **Switch patient** — only the chosen one shows |
| **POR.16** | Termination | **Leave the program** — gentle 3-step walkthrough, nothing deleted without confirm |
| — | Memory book / Promises / Routines | plain sections + add |

Tap the `demo ⚙` chip to flip calm/attention or jump straight to any management screen.

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
