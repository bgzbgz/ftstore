# Market Size Tool - User Guide

## 🚀 Quick Start

1. **Open the file**: Double-click `market-size-tool.html`
2. The tool works entirely in your browser - no installation needed
3. All data is stored locally (localStorage)

---

## ✨ Features Implemented

### 8-Point Tool Criteria ✓

1. **Forces a final clear decision** ✓
   - Produces concrete market size and 3-year forecast numbers

2. **Zero questions needed** ✓
   - Self-explanatory interface with WHY/WHAT/HOW context always visible
   - Inline hints and validation messages

3. **Extremely easy first steps** ✓
   - Start with just 4 simple inputs
   - Real-time validation with helpful error messages

4. **Instant feedback** ✓
   - Live calculations as you type
   - Input fields turn black border on focus
   - Validation messages appear immediately

5. **Gamification elements** ✓
   - Progress dots showing journey (3 steps)
   - Animated transitions
   - Top forces ranking system with "FOCUS" badges
   - Score calculations visible in real-time

6. **Crystal clear results** ✓
   - Visual comparison cards (Current vs. Future)
   - Summary dashboard with all key metrics
   - Growth percentages highlighted

7. **Public commitment** ✓
   - "Share with Team" button (ready for webhook integration)
   - PDF export via browser print function

8. **Smells like Fast Track** ✓
   - Plaak font for headings, Riforma for body
   - Black/white/grey color palette
   - Numbered sections with black background
   - WHY/WHAT/HOW sidebar structure

---

## 🎨 Design System Compliance

### Typography
- ✅ Plaak (Bold) for all headings
- ✅ Riforma (Regular) for body text
- ✅ 36px for WHY/WHAT/HOW
- ✅ 18px for section numbers

### Colors
- ✅ #FFFFFF (White background)
- ✅ #000000 (Black text/accents)
- ✅ #E0E0E0 (Grey borders)
- ✅ #F8F8F8 (Context boxes)

### Components
- ✅ Numbered sections with black background
- ✅ Context boxes with 4px black left border
- ✅ Input fields with border transition on focus
- ✅ Primary/secondary button styles
- ✅ 0.2s ease transitions throughout

---

## 📊 How It Works

### Step 1: Market Size Available
**Inputs:**
- Total Number of Customers
- Average Spending per Customer (€)
- Average Purchases per Year
- Gross Profit Margin (%)

**Outputs:**
- Market Size = Customers × Spending × Purchases
- Profit Pool = Market Size × Margin

### Step 2: Driving Forces Brainstorm
**Process:**
- Add unlimited driving forces
- Rate each force: Impact (1-5) and Probability (1-5)
- Score auto-calculated: **(2 × Impact) + Probability**
- Forces auto-ranked by score
- Top 7 marked as "FOCUS"

**Why 2× Impact?**
High-impact events require strategic preparation regardless of probability.

### Step 3: Future Impact Analysis
**Input Matrix:**
- Estimate % change for each top force across 4 variables:
  - Total Customers (%)
  - Average Spending (%)
  - Purchases per Year (%)
  - Gross Margin (percentage points)

**Calculations:**
```
Future Customers = Current × (1 + ΣCustomer%)
Future Market = Current Market × (1 + ΣCustomer%) × (1 + ΣSpending%) × (1 + ΣPurchases%)
Future Margin = Current Margin + ΣMargin (in percentage points)
Future Profit Pool = Future Market × Future Margin
```

**Why Multiply?**
Growth factors compound! 10% customer growth + 10% spending growth = 21% market growth (not 20%).

---

## 🎯 Key Features

### Progressive Disclosure
- Steps unlock sequentially
- Can't proceed until current step is complete
- Back buttons allow editing previous steps

### Live Validation
- Red error messages for incomplete data
- Disabled "Next" buttons until criteria met
- Inline guidance text under each input

### Worksheet-Style Layout
- Left sidebar: WHY/WHAT/HOW context (always visible)
- Main area: Inputs and calculations
- Designed for team collaboration (not solo survey)

### Visual Feedback
- Progress indicator shows current step
- Animated transitions between views
- Hover effects on interactive elements
- Score calculations update in real-time

### Auto-Ranking
- Forces automatically sorted by score
- Top 7 highlighted with "FOCUS" badge
- Only top 7 flow into impact analysis

---

## 💾 Data Persistence

Currently uses browser `localStorage`:
- Data persists across page refreshes
- Private to your browser
- No server connection needed

**For Production:**
Replace the `Share with Team` button logic with your webhook integration (n8n, Zapier, etc.)

---

## 🖨️ Export Options

### PDF Export
Click "Export PDF" or use browser print (Ctrl/Cmd + P):
- Clean layout optimized for printing
- Navigation buttons hidden
- Ready for team distribution

### Future Integration
The tool is ready for:
- Webhook submissions (n8n)
- Database storage
- Team collaboration features
- Email distribution

---

## 🔧 Customization

### Change Currency
Line 198: Modify `formatCurrency` function
```javascript
const formatCurrency = (value, currency = '$') => {
```

### Adjust Top Forces Count
Line 167: Change from 7 to desired number
```javascript
const topForces = rankedForces.slice(0, 7);
```

### Modify Colors
Styles section (lines 17-160): Update hex values

---

## 📱 Responsive Design

- Desktop-first (optimized for 1024px+)
- Sidebar stacks on mobile (<768px)
- Print-friendly layout

---

## ⚠️ Browser Requirements

Works in all modern browsers:
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ⚠️ IE11 not supported (uses modern JavaScript)

---

## 🎓 Fast Track Philosophy

**Core Principle:** 60-70% accuracy using internal team knowledge beats expensive 100% research.

**Speed over perfection:**
- Calculate market size in under 5 minutes
- No external research needed
- Focus on strategic clarity, not precision
- Collaborative, not analytical

---

## 🐛 Troubleshooting

**Fonts not loading?**
- Ensure `.otf` files are in the same folder as HTML
- Check browser console (F12) for errors

**Data not saving?**
- Check if localStorage is enabled in browser
- Private/incognito mode may block storage

**Calculations seem wrong?**
- Remember: Growth is multiplicative, not additive
- Margin changes are in percentage *points*, not percentages

---

## 📞 Support

For questions about the tool logic, refer to:
- `how does the market size tool work.txt`
- `fast track tool design template.txt`

---

**Built with:** React 18, TailwindCSS, Fast Track Design System
**Version:** 1.0
**Last Updated:** December 2025

