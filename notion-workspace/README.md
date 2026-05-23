# Notion Trading Workspace — Setup Guide

## How to Create Your Notion Workspace (Step-by-Step)

This guide will help you create a professional trading workspace in Notion with:
- A Home Dashboard with clickable links to all pages
- A Calendar-based Trading Journal with image support
- All 6 pages accessible from a sidebar dropdown

---

## STEP 1: Create the Workspace Structure

1. Open Notion
2. In your sidebar, click **"+ Add a page"**
3. Name it: **"Trading System"**
4. This will be your HOME page (Dashboard)

Now create **sub-pages** inside it (these will appear as a dropdown in sidebar):

- Click inside the "Trading System" page
- Type `/page` and create these sub-pages one by one:
  1. **Dashboard** (or use the main page as Dashboard)
  2. **System Rules**
  3. **Pre-Trade Checklist**
  4. **Trading Journal** (this will be a DATABASE - see Step 3)
  5. **Daily Routine**
  6. **Roadmap**

Your sidebar will now show:

```
▼ Trading System
  ├── Dashboard
  ├── System Rules
  ├── Pre-Trade Checklist
  ├── Trading Journal
  ├── Daily Routine
  └── Roadmap
```

---

## STEP 2: Set Up the Dashboard (Home Page)

Copy and paste the content from `00-DASHBOARD.md` into your main page.

**To make clickable links to sub-pages:**
1. Type `@` then start typing the page name (e.g., @System Rules)
2. Click the page from the dropdown
3. This creates a clickable link that takes you to that page
4. Do this for all 6 pages

**Pro tip:** Use Notion's "Link to page" block:
- Type `/link` → select "Link to page" → choose your sub-page
- This creates a nice card-style link

---

## STEP 3: Create the Trading Journal as a DATABASE (Calendar View)

This is the most important step. The journal needs to be a **Notion Database** so you get:
- Calendar view (see trades by day)
- Add button on each day
- Image attachments
- Filters and sorting

### How to create it:

1. Go to your **Trading Journal** sub-page
2. Delete any content in it
3. Type `/database` → select **"Database - Full page"**
4. Or type `/calendar` → select **"Calendar view"**

### Set up these DATABASE PROPERTIES (columns):

| Property Name | Type | Options |
|---|---|---|
| Trade # | Title (default) | Auto-number your trades |
| Date | Date | The trade date |
| Pair | Select | XAUUSD, NAS100, EURUSD |
| Direction | Select | LONG, SHORT |
| Session | Select | London, New York |
| Result | Select | +1R, +2R, +3R, BE, -1R |
| P&L ($) | Number | Dollar amount |
| R:R Achieved | Number | e.g., 2.0 |
| Followed Rules? | Checkbox | Yes/No |
| Grade | Select | A, B, C, D |
| Emotion Before | Select | Calm, Anxious, FOMO, Revenge, Bored |
| Emotion During | Select | Calm, Anxious, Wanted to close, Wanted to move SL |
| HTF Bias | Select | Bullish, Bearish |
| Entry Price | Number | |
| Stop Loss | Number | |
| Take Profit | Number | |
| Lot Size | Number | |
| HTF Screenshot | Files & media | Upload H4/H1 chart |
| Entry TF Screenshot | Files & media | Upload M5/M15 entry |
| Before Entry | Files & media | Upload chart before entry |
| After Entry | Files & media | Upload chart after entry |
| Notes | Text | Any additional notes |
| Rules Broken | Text | Which rule if any |

### Set up VIEWS:

1. **Calendar View** (default) — shows trades on each day
   - Click "+ Add a view" → "Calendar"
   - Set the date property as the calendar date

2. **Table View** — for detailed data review
   - Click "+ Add a view" → "Table"

3. **Gallery View** — to see chart screenshots
   - Click "+ Add a view" → "Gallery"
   - Set card preview to "HTF Screenshot"

### How the Calendar Works:

