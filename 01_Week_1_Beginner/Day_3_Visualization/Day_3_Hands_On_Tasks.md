# 📊 DAY 3: BASIC VISUALIZATION
## Learning Guide - Chart Types & Creating Your First Dashboard

---

## WHAT IS DATA VISUALIZATION?

**Definition:** Converting data into visual format (charts, graphs, maps) so people understand insights quickly.

**Why?** 
```
Data table: 1000 rows × 10 columns → Hard to understand
Chart: One visual → Insight in 2 seconds
```

---

## KEY CONCEPT: MATCH QUESTION TO CHART TYPE

```
What's your question?
├─ "Show TREND over TIME?" → LINE CHART
├─ "COMPARE values?" → COLUMN/BAR CHART
├─ "Show PART OF WHOLE?" → PIE/DONUT
├─ "Show RELATIONSHIP?" → SCATTER PLOT
├─ "Need DETAILS?" → TABLE
└─ "Show RANKING?" → SORTED BAR CHART
```

---

## CHART TYPES

### 1️⃣ COLUMN CHART (Vertical Bars)
**Best for:** Comparing values across categories

```
Use when: "Which store has highest sales?"
Example: Sales by store (S001, S002, S003...)
Height = Sales amount
Width = Store name
```

**Data kamu:** Sales by store_id

---

### 2️⃣ BAR CHART (Horizontal Bars)
**Best for:** Comparing categories, long names

```
Use when: "Rank products by sales"
Example: Top 10 products
Bar length = Sales
Label = Product name
```

**Data kamu:** Top products by revenue

---

### 3️⃣ LINE CHART
**Best for:** Trends over time

```
Use when: "How did sales change each month?"
Example: Sales trend over 2020-2024
X-axis = Month/Year
Y-axis = Sales amount
Line shows direction
```

**Data kamu:** Sales by transaction_year

---

### 4️⃣ PIE CHART
**Best for:** Part-to-whole (percentages)

```
Use when: "What % of sales by gender?"
Example: Male 60%, Female 40%
Slice size = percentage
Only works for 3-7 categories max
```

**Data kamu:** Sales by gender

---

### 5️⃣ DONUT CHART
**Best for:** Better than pie chart

```
Use when: Same as pie, but nicer looking
Advantage: Can show center metric
Example: Center shows total, slices show breakdown
```

**Data kamu:** Sales by age_segment

---

## VISUALIZATION WORKFLOW IN POWER BI

```
Step 1: Prepare data (DONE in Day 2)
Step 2: Create visualization
        ├─ Drag fields to visual
        ├─ Choose chart type
        └─ Configure axes/values

Step 3: Format visual
        ├─ Colors
        ├─ Labels
        ├─ Legend
        └─ Titles

Step 4: Add to dashboard
Step 5: Add interactivity (slicers)
```

---

## HOW TO CREATE A CHART IN POWER BI

### BASIC STEPS

```
1. Insert tab → Choose chart type
2. Drag column to X-axis (Categories)
3. Drag column to Y-axis (Values)
4. Chart appears!
5. Format as needed
```

### EXAMPLE: Column Chart

```
1. Insert → Column Chart
2. Drag "store_id" to Axis
3. Drag "list_price" to Values
4. Chart: Sales by store
```

---

## COLOR BEST PRACTICES

### Professional Palette
```
✅ DO:
- Use 1-3 main colors
- Blue = primary
- Orange/Red = accent
- Gray = neutral

❌ DON'T:
- Rainbow colors
- Too many colors (>5)
- Neon colors
- Red + Green (colorblind unfriendly)
```

### Color Meaning
```
Blue = Safe, professional, trustworthy
Red = Alert, negative, important
Green = Positive, success, good
Gray = Neutral, less important
Orange = Warning, highlight
```

---

## FORMATTING TIPS

### Chart Titles
```
✅ Good: "Total Sales by Store"
❌ Bad: "Sales"

✅ Good: "Revenue Trend (2020-2024)"
❌ Bad: "Chart"
```

### Data Labels
```
✅ Show: Numbers, percentages (if helpful)
❌ Show too many: Clutters visual

Rule: Only if space allows
```

### Legend Position
```
Right side: Default (good)
Bottom: If space limited
Top: If chart is tall
Hide: If only 1 data series
```

---

## SLICERS (FILTERS)

**What:** Interactive buttons to filter data

**Types:**
```
Dropdown slicer: Choose 1-2 values
Checkbox slicer: Select multiple
Timeline slicer: Pick date range
```

**How to add:**
```
Insert tab → Slicer
Choose column (store_id, gender, etc)
Slicer appears
Click to filter all visuals
```

---

## DASHBOARD LAYOUT

### Good Dashboard Design

```
┌─────────────────────────────────────┐
│  KPI CARDS (Top - Most Important)   │
│  ┌──────────┐ ┌──────────┐         │
│  │ Total $  │ │ Orders   │         │
│  └──────────┘ └──────────┘         │
├─────────────────────────────────────┤
│  MAIN VISUALS (Middle - Focus)      │
│  ┌──────────────┐ ┌──────────────┐  │
│  │  Sales Trend │ │ Top Products │  │
│  └──────────────┘ └──────────────┘  │
├─────────────────────────────────────┤
│  DETAILS (Bottom - Supporting)      │
│  ┌──────────────────────────────┐   │
│  │  Sales by Region             │   │
│  └──────────────────────────────┘   │
├─────────────────────────────────────┤
│  FILTERS (Left or Top)              │
│  [Store ▼] [Gender ▼] [Year ▼]     │
└─────────────────────────────────────┘
```

---

## ACCESSIBILITY

### Colorblind Friendly
```
✅ Use blue + orange (not red + green)
✅ Use patterns + colors
✅ High contrast (dark text on light)
```

### Mobile Friendly
```
✅ Large buttons (slicers)
✅ Clear labels
✅ Responsive layout
```

---

## COMMON MISTAKES

❌ **Too many charts on one page** → Confusing
✅ Do: 4-6 visuals per page

❌ **Wrong chart type** → Misrepresents data
✅ Do: Match question to chart

❌ **No titles/labels** → Unclear
✅ Do: Clear titles, data labels

❌ **Too many colors** → Distracting
✅ Do: 2-3 main colors

---

## SUMMARY: KEY TAKEAWAYS

```
✅ Match question to chart type
✅ Use professional colors
✅ Add clear titles & labels
✅ Keep designs simple
✅ Add slicers for interactivity
✅ Test on mobile
✅ Think about colorblind users
```

---

## READY FOR HANDS-ON?

You'll create:
- 4+ professional charts
- Using cleaned data from Day 2
- With slicers
- On a dashboard
- Professional formatting

Let's go! 🚀