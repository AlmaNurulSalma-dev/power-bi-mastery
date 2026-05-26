# DAY 1: HANDS-ON TASKS
## Task 1 (Easy) → Task 2 (Medium) → Task 3 (Hard)

**Prerequisites:**
- [ ] Power BI Desktop installed
- [ ] Free Microsoft account
- [ ] Day 1 Learning Guide read

---

## TASK 1: LOAD SAMPLE DATA (EASY)
**Duration:** 20-30 minutes
**Difficulty:** ⭐ Easy
**What you'll learn:** How to load data into Power BI

### Objective
Load the built-in "Sales" sample dataset into Power BI Desktop and explore the data.

### Step-by-Step Instructions

#### Step 1: Open Power BI Desktop
1. Click Start menu → Search "Power BI" → Open "Power BI Desktop"
2. You'll see the welcome screen
3. Sign in with your Microsoft account (or create free one)
4. Click "Get started"

---

#### Step 2: Load Sample Data
1. Click **File** (top left menu)
2. Click **Open report**
3. Look for "Retail Analysis Sample.pbix"
   - If you don't see it, go to: File → Samples → Retail Analysis Sample
4. Click **Open**

*Wait ~30 seconds for Power BI to load the sample*

---

#### Step 3: Explore What Loaded
Once loaded, you'll see:
- **Left sidebar:** 3-4 report pages already created
- **Canvas:** A pre-made dashboard with charts
- **Right panel:** Fields panel showing all data columns

**What you're seeing:**
- This is someone's pre-built report
- It has visuals (charts, tables)
- It has data behind it

---

#### Step 4: Click Through Pages
In the left sidebar, you'll see tabs like:
- Overview
- Regional Analysis
- Product Details
- Trend Analysis

**Click each one** and notice:
- Different visuals on each page
- Different data being shown
- Different charts (bar, line, pie, etc.)

---

#### Step 5: Explore the Fields
Look at the **Right panel** (Fields):
You'll see tables like:
- Sales (contains Amount, OrderDate, Quantity)
- Product (contains ProductName, Category, Color)
- Region (contains City, Country, Region)

**What this means:**
- These are your data tables
- Each has columns (fields)
- Power BI will use these to create visuals

---

#### Step 6: Take a Screenshot
Screenshot the desktop and save in your Day 1 folder:
- Path: `01_Week_1_Beginner\Day_1_Intro\Day_1_Task_1_Screenshot.png`

---

### Reflection Question
Answer this in your notes:
- What surprised you about what Power BI pre-built?
- How many visuals did you count across all pages?
- What data tables did you identify?

---

## TASK 2: CREATE YOUR FIRST VISUAL (MEDIUM)
**Duration:** 30-40 minutes
**Difficulty:** ⭐⭐ Medium
**What you'll learn:** Creating visualizations from scratch

### Objective
Create a simple bar chart showing Sales by Product Category.

### Prerequisites
You should have Task 1 completed (Retail Analysis Sample loaded)

---

### Step-by-Step Instructions

#### Step 1: Create New Report Page
1. Look at the bottom of the screen, right side
2. You'll see a "+" icon next to the page tabs
3. Click the "+" to create a new blank page
4. You now have a blank canvas!

---

#### Step 2: Add First Visual
1. Go to **Insert tab** (top ribbon)
2. Click **Column Chart** (or Bar Chart)
3. A placeholder chart appears on your canvas
4. Resize it by dragging corners to make it bigger

---

#### Step 3: Add Data to Your Chart
You should see a **Visualizations panel** on the right.
Below it, you'll see sections:
- Fields
- Legend
- Axis
- Values

**Do this:**
1. In the **Fields** section on right, find **Product** table
2. Expand it (click arrow)
3. Drag **Category** to the **Axis** section
4. Drag **Sales** (or Amount) to the **Values** section

**Result:** You've created your first chart! 🎉

---

#### Step 4: Customize Your Chart
1. Right-click the chart → **Edit title**
2. Change title to: "Total Sales by Category"
3. Click elsewhere to save

---

#### Step 5: Add a Second Visual
1. Click blank area of canvas
2. Go to **Insert tab** again
3. Click **Card** visual
4. Drag **Amount** (or Sales) to the Values

**Result:** Shows a single large number (total sales)

---

