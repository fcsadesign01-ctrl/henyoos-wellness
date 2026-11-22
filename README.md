# henyoOS · Wellness & Spa — UI/UX

Planning and design work for the **Wellness & Spa (WLN)** vertical of henyoOS: the operating system for spas and wellness centres (booking, checkout, memberships, payroll, inventory, marketing, SMS, reports).

Live canvas: [Spa & Wellness Platform – Map & Storyboard](https://claude.ai/artifact/DJ8tavswdP6NKCuuE953Kx)

## Status (paused 22 Nov 2026)

| Step | What | Status |
|---|---|---|
| 1 · Map | Overview, site map (10 modules), build phases | Done |
| 2 · Moodboard | Hierarchy rule + 5 directions | Done, **Direction E (henyoOS Wellness purple)** chosen |
| 3 · Storyboard, part 1 | Staff web: daily loop (7 screens) | Done |
| 3 · Storyboard, guest booking | Mobile web: 6 screens + flow map | Done |
| 3 · Storyboard, next | Provider mobile app; manager screens; dark theme set; flows frame by frame | To do |
| 4 · Build | Clickable hi-fi prototype: staff daily loop + guest booking | Round 1 done (`prototype/`) |

## Try the prototype

`prototype/index.html` is a self-contained clickable prototype (one file, no build step). Open it in any browser, or turn on GitHub Pages for this repo (Settings › Pages › Deploy from branch › `main` / root) and visit `/prototype/`.

- **Start page:** pick the staff app (desktop/tablet) or guest booking (phone). It also has a list of things for testers to try.
- **Staff app:** appointment book (click an empty spot to book, click a block for actions), new appointment panel, take payment (tips, tenders, retail with Sale by), checkout list, invoices with reopen (auto-backdate) and refund, guest profiles, membership sale (its own invoice), alalAI panel, country switch (UAE AED / Philippines PHP / Saudi SAR), light and dark themes.
- **Guest booking:** spa home → service → who & when → details (phone first, intro price) → hold with card → booked. The booking appears on the staff book as "Online".
- Sample data only, saved in the browser's local storage; "Reset demo" starts over. Demo clock is fixed at 12:40 on Sun 22 Nov 2026. No real payments; only the last 4 digits of a typed card are kept.
- Not built yet: provider mobile app, manager screens (payroll, inventory, marketing, reports, setup), SMS inbox.

## Decisions so far

- **Product:** a platform for many spas (white-label), part of henyoOS. Product name in screens stays `[PRODUCT NAME]` / `[SPA NAME]` placeholders for now.
- **Surfaces:** staff web app (front desk + back office), provider mobile app, guest booking.
- **Deliverable:** clickable hi-fi prototype.
- **Locale:** English, Arabic-ready (RTL later). **Currency follows each center's country** (UAE · AED · +971 shown in mocks).
- **Look:** minimalist, hierarchy first (the pyramid): one focal point, one purple primary button, three text sizes, color only for status. Light and dark themes.
- **Theme:** henyoOS launcher frame (logo, navy #0B1220, background #F5F8FC, Plus Jakarta Sans) + Wellness tile purple **#7C3AED** as the single accent; buttons are purple. Dark accent #B794F6.
- **alalAI** lives inside Wellness & Spa (Operations / Guidance / Learning).
- **Guest booking:** spa's own brand ("Powered by henyoOS" footer), mobile web link, service first, card held but nothing charged (pay at spa), 50% late-cancel / no-show fee.

## Open items

- Real plan names and prices (Essential / Monthly Glow / Household are placeholders).
- Cancellation window (assumed 2 h before) and fee %.
- Member sign-in for guest booking (proposed: SMS one-time code).
- Therapist photos and specialties in guest booking.

## Files

`design/` holds the canvas source. Each `*.dc.html` is one artboard written for the Claude Design canvas (it loads the canvas's `support.js`, so open it through the canvas link above rather than directly in a browser). `canvas.json` is the board layout.

| File | Board |
|---|---|
| Main, Sitemap, Phases | 01 · Map |
| Principles, MoodA–MoodE | 02 · Moodboard |
| Book, NewAppt, Guest, Pay, Invoice, Alal, Membership | 03 · Storyboard, staff daily loop |
| GFlow, G1Home … G6Booked | 04 · Guest booking |

Source requirements: *Salon & Spa Management Platform — Product & Developer Guide* (kept out of this repo).
