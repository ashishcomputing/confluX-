# ConfluX+

**Advanced ICT + SMC + XAI Confluence Indicator for TradingView**

*by ASHFX*

ConfluX+ is a comprehensive, highly customizable Pine Script v5 indicator designed for traders who follow **Smart Money Concepts (SMC)**, **ICT (Inner Circle Trader)** methodologies, and custom confluence logic (X1_AI).

It provides deep insight into market structure, liquidity, order flow imbalances, and institutional order blocks in real time — with both swing and internal (lower-timeframe) perspectives.

---

## ✨ Key Features

### Smart Money Concepts & Market Structure
- **Swing Structure** (BOS & CHoCH) with full bullish/bearish controls
- **Internal (Real-time) Structure** for lower-timeframe confluences
- Historical or Present-only display modes
- Optional confluence filter for internal breaks

### Order Blocks
- **Internal Order Blocks** (up to 20 displayed)
- **Swing Order Blocks**
- Configurable mitigation (Close or High/Low)
- Volatility filtering (ATR or Cumulative Mean Range)
- Color-coded and transparent boxes

**Volumetric Order Blocks (v1.1 refinement)**:
- Integrated directly into the main `ConfluX+.pine` (and `ConfluX+ v1.1.pine`): volumetric volume data (total + bull/bear split calculated over the formation range), displayed inside the OB boxes with percentages, [BREAKER] and [COMBINED] tags.
- Built from the Flux Charts volumetric base you shared + optimizations from the original ConfluX+ OB logic (range-based best-candle selection, ATR/range filter, proper mitigation alerts, drawing object management to prevent clutter).

### Fair Value Gaps (FVG)
- Bullish and bearish FVGs
- Auto or manual threshold filtering
- Multi-timeframe support
- Extendable boxes

### Equal Highs / Equal Lows (EQH / EQL)
- Detects significant equal highs and lows
- Adjustable confirmation length and sensitivity threshold

### Premium / Discount / Equilibrium Zones
- Dynamic zones based on trailing swing extremes
- Premium (above), Discount (below), and Equilibrium (50% level)

### Additional Tools
- Multi-Timeframe Highs & Lows (Daily / Weekly / Monthly levels)
- Strong / Weak High & Low labels (trailing extremes)
- Trend-colored candles (optional)
- Swing point labels (HH, HL, LH, LL)
- 15+ built-in **alert conditions**

### Styling & Usability
- Colored or Monochrome themes
- Highly granular input groups with tooltips
- Max labels/lines/boxes increased for heavy chart usage

---

## 📦 Installation

### Method 1: Pine Editor (Recommended for latest version)

1. Open TradingView and navigate to any chart.
2. Click **Pine Editor** (bottom panel).
3. Remove the default code.
4. Open the file `ConfluX+.pine` from this repository.
5. Copy **all** of its content.
6. Paste into the Pine Editor.
7. Click **Add to chart** (or `Ctrl+S` / `Cmd+S`).

### Method 2: From this GitHub repo
- Always grab the latest `ConfluX+.pine` from the `main` branch.

> **Note:** This indicator is **not** (yet) published as a public TradingView script. Using the Pine Editor method gives you the most up-to-date version with any fixes or enhancements.

---

## ⚙️ Settings Overview

The indicator is organized into clear input groups:

| Group                        | Purpose |
|-----------------------------|---------|
| **Smart Money Concepts**    | Mode (Historical/Present), Style (Colored/Mono), Color Candles |
| **Real Time Internal Structure** | Toggle internals, BOS/CHoCH filters, colors, confluence filter, label size |
| **Real Time Swing Structure** | Swing BOS/CHoCH, swing points, strong/weak highs & lows |
| **Order Blocks**            | Internal + Swing OBs, count, filter method, mitigation type, colors |
| **EQH/EQL**                 | Equal highs/lows detection with length + threshold |
| **Fair Value Gaps**         | Enable FVGs, auto threshold, custom timeframe, extend, colors |
| **Highs & Lows MTF**        | Daily/Weekly/Monthly levels with line styles |
| **Premium & Discount Zones**| Visual premium/discount/equilibrium zones |