#### Step 6: Save Your Work
1. Click **File** → **Save**
2. Name it: `Day_1_First_Report.pbix`
3. Save in: `01_Week_1_Beginner\Day_1_Intro\Projects\`

---

### Reflection Questions
1. How did adding fields change your visual?
2. What happened when you dragged Category to Axis?
3. What happened when you dragged Amount to Values?
4. How is this different from Excel?

---

## TASK 3: ADD INTERACTIVITY (HARD)
**Duration:** 40-50 minutes
**Difficulty:** ⭐⭐⭐ Hard
**What you'll learn:** Interactive filters (slicers)

### Objective
Add a Region slicer so users can filter the chart by region.

### Prerequisites
Complete Task 2 first

---

### Step-by-Step Instructions

#### Step 1: Add a Slicer
1. On your blank report page, click blank area
2. Go to **Insert tab**
3. Click **Slicer** (looks like a funnel icon)
4. A slicer placeholder appears

---

#### Step 2: Configure Slicer
1. In the **Visualizations** panel, look for **Fields**
2. Find the **Region** table
3. Expand it and find **Region** column
4. Drag **Region** to your slicer

**Result:** Slicer shows all available regions

---

#### Step 3: Test the Slicer
1. Click a region (e.g., "North")
2. Notice: Your bar chart changes to show only that region!
3. Click another region
4. Click "Clear filter" to show all again

**This is interactivity!** ✨

---

#### Step 4: Format the Slicer (Bonus)
1. Click the slicer
2. Click the **Format** icon (paint brush) in Visualizations panel
3. Adjust "Text size" to make text bigger
4. Change "Slicer header" color if you want

---

#### Step 5: Add Another Slicer
Repeat Steps 1-2, but this time:
1. Create another slicer
2. Add **Product Category** to it
3. Now users can filter by BOTH Region AND Category!

---

#### Step 6: Final Save
1. **File** → **Save**
2. This should auto-save as `Day_1_First_Report.pbix`

---

### Testing Your Report
1. Click Region slicer → Select "East"
2. Click Category slicer → Select "Phones"
3. Your bar chart shows only Phone sales in the East region!
4. Click "Clear" on slicers to reset

**Congratulations!** You've created an interactive Power BI report! 🎉

---

### Reflection Questions
1. How did the slicer change user experience vs static chart?
2. What if a user wants to see 2 regions at once?
3. How is this better than sending an Excel file?

---

## TASK COMPLETION CHECKLIST

### Task 1: Load Sample Data
- [ ] Power BI Desktop installed
- [ ] Retail Analysis Sample loaded
- [ ] Explored all pages
- [ ] Reviewed Fields panel
- [ ] Screenshot saved

**Time spent:** _____ minutes

---

### Task 2: Create Your First Visual
- [ ] Created new blank page
- [ ] Created column chart
- [ ] Added Category to Axis
- [ ] Added Amount/Sales to Values
- [ ] Changed chart title
- [ ] Created Card visual
- [ ] Saved report as PBIX file

**Time spent:** _____ minutes
**Confidence level:** ⭐⭐⭐⭐⭐

---

### Task 3: Add Interactivity
- [ ] Created first slicer with Region
- [ ] Tested slicer interaction
- [ ] Chart filtered based on slicer
- [ ] Created second slicer with Category
- [ ] Both slicers work together
- [ ] Formatted slicer appearance
- [ ] Saved final report

**Time spent:** _____ minutes
**Confidence level:** ⭐⭐⭐⭐⭐

---

## TROUBLESHOOTING

### Problem: "Power BI won't open"
**Solution:** 
- Restart computer
- Uninstall & reinstall Power BI Desktop
- Try launching as Administrator (right-click → Run as Admin)

---

### Problem: "Sample data won't load"
**Solution:**
- Go to File → Options & Settings → Options
- Search "Sample"
- Download Retail Analysis Sample again

---

### Problem: "My chart is blank"
**Solution:**
- Check that you've added fields to the visual
- Make sure you're dragging the right field
- Click the chart → Check Visualizations panel shows your fields

---

### Problem: "Slicer doesn't filter the chart"
**Solution:**
- Ensure slicer and chart are on same page
- Check that chart has the same field as slicer
- Delete and recreate slicer

---

## KEY LEARNINGS TODAY

You've learned:
1. ✅ How to load data into Power BI
2. ✅ How to create visualizations
3. ✅ How to make reports interactive
4. ✅ How to save your work

**This is the foundation!** Everything else builds on these skills.

---

## NEXT: WRITE YOUR CASE STUDY ESSAY

Once you complete all 3 tasks:
1. Reflect on what you learned
2. Write a 1000+ word essay
3. Use the Case Study Template in `00_Resources\Templates\`
4. See Day 1 Essay Prompt in next document

---

## FINAL NOTES

**Common mistakes to avoid:**
- ❌ Don't overthink it - you're learning!
- ❌ Don't skip Steps - follow them in order
- ❌ Don't worry about making it perfect - just practice
- ✅ Do experiment - try things! (you can't break it)
- ✅ Do ask questions - that's how you learn
- ✅ Do save frequently - in case of crashes

**Remember:** Every expert was once a beginner. You're on the right path! 🚀