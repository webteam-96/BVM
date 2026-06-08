# Bharatiya Vyapar Mahotsav 2026 (BVM) — Web Demo

An interactive **web prototype** of the BVM 2026 trade-fair mobile app — a single, self-contained
HTML file. No build step, no install. Built from a Figma design and enriched with **real data and
real logos** from the official site, [bharatiyavyaparmahotsav.com](https://bharatiyavyaparmahotsav.com/).

> **BVM 2026** — *"Made in India. Made for India. Made for the World."* · The Great Indian Common Market
> 12–15 August 2026 · Bharat Mandapam, Pragati Maidan, New Delhi · Organised by **ITPO + CAIT**

## Run it

Double-click **`index.html`**, or drag it into any modern browser.

> Needs internet: it loads Tailwind, Google Fonts (Rajdhani + DM Sans), Lucide icons, the real BVM
> logo + sponsor/exhibitor logos from bharatiyavyaparmahotsav.com, a live QR (api.qrserver.com),
> and themed photos (LoremFlickr → Picsum fallback). Everything else lives in the one file.

## 12 screens

Splash · Login/OTP · Home (discovery) · **Stall Detail (full exhibitor profile)** · Product Detail ·
Send Enquiry · Saved Confirmation · Saved Stalls · **Zones** · **Scanner** · **Notifications** · **Profile**
— all inside a centered iPhone frame. Bottom nav (Home · Zones · Scanner · Saved · Profile) and the
notification bell are all wired to real screens.

## What's functional

- **OTP login** — tap `Send code` (demo code **4-8-2-9-3-1**), type it (auto-advance), `Verify`. Wrong/short codes shake.
- **Live search** + **17 sector filters** — combine live across 37 exhibitors (e.g. Consumer + "water" → Kent RO).
- **Save / wishlist** — heart any exhibitor → it appears in the data-driven Saved list + Profile count.
- **Scanner** — animated QR viewfinder; **Simulate a Scan** opens a random stall; or type a stall code (e.g. `B2B-A-050`).
- **Zones** — the 8 real BVM zones with live exhibitor counts; tap a sector to jump to a filtered Home.
- **Notifications** — themed alerts with unread states, tap-to-open, and Mark-all-read (updates the bell badge).
- **Profile** — visitor pass with a real scannable QR, saved/enquiry/meeting stats, and a full settings menu.

## Stall Detail = full exhibitor profile

Each exhibitor card opens a complete profile: rating, **business stats** (established, team, exports,
MOQ), **social links**, About, **Products & Catalogue**, **Documents & Downloads**, **Certifications**,
a **Business Details** table (GSTIN, HQ, categories…), **Gallery**, and **Visitor Reviews**.

The **Company Brochure** and **Product Catalogue** generate a real, BVM-branded, **printable document
in a new tab** (save as PDF via the browser print dialog). The **Rate Card** opens the genuine BVM
stall-pricing PDF from the official site.

## Real data baked in (37 participants)

22 real BVM sponsors/exhibitors with their **real hosted logos** (Kent, Uno Minda, Sona Comstar,
Shriram Finance, Signature Global, Urja Global, PC Jeweller, Nutslane, Bossard, Help Us Green,
Dhanuka, Kendriya Bhandar, Galaxy, Porter, Dasnac, Credora, Kuhl, Amore, Bonnaraoo, Inlog, Rajdeep,
Swaastik) + 15 well-known Indian brands for sector diversity, shown as clean monogram tiles
(Fabindia, Raymond, Jaipur Rugs, Channapatna, Patanjali, Dabur, Himalaya, Cipla, Infosys, boAt,
Taj Hotels, Incredible India, Funskool, Titan, Haldiram's). Booth-enquiry contact uses the **real
BVM secretariat** (+91 96677 51132 · contactus@bvm2026.com).

## Customising (all data lives in `index.html`)

- **Add an exhibitor:** push to the `EXHIBITORS` array (use `logo:null` for a monogram tile), add a `META` entry.
- **Add a sector:** add to `SECTORS` (key, label, short, color) — chips, filters and the Zones page update automatically.
- **Swap a photo:** change an `<img class="ph">`'s `data-kw` / `data-seed`.

## Design system (from Figma)

navy `#001454` · accent orange `#a04100` · CTA orange `#fe6b00` · gold `#f5be3c` · 17 sector colors ·
Rajdhani (display) + DM Sans (body). All tokens live in the `tailwind.config` block at the top of `index.html`.
