# 📊 DAY 3: HANDS-ON TASKS
## Create Your First Dashboard with Interactive Visualizations

---

## OVERVIEW

**Goal:** Create professional dashboard with 5+ visualizations using cleaned data from Day 2

**Time:** 90 minutes (3 tasks × 30 min each)
**Difficulty:** Easy → Medium → Hard

---

## ✅ BEFORE YOU START

Checklist:
- [ ] Day_2_Power_Query_Practice.pbix loaded
- [ ] Clean data available (customer, product, sales, store)
- [ ] Power BI Desktop open
- [ ] New blank report ready

---

## TASK 1: CREATE BASIC CHARTS (30 minutes)

**Goal:** Create 3 basic charts

### Chart 1: Column Chart - Sales by Store

**Steps:**
1. Insert tab → Column Chart
2. Drag to Visualizations:
   - Axis: store_id (from store_data)
   - Values: Sum of list_price (from product_data)
3. Result: Vertical bars showing sales per store
4. Format:
   - Title: "Total Sales by Store"
   - Data labels: ON
   - Colors: Blue theme

**Expected result:**
```
Bar heights show:
- S001: Some amount
- S002: Some amount
- S003: Some amount
- etc.
```

---

### Chart 2: Bar Chart - Top 10 Products

**Steps:**
1. Insert tab → Bar Chart (horizontal)
2. Drag to Visualizations:
   - Axis: product_id
   - Values: Sum of list_price
3. Sort descending (highest sales first)
4. Filter to Top 10 products
5. Format:
   - Title: "Top 10 Products by Revenue"
   - Data labels: ONTop 10 Products by Revenue

**Expected result:**
```
Longest bars at top (highest sales)
Shortest bars at bottom (10th position)
```

---

### Chart 3: Pie Chart - Sales by Gender

**Steps:**
1. Insert tab → Pie Chart
2. Drag to Visualizations:
   - Legend: gender
   - Values: Sum of list_price
3. Format:
   - Title: "Sales Distribution by Gender"
   - Data labels: Percentages
   - Colors: Contrasting colors (not red + green)

**Expected result:**
```
Pie slices showing:
- Male: X%
- Female: Y%
- Other: Z% (if not removed)
```

---

## TASK 2: CREATE TIME & SEGMENT CHARTS (30 minutes)

**Goal:** Create 2 more charts with custom columns from Day 2

### Chart 4: Line Chart - Sales Trend by Year

**Steps:**
1. Insert tab → Line Chart
2. Drag to Visualizations:
   - Axis: transaction_year (custom column from Day 2)
   - Values: Sum of list_price
   - Legend: None (only 1 line)
3. Format:
   - Title: "Sales Trend Over Time"
   - Data labels: ON
   - Line color: Blue
   - Line thickness: Medium

**Expected result:**
```
Line showing sales trend from 2020 → 2024
Up/down pattern visible
```

---

### Chart 5: Donut Chart - Sales by Age Segment

**Steps:**
1. Insert tab → Donut Chart
2. Drag to Visualizations:
   - Legend: age_segment (custom column from Day 2)
   - Values: Sum of list_price
3. Format:
   - Title: "Sales by Age Segment"
   - Data labels: Percentages
   - Center metric: Total sales amount
   - Colors: Professional palette (blue, orange, gray)

**Expected result:**
```
Donut with center showing total
Segments: Young, Adult, Senior
Percentages clear
```

---

## TASK 3: ADD SLICERS & DASHBOARD LAYOUT (30 minutes)

**Goal:** Add interactivity and create professional dashboard

### Step 1: Add Slicers (Filters)

**Slicer 1: Store Filter**
1. Insert tab → Slicer
2. Select: store_id
3. Style: Dropdown
4. Position: Top-left
5. Connect to: ALL charts (click chart → Format → Edit Interactions)

**Slicer 2: Gender Filter**
1. Insert tab → Slicer
2. Select: gender
3. Style: Buttons (Checkbox)
4. Position: Top-middle
5. Connect to: ALL charts

**Slicer 3: Year Range Filter**
1. Insert tab → Slicer
2. Select: transaction_year
3. Style: Between (range)
4. Position: Top-right
5. Connect to: ALL charts

---

### Step 2: Organize Dashboard Layout

**Page Layout:**
```
┌──────────────────────────────────────────────┐
│  SLICERS (Top Row)                           │
│  [Store ▼] [Gender ☐☐☐] [Years: 2020-2024] │
├──────────────────────────────────────────────┤
│  TOP VISUALS (Middle)                        │
│  ┌─────────────────┐  ┌─────────────────┐   │
│  │ Sales by Store  │  │ Top 10 Products │   │
│  │ (Column)        │  │ (Bar)           │   │
│  └─────────────────┘  └─────────────────┘   │
├──────────────────────────────────────────────┤
│  TREND VISUAL (Bottom-Left)                  │
│  ┌──────────────────────────────────────┐   │
│  │ Sales Trend (Line Chart)             │   │
│  └──────────────────────────────────────┘   │
├──────────────────────────────────────────────┤
│  DISTRIBUTION VISUALS (Bottom-Right)        │
│  ┌─────────────────┐  ┌─────────────────┐   │
│  │ Sales by Gender │  │ Sales by Age    │   │
│  │ (Pie)           │  │ (Donut)         │   │
│  └─────────────────┘  └─────────────────┘   │
└──────────────────────────────────────────────┘
```

---

### Step 3: Format Dashboard

**Colors & Theme:**
- Background: Light gray (not white)
- Charts: Blue primary color
- Accents: Orange for key metrics
- Text: Dark gray (not black)

**Typography:**
- Title: 18pt, bold, dark gray
- Slicer labels: 11pt, bold
- Chart labels: 10pt, regular

**Spacing:**
- Between slicers: 20px
- Between charts: 30px
- Top margin: 40px

---

### Step 4: Test Interactivity

**Test each slicer:**
```
1. Click Store slicer → All charts update? ✓
2. Click Gender slicer → All charts update? ✓
3. Click Year range → All charts update? ✓
4. Combination filters → Works together? ✓
```

**Test on Mobile:**
- View → Mobile Layout
- Check if slicers still accessible
- Check if charts readable on small screen

---

## FINAL CHECKLIST

### Visuals Created
- [ ] Chart 1: Column chart (Sales by Store)
- [ ] Chart 2: Bar chart (Top 10 Products)
- [ ] Chart 3: Pie chart (Sales by Gender)
- [ ] Chart 4: Line chart (Sales Trend)
- [ ] Chart 5: Donut chart (Sales by Age Segment)

### Slicers Created
- [ ] Slicer 1: Store dropdown
- [ ] Slicer 2: Gender buttons
- [ ] Slicer 3: Year range

### Formatting Complete
- [ ] Professional colors (2-3 main colors)
- [ ] Clear titles on all visuals
- [ ] Data labels visible
- [ ] Legends positioned correctly
- [ ] Dashboard well-organized
- [ ] Mobile-friendly layout

### Interactivity Working
- [ ] All slicers connected to all charts
- [ ] Filtering works across all visuals
- [ ] No errors or broken connections
- [ ] Combination filters work

### Save & Export
- [ ] Save as: Day_3_Visualization_Dashboard.pbix
- [ ] Location: 01_Week_1_Beginner/Day_3_Visualization/Projects/
- [ ] File size reasonable (< 50MB)

---

## REFLECTION QUESTIONS

1. **Which chart type was easiest to create?**
   Answer: _________________________________

2. **Which was hardest?**
   Answer: _________________________________

3. **Did the dashboard tell a clear story about the data?**
   Answer: _________________________________

4. **What would you change for better visuals?**
   Answer: _________________________________

5. **How did slicers enhance the dashboard?**
   Answer: _________________________________

---

## TROUBLESHOOTING

### Chart doesn't show data?
- Check: Is field correct data type?
- Check: Are there null values?
- Check: Is relationship correct?

### Slicer doesn't filter?
- Check: Is slicer connected to chart? (Edit Interactions)
- Check: Is field from correct table?
- Check: Does field exist in all tables?

### Colors look bad?
- Use: ColorBrewer (https://colorbrewer2.org/)
- Use: Power BI default themes
- Avoid: Too many colors (max 5)

### Mobile view broken?
- View → Mobile Layout
- Resize charts as needed
- Stack vertically (not side-by-side)

---

## TIME BREAKDOWN

```
Task 1 (Charts 1-3): 30 min
Task 2 (Charts 4-5): 30 min
Task 3 (Slicers + Layout): 30 min
─────────────────────────
Total: 90 minutes
```

If taking longer, that's normal! Focus on understanding, not speed.

---

## NEXT AFTER DAY 3

Day 4: Data Exploration
- Drill-down capabilities
- Bookmarks
- Advanced filtering
- Storytelling with data

---

Good luck! Your first professional dashboard awaits! 🚀