All settings include detailed tooltips directly in TradingView.

**Pro tip:** Start with defaults, then enable features one group at a time (e.g. first Structure + Order Blocks, then add FVGs).

---

## 🔔 Alerts

ConfluX+ exposes the following `alertcondition`s (use TradingView's alert creation dialog):

- Internal Bullish / Bearish BOS
- Internal Bullish / Bearish CHoCH
- Bullish / Bearish BOS (swing)
- Bullish / Bearish CHoCH (swing)
- Bullish / Bearish Internal OB Breakout
- Bullish / Bearish Swing OB Breakout
- Equal Highs / Equal Lows
- Bullish FVG / Bearish FVG

You can create separate alerts for each or combine them using the alert dialog conditions.

---

## 🖼️ Screenshots

_Add your own chart screenshots here showing the indicator in action (structure, OBs, FVGs, zones, etc.)._

Example ideas:
- EURUSD with full confluences
- Strong structure shift + OB + FVG alignment
- Premium zone rejection

---

## 📜 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

You are free to use, modify, and share the indicator for personal or commercial trading systems, as long as the original copyright notice is preserved.

---

## ⚠️ Disclaimer

This indicator is provided for **educational and informational purposes only**.

- Trading involves substantial risk of loss.
- Past performance is not indicative of future results.
- This tool does **not** constitute financial, investment, or trading advice.
- Always backtest thoroughly and use proper risk management.

The author (ASHFX) and contributors are not responsible for any financial losses incurred while using this indicator.

---

## 🙏 Credits & Inspiration

- **ASHFX** — Original concept, development, and X1_AI confluences
- **ICT (Inner Circle Trader)** methodology
- **Smart Money Concepts (SMC)** community
- TradingView Pine Script team for the powerful scripting environment

Special thanks to all traders who share knowledge openly in the ICT/SMC space.

---

## 🔗 Repository & Versioning

https://github.com/ashishcomputing/confluX-

**File naming policy (per your instructions):**
- Main working file always stays **ConfluX+.pine** (the original name).
- Refinements are versioned as **ConfluX+ v1.0.pine**, **ConfluX+ v1.1.pine**, etc.
- We learn from every code you share (e.g. the volumetric Order Blocks script) and integrate/refine the relevant parts (especially OBs in this v1.1) without creating unrelated new names.

**v1.1 highlights (OB-focused optimization):**
- Full crosscheck and syntax cleanup completed (no remaining errors found: all := tuple issues inside UDFs resolved with proper local temp pattern, string literals fixed, UDT fields consistent, function calls aligned, etc.).
- Volumetric OBs integrated as described above.
- All prior refinements (Present mode default, MTF levels limited to Daily, structure line management, etc.) preserved.

---

## 📦 Published / Project Closed

**Status: Published at v1.1 (final clean version)**

- Main file: `ConfluX+.pine`
- Versioned release: `ConfluX+ v1.1.pine` (recommended for use; includes all optimizations and the volumetric Order Block enhancements).
- History snapshot: `ConfluX+ v1.0.pine`

**Raw download links (for Pine Editor):**
- Latest: https://raw.githubusercontent.com/ashishcomputing/confluX-/main/ConfluX+.pine
- v1.1: https://raw.githubusercontent.com/ashishcomputing/confluX-/main/ConfluX%20v1.1.pine

The project is now closed. All codes have been crosschecked for syntax and logical issues (no further errors detected in the final pass). Future tweaks can start a v1.2 branch if needed.

Thank you for the iterative refinements — the indicator now has robust, volumized Order Blocks while staying true to the original ConfluX+ design.

---

**ConfluX+** — Clarity through confluence.

*Built for serious structure traders.*
