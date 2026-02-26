# GutCheck TrueOTD

**Conflict-Free Car Buying Intelligence — On the Lot & At Home**

GutCheck TrueOTD is a mobile-first Progressive Web App that delivers instant, conflict-free vehicle purchase analysis. It decodes any VIN, classifies every dealer sticker line item (PAY / NEGOTIATE / REFUSE), applies regional distributor markup intelligence, and produces a true all-in Out-The-Door price with an exact negotiation playbook — in under 10 seconds.

Part of the **GutCheck Financial** ecosystem.

---

## Two Usage Modes

### 📷 On-Lot Mode (Camera)
Open the app on your phone at the dealership. Point at the VIN plate on the dashboard, door jamb, or window sticker. The app captures and OCR-reads the VIN automatically — no typing, no dealer involvement.

### ⌨️ At-Home Mode (Manual Entry)
Enter any VIN from a dealer website, CarGurus listing, or emailed quote. Add MSRP and dealer add-on details from the sticker. Get the full analysis before you ever walk in.

---

## Features

- **VIN Decode** — Live NHTSA vPIC API: year, make, model, trim, engine, drivetrain, assembly plant
- **OTD-First Display** — Target price shown first, prominently
- **Line-Item Classification** — PAY · NEGOTIATE (with % target) · REFUSE (with reason + dealer cost est.)
- **Regional Distributor Intelligence** — Southeast Toyota (SET), Gulf States, JM Family markup libraries built-in
- **State Tax + Tags** — Auto-calculated, all 50 states
- **Negotiation Playbook** — Exact scripts and dollar targets per line item
- **Camera VIN Scan** — Tesseract.js OCR, works on-lot from any phone browser

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML/CSS/JS — no framework, no build step |
| VIN Decode | NHTSA vPIC API — free, no auth required |
| OCR | Tesseract.js v4 — browser-native |
| Hosting | Vercel / GitHub Pages compatible |
| PWA | Mobile-web-app-capable meta tags |

---

## File Structure

```
gutcheck-trueotd/
├── app/
│   └── index.html          # Main application (single file, self-contained)
├── docs/
│   ├── competitive-analysis.html   # Visual competitive benchmarking
│   ├── target-market.html          # Market segments, personas, GTM
│   ├── executive-summary.docx      # Investor executive summary
│   └── business-plan.docx         # Full 2025-2027 business plan
└── README.md
```

---

## Quick Start

### Option 1 — Open directly
Open `app/index.html` in any browser. No server needed for manual VIN entry.

> **Note:** Camera/OCR requires HTTPS. For local development with camera:
> ```bash
> npx serve .
> # then open https://localhost:3000
> ```

### Option 2 — Deploy to Vercel
```bash
npm install -g vercel
vercel --prod
```

### Option 3 — GitHub Pages
Push to GitHub > Settings > Pages > Source: `app/` folder

---

## How It Works

```
User scans VIN (camera) or enters VIN manually
        |
NHTSA vPIC API decodes vehicle (year/make/model/trim/plant)
        |
Sticker line items classified against ADDON_INTEL database
  PAY       -> Factory MSRP, state tax, reg fees
  NEGOTIATE -> Regional add-ons with % discount targets
  REFUSE    -> Junk fees with $0 target
        |
State tax calculated (all 50 states built-in)
Doc fee benchmarked against state market average
        |
TrueOTD Target displayed first, prominently
Negotiation playbook with exact scripts generated
```

---

## API Dependencies

| API | Purpose | Cost | Auth Required |
|-----|---------|------|--------------|
| NHTSA vPIC | VIN decode | Free | None |
| Tesseract.js | OCR / camera scan | Free (CDN) | None |

No API keys required. No backend required. Runs entirely in the browser.

---

## Business Model

| Tier | Price | Features |
|------|-------|---------|
| Free | $0 | 3 VIN scans/month |
| Pro | $9.99/mo | Unlimited scans, dealer comparison, saved reports |
| B2B API | $499-$2,499/mo | White-label for credit unions, fintech, fleet |
| Affiliate | ~$22/user avg | Insurance, warranty, financing referrals |

---

## Competitive Position

GutCheck TrueOTD is the only tool that:
- Leads with the all-in OTD number (competitors bury it)
- Offers on-lot camera VIN scanning from any phone
- Identifies items to REFUSE entirely, not just negotiate
- Contains regional distributor (SET, Gulf States) markup intelligence
- Earns zero dealer advertising revenue — structural trust moat

---

## Roadmap

| Version | Features | Target |
|---------|---------|--------|
| v2.1 (Live) | VIN decode, sticker OTD, PAY/NEG/REFUSE, playbook | Now |
| v3.0 | Enhanced camera OCR, dealer comparison | Q3 2025 |
| v3.5 | Finance/lease analyzer, save and share reports | Q4 2025 |
| v4.0 | Real dealer transaction price feeds | Q1 2026 |
| v4.5 | B2B API, white-label for credit unions | Q2 2026 |
| v5.0 | GutCheck Financial integration — affordability + OTD unified | Q3 2026 |

---

## Legal

GutCheck TrueOTD is a reference tool for consumer education. VIN data sourced from NHTSA public API. Tax rates approximate — verify with your state DMV. Not legal or financial advice.

---

*GutCheck TrueOTD — Part of the GutCheck Financial ecosystem*
