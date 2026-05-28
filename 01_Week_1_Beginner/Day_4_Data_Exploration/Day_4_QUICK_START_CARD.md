# ⚡ DAY 4 QUICK START CARD
## Data Exploration - 90 Minute Sprint

---

## 🎯 GOAL

Make dashboard interactive with drill-downs, bookmarks, and advanced filters

---

## ⏱️ TIME BREAKDOWN

```
Task 1 (30 min): Create 2 hierarchies + drill-down
Task 2 (30 min): Create 4-5 bookmarks
Task 3 (30 min): Advanced filtering + drill-through
Total: 90 minutes
```

---

## 🔨 TASK 1: HIERARCHIES (30 min)

### Create Hierarchy 1: Store Geography
```
Modeling → New Hierarchy
Name: "Store Geography"
Order: Region → City → Store

Then add to visual:
- Remove individual "store" field
- Drag "Store Geography" hierarchy
- Drill buttons appear automatically
```

### Create Hierarchy 2: Product
```
Modeling → New Hierarchy
Name: "Product Category"
Order: Category → Product

Add to visual:
- Remove individual "product" field
- Drag "Product Category" hierarchy
- Test drill-down
```

### Test
```
[ ] Drill down works [↓]
[ ] Drill up works [↑]
[ ] Multiple levels work
[ ] No errors
```

---

## 📌 TASK 2: BOOKMARKS (30 min)

### Bookmark 1: Executive Overview
```
View tab → Bookmarks → New
Name: "Executive Overview"
Setup: All slicers on ALL, KPIs prominent
Save
```

### Bookmark 2: Store Manager View
```
View tab → Bookmarks → New
Name: "Store S002 Analysis" (use actual store)
Setup: Filter to 1 store, drill to store level
Save
```

### Bookmark 3: Product Performance
```
View tab → Bookmarks → New
Name: "Product Performance"
Setup: Products prominent, show rankings
Save
```

### Bookmark 4: Seasonal Analysis (Optional)
```
View tab → Bookmarks → New
Name: "Seasonal Comparison"
Setup: Filter by season/year, compare
Save
```

### Bookmark 5: Custom Discovery
```
View tab → Bookmarks → New
Name: "[Your finding name]"
Setup: Show interesting pattern
Save
```

### Test
```
[ ] 4-5 bookmarks created
[ ] Each saves state
[ ] Clicking bookmarks switches views
[ ] No errors
```

---

## 🔍 TASK 3: ADVANCED FILTERING (30 min)

### Advanced Filter 1: Date Range (if applicable)
```
Insert → Slicer → Date
Style: Between
Position: Top
Connect: All date-dependent charts
```

### Advanced Filter 2: Top N
```
Option A (on chart):
Click chart → Data → Filters
Add: product_id → Top N → 10

Option B (slicer):
Insert → Slicer → product_id
Set: Top N = 10
```

### Advanced Filter 3: Drill-Through Page
```
Step 1: Create new page "Store Details"
Step 2: Add store metrics fields
Step 3: Go to main dashboard
Step 4: Right-click store chart
Step 5: Drill through → Select "Store Details"
Step 6: Test: Click store → Jump to detail page
```

### Advanced Filter 4: Highlight Mode (Optional)
```
Click chart → Format → Edit Interactions
Choose slicer → Interaction type: Highlight
(not Filter)

Result: Selected highlights, others gray out
```

### Test
```
[ ] Date range filter works
[ ] Top N filter works
[ ] Drill-through jumps correctly
[ ] Detail page filters
[ ] Highlight mode works (if done)
```

---

## ✅ CHECKLIST

### Hierarchies
- [ ] Store Geography hierarchy created
- [ ] Product Category hierarchy created
- [ ] Both added to visuals
- [ ] Drill buttons work

### Bookmarks
- [ ] Executive Overview
- [ ] Store Manager View
- [ ] Product Performance
- [ ] Seasonal Analysis (optional)
- [ ] Custom Discovery
- [ ] All switch correctly

### Advanced Filters
- [ ] Date range filter
- [ ] Top N filter
- [ ] Drill-through page (optional)
- [ ] Highlight mode (optional)

### Overall
- [ ] No errors
- [ ] All interactivity tested
- [ ] File saved as: Day_4_Data_Exploration_Dashboard.pbix

---

## 📊 QUICK COMMANDS

**Create Hierarchy:**
```
Modeling → New Hierarchy → Add columns → Save
```

**Save Bookmark:**
```
View → Bookmarks → New → Name → Save
```

**Add Advanced Filter:**
```
Insert → Slicer (for date/top N)
OR
Click chart → Data → Filters (on chart)
```

**Set Drill-Through:**
```
Right-click visual → Drill through → Choose target page
```

---

## 🎨 KEY CONCEPTS

```
Drill-down:
- Explore hierarchies (Region → City → Store)
- Natural "zoom in" flow
- Auto-creates hierarchy levels

Bookmarks:
- Save current view state
- Switch between views (1 click)
- Tell data story sequentially

Advanced Filters:
- Complex conditions (Top N, date ranges)
- Drill-through to detail pages
- Highlight vs Filter modes
```

---

## 📁 FILE LOCATION

```
Save as: Day_4_Data_Exploration_Dashboard.pbix

Location:
01_Week_1_Beginner/Day_4_Data_Exploration/Projects/
```

---

## 🚀 GO TIME!

```
1. Open Day_3 dashboard (or rebuild from Day 2 data)
2. Task 1: Create hierarchies (30 min)
3. Task 2: Create bookmarks (30 min)
4. Task 3: Advanced filtering (30 min)
5. Test everything
6. Save file
7. Done! 🎉
```

---

**By end of Day 4, dashboard is interactive & explorable!** 🔍