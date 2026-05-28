# 🔍 DAY 4: HANDS-ON TASKS
## Data Exploration - Drill-Down, Bookmarks & Advanced Filtering

---

## OVERVIEW

**Goal:** Add exploration capabilities to Day 3 dashboard using drill-downs, bookmarks, and advanced filters

**Time:** 90 minutes (3 tasks × 30 min each)
**Difficulty:** Medium → Medium-Hard → Hard

**Prerequisites:**
- Day_3_Visualization_Dashboard.pbix (from Day 3)
- OR Day_2_Power_Query_Practice.pbix + create visuals

---

## TASK 1: CREATE HIERARCHIES & DRILL-DOWN (30 minutes)

### Goal: Set up 2 hierarchies with drill-down capability

---

### Hierarchy 1: Geographic (Store)

**If you have location data:**

```
Create hierarchy: Store Geography
├─ Region (if available)
├─ City (if available)
└─ Store

Steps:
1. Modeling tab → New Hierarchy
2. Name: "Store Geography"
3. Add columns in order:
   - Region (parent)
   - City
   - Store (detail)
4. OK

Now in visuals:
5. Find bar/column chart showing stores
6. Replace store field with "Store Geography" hierarchy
7. Drill buttons appear automatically
8. Test: Click drill-down button [↓]
```

**Expected result:**
```
Level 1: [Region: North] [Region: South] [Region: East]
         (Click drill button)
Level 2: [City: Boston] [City: NYC] (from North region)
         (Click drill button)
Level 3: [Store: S001] [Store: S002] (from Boston)
```

---

### Hierarchy 2: Product

**If you have product categories:**

```
Create hierarchy: Product Category
├─ Category (if available)
├─ Subcategory (if available)
└─ Product ID

Steps:
1. Modeling tab → New Hierarchy
2. Name: "Product Category"
3. Add columns in order:
   - Category (parent)
   - Subcategory (if exists)
   - Product ID (detail)
4. OK

5. Find chart showing products (bar chart?)
6. Replace product field with "Product Category"
7. Test drill-down functionality
```

**Expected result:**
```
Level 1: [Bottoms] [Tops] [Accessories]
Level 2: [Shirts] [T-Shirts] (from Tops category)
Level 3: [Specific Product ID] (detailed)
```

---

### Test Drill-Down

For each hierarchy:
- [ ] Drill down button [↓] works
- [ ] Shows next level of detail
- [ ] Drill up button [↑] returns to parent
- [ ] Multiple drill levels functional
- [ ] No errors when drilling

---

## TASK 2: CREATE BOOKMARKS (30 minutes)

### Goal: Create 4-5 bookmarks for different views

---

### Bookmark 1: Executive Overview

**Purpose:** High-level dashboard for leadership

```
Setup:
1. Ensure all slicers show ALL data
2. Highlight KPI cards prominently
3. Show total sales, order count
4. Main trends visible
5. No detailed drill-downs needed

Save as bookmark:
1. View tab → Bookmarks → New
2. Name: "Executive Overview"
3. Description: "High-level summary for leadership"
4. Save

What it captures:
- All stores visible
- All years visible
- Top-level charts (not drilled down)
- Clean, simple view
```

---

### Bookmark 2: Store Manager View

**Purpose:** Single store deep dive

```
Setup:
1. Set slicers:
   - Store: Choose 1 store (e.g., S002)
   - Year: All years OR current year
2. Drill down hierarchies:
   - If store hierarchy exists, go to store level
   - If product hierarchy exists, show products sold in that store
3. Focus on:
   - Revenue from this store
   - Top products in this store
   - Customer breakdown for this store
4. Arrange visuals for store focus

Save as bookmark:
1. View tab → Bookmarks → New
2. Name: "Store S002 Analysis" (use actual store)
3. Save

What it captures:
- Single store filtered
- Drilled down to store level
- Store-specific metrics highlighted
- Manager-focused view
```

---

### Bookmark 3: Product Performance

**Purpose:** Product-centric analysis

```
Setup:
1. Ensure product chart is prominent
2. Drill down to product level (if hierarchy exists)
3. Show top-performing products
4. Filter by:
   - Category (optional - all categories)
   - Region (optional - all regions)
5. Focus on:
   - Revenue by product
   - Product rankings
   - Seasonal trends (by year)

Save as bookmark:
1. View tab → Bookmarks → New
2. Name: "Product Performance"
3. Save
```

---

### Bookmark 4: Seasonal Analysis (Optional)

**Purpose:** Compare seasons

```
Setup:
1. If you have season data:
   - Filter to Summer only
   - Compare with Winter
   - Show sales differences
2. If using year:
   - Compare 2023 vs 2024
   - Show growth patterns
3. Highlight:
   - Best-performing season
   - Product variations by season
   - Regional differences

Save as bookmark:
1. View tab → Bookmarks → New
2. Name: "Seasonal Comparison"
3. Save
```

---

### Bookmark 5: Custom Discovery (Your choice)

**Purpose:** Any interesting pattern you find

```
Examples:
- "High-Value Customers" (filter by spending)
- "Weekend vs Weekday" (if date available)
- "Regional Spotlight" (one region focus)
- "Price vs Quantity" (correlation analysis)

Setup:
1. Explore your data
2. Find something interesting
3. Set slicers/filters to show it
4. Save as bookmark with descriptive name

Save as bookmark:
1. View tab → Bookmarks → New
2. Name: "[Your discovery name]"
3. Save
```

