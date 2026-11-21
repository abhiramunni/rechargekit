# RechargeKit — Never Miss a Recharge Again

**Live:** https://abhiramunni.github.io/rechargekit/

Every recharge, every validity date, every rupee — in one calm place. RechargeKit tracks your mobile, broadband and DTH connections so nothing expires on you: validity countdowns, daily-data gauge, a plan finder that ranks plans by rupees per day, and a recharge log that totals what you actually spend.

## What it does

- **My connections** — validity cards with days-left rings and status pills (OK / Due soon / Expired). Tap any card for the full detail sheet: plan, last recharge, valid-till date, recharge history. One tap on "Recharged" rolls the validity forward by the plan's length and logs the payment.
- **Next recharge, ticking** — a live countdown (days / hours / minutes / seconds) to the soonest expiry, with plain-words advice when it is 3 days or fewer away.
- **Today's data** — a gauge for your daily-data plan (seeded: Jio 1.5 GB a day). Log what you have used; the gauge shows what is left and a 7-day chart plots usage against the quota line.
- **Plan finder** — 12 real November 2026 prepaid plans (Jio, Airtel, Vi, BSNL) ranked by **rupees per day**, the honest way to compare a 28-day plan with a 90-day one. Filter by operator, minimum daily data and minimum validity. Prices are indicative — the app says so, and tells you to confirm in the operator's app before paying.
- **Recharge log & spend** — every recharge logged, November spend totalled against an editable monthly budget (ring + plain-words note), plus a per-cycle cost split across mobile / broadband / DTH.
- **Six plain-language guides** — validity vs talktime, the 90-day SIM rule, data rollover, porting, DTH a-la-carte, auto-pay double-charges.
- **Private by design** — no account, no cloud. Everything lives in your browser's localStorage. Copy summary, remove sample data, two-tap erase-all.

## Seed data (removable)

Four sample connections: Jio primary mobile (₹299, 1.5 GB/day, valid till 25 Nov 2026 — 4 days left on 21 Nov), Airtel Xstream Fiber (₹499/mo, renews 1 Dec), Tata Play DTH (₹299/mo, renews 28 Nov), Vi second SIM (₹199, valid till 30 Nov). November spend so far: ₹698 (Vi ₹199 on 3 Nov + Airtel ₹499 on 1 Nov) of a ₹1,500 budget — 47%. Cheapest plan in the finder: BSNL ₹197, 2 GB a day for 70 days — ₹2.81 a day.

## Tech

Single self-contained `index.html` (plus two photos in the repo root, referenced by filename) — no backend, no build step, no sign-up. Fraunces + Inter, warm editorial palette (ivory paper, espresso ink, bronze/amber/terracotta), cinematic signal-bar intro with tap-to-skip, 3-step onboarding tour, Ken Burns photography.

## QA

66/66 headless jsdom assertions pass (`node qa-test.js`), `node --check` clean, zero uncaught JS errors, no pictographic emoji. Hand-verified: validity countdowns (Jio 4d, Tata Play 7d, Vi 9d, Airtel 10d from 21 Nov 2026), per-day prices (BSNL 197 → ₹2.81, Jio 239 → ₹8.54, Jio 899 → ₹9.99, Airtel 979 → ₹11.65), November spend ₹698, mark-as-recharged rolls Jio 25 Nov + 28 days to 23 Dec 2026.

Published in 24 commits on main, all authored by abhiramunni.