- You'll see a monthly calendar
- Each day has a **"+"** button to add a new trade
- Click any day → "New" → fills in the date automatically
- Click an existing trade to open it and see all details + images
- Upload screenshots directly into the Files & media properties

---

## STEP 4: Import the Other Pages

For each remaining page, copy the markdown content:

| Page | File to Copy From |
|---|---|
| System Rules | `01-SYSTEM-RULES.md` |
| Pre-Trade Checklist | `02-PRE-TRADE-CHECKLIST.md` |
| Daily Routine | `03-DAILY-ROUTINE.md` |
| Roadmap | `04-ROADMAP.md` |

**How to import:**
1. Open the sub-page in Notion
2. Click `...` (top right) → Import → Markdown
3. Select the .md file
4. OR just copy-paste the raw markdown content directly

---

## STEP 5: Add Navigation (Back to Home)

On every sub-page, add a "Back to Dashboard" link at the top:

1. At the top of each page, type: `← Back to Dashboard`
2. Select "← Back to" text → make it a link → link to your Dashboard page
3. OR type `@Dashboard` to create a mention link

**Even easier:** Notion's breadcrumb navigation at the top already shows:
```
Trading System > System Rules
```
Click "Trading System" to go back to home.

---

## STEP 6: Template for New Journal Entries

Create a template so every new trade has the same format:

1. In your Journal database, click the dropdown arrow next to "New"
2. Click "+ New template"
3. Name it: "New Trade Entry"
4. Pre-fill:
   - Risk: 0.5%
   - Set default selects if you want
5. In the template body, add:

```
## Trade Analysis

### Setup:
- HTF Bias:
- Key Zone:
- Liquidity Sweep:
- BOS Confirmed:

### Execution:
- Entry reasoning:
- What I did well:
- What I could improve:

### Screenshots:
(attach below)
```

Now every time you click "+" on a calendar day, it uses this template!

---

## FINAL RESULT:

Your workspace will look like this:

```
🏠 TRADING SYSTEM (Home/Dashboard)
│
├── 📊 Quick Stats widget
├── 🪞 Identity Statement
├── 💎 Daily Reminders
├── 🔗 CLICKABLE LINKS:
│   ├── → System Rules
│   ├── → Pre-Trade Checklist
│   ├── → Trading Journal (Calendar)
│   ├── → Daily Routine
│   └── → Roadmap
│
├── 📋 System Rules (sub-page)
│   └── Complete 7-rule playbook
│
├── ✅ Pre-Trade Checklist (sub-page)
│   └── Mental check + 7 rules + decision tree
│
├── 📓 Trading Journal (DATABASE)
│   ├── 📅 Calendar View (default)
│   ├── 📊 Table View
│   ├── 🖼️ Gallery View (screenshots)
│   └── Each entry has:
│       ├── Result (+1R, +2R, BE, -1R, etc.)
│       ├── HTF Screenshot
│       ├── Entry TF Screenshot
│       ├── Before Entry image
│       └── After Entry image
│
├── 🕐 Daily Routine (sub-page)
│   └── Morning → Sessions → Shutdown
│
└── 🗺️ Roadmap (sub-page)
    └── 5-phase plan with progress tracking
```

---

## BONUS TIPS:

1. **Pin your Dashboard** to Notion's favorites (star icon) for quick access
2. **Use Notion's sidebar toggle** (◀) to collapse/expand your trading pages
3. **Set Calendar as default view** on your journal so you always land on it
4. **Add icons** to each page (click the icon area):
   - 🏠 Dashboard
   - 📋 System Rules
   - ✅ Pre-Trade Checklist
   - 📓 Trading Journal
   - 🕐 Daily Routine
   - 🗺️ Roadmap
5. **Use covers** — add a trading-related image as cover for each page

---

## Need Help?

If you get stuck on any step, screenshot your Notion and send it to me.
I'll guide you through it.

Good luck. Now go build it and start executing. 🎯