---

### Test Bookmarks

- [ ] All 4-5 bookmarks created
- [ ] Each bookmark saves its state
- [ ] Clicking bookmark switches views correctly
- [ ] Slicers reset appropriately
- [ ] Drill-downs remembered
- [ ] No errors when switching bookmarks

---

## TASK 3: ADVANCED FILTERING & DRILL-THROUGH (30 minutes)

### Goal: Implement advanced filtering techniques

---

### Advanced Filter 1: Date Range Filter (if applicable)

**If you have date data:**

```
Setup date range filter:
1. Insert → Slicer → Date
2. Style: Between (shows date range picker)
3. Name: "Date Range"
4. Position: Top of page
5. Connect to: All date-dependent visuals

What it enables:
- User selects: "Jan 1 - Mar 31"
- All charts update to show only that period
- More flexible than year slicer

Test:
- Select date range
- All visuals update? ✓
- Date range clearly visible? ✓
```

---

### Advanced Filter 2: Top N Filter

**Show only top products (e.g., Top 10)**

```
Setup:
1. On bar/column chart with products
2. Click chart → Data → Filters
3. Add filter:
   - Field: product_id
   - Filter type: Top N
   - Top: 10 (or your choice)
4. Apply

What it shows:
- Only top 10 products by sales
- Hides lower-performing products
- User can see: "Top 10 out of 1,000 products"

Alternative (more flexible):
Create slicer with Top N setting
- View tab → Slicer
- Field: product_id
- Top N: 10
- Users can change number
```

---

### Advanced Filter 3: Drill-Through Page (Optional but recommended)

**Create detail page that drill-through can target**

```
Step 1: Create new page
- New → Page
- Name: "Store Details"

Step 2: Add fields
- Store name, region, city
- Sales metrics for that store
- Product breakdown
- Customer breakdown

Step 3: Set up drill-through source
- Go back to main dashboard
- Find store chart/visual
- Right-click visual → Drill through
- Choose: "Store Details" as target

Step 4: Test drill-through
- Click on a store in main dashboard
- Should jump to "Store Details" page
- Page should show only that store's data
- Column from main table auto-filters detail page

What user sees:
Main page: Sales by store
Click store → Detail page: Detailed store analysis
```

---

### Advanced Filter 4: Highlight Mode (Optional)

**Instead of filtering, highlight selected values**

```
Setup (alternative to filtering):
1. Select visual with multiple values
2. Click visual → Format → Edit Interactions
3. Choose slicer
4. Interaction type: Highlight (not Filter)

What happens:
- User clicks slicer
- Selected data highlights (darker)
- Other data grays out (not hidden)
- User still sees context

Example:
- User clicks "Store S002"
- S002 data bright, others gray
- User can see "S002 is 20% of total"
- Without filtering, keeps perspective
```

---

## TEST ALL FUNCTIONALITY

### Checklist

- [ ] Drill-downs work (store → city → store)
- [ ] Drill-downs work (category → product)
- [ ] All 4-5 bookmarks functional
- [ ] Switching bookmarks restores state
- [ ] Date range filter works
- [ ] Top N filter works
- [ ] Drill-through jumps to detail page
- [ ] Detail page filters correctly
- [ ] Highlight mode works (if implemented)
- [ ] No errors or glitches

---

## SAVE & DOCUMENT

**Save file:**
```
File → Save As

Name: Day_4_Data_Exploration_Dashboard.pbix
Location: 01_Week_1_Beginner/Day_4_Data_Exploration/Projects/
```

**Document what you built:**
- List hierarchies created
- List bookmarks created
- List filters implemented
- List drill-through pages (if created)

---

## REFLECTION QUESTIONS

1. **Which exploration technique was most useful?**
   - Drill-down? Bookmarks? Advanced filters?
   - Why?

2. **How did hierarchies improve exploration?**
   - Did users (you) understand data better?

3. **Did bookmarks help tell data story?**
   - Could you sequence them to reveal insights?

4. **What advanced filter surprised you?**
   - Did you discover something unexpected?

5. **If you were a business user, what would you want to explore?**
   - What bookmarks would help most?

---

## TROUBLESHOOTING

### Drill-down not appearing
- Check: Is hierarchy created?
- Check: Is hierarchy added to visual (not individual field)?
- Fix: Use hierarchy in visual, not individual columns

### Bookmark doesn't save state
- Check: What changed? Hierarchy level? Slicer?
- Note: Some changes may not save in bookmark
- Workaround: Use manual slicer positioning

### Drill-through doesn't work
- Check: Is detail page created?
- Check: Are you right-clicking correct visual?
- Check: Is target page field related to source?
- Fix: Verify relationship between tables

### Slicer doesn't filter
- Check: Is slicer connected? (Edit Interactions)
- Check: Is slicer field correct?
- Check: Does field exist in all tables?

---

## NEXT: CAPSTONE PROJECT

After Day 4, you'll use all these techniques in:

**Week 1 Capstone: Sales Dashboard**
- Visualizations (Day 3 concepts)
- Exploration features (Day 4 concepts)
- Professional appearance
- Interactive storytelling

This is where everything comes together! 🚀

---

Good luck exploring! 🔍