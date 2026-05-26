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

#### Step 2: Load Online Retail Dataset
1. Go to: https://www.kaggle.com/datasets/vijayuv/onlineretail
2. Click **Download** button (may need Kaggle account - free)
3. Save the file to: `00_Resources/Sample_Data/`
4. Back in Power BI, click **File** → **Get Data** → **Text/CSV** (or **Excel** if xlsx)
5. Browse to your downloaded file and click **Open**
6. Click **Load** to import the data

*Wait ~10-15 seconds for data to load*

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
- What columns did you see in the Online Retail dataset?
- How many rows of data loaded?
- What type of transactions are in this dataset?

---

## TASK 2: CREATE YOUR FIRST VISUAL (MEDIUM)
**Duration:** 30-40 minutes
**Difficulty:** ⭐⭐ Medium
**What you'll learn:** Creating visualizations from scratch

### Objective
Create a bar chart showing Total Sales by Country using the Online Retail dataset.

### Prerequisites
You should have Task 1 completed (Online Retail dataset loaded)

---

### Step-by-Step Instructions

#### Step 1: Create New Report Page
1. Look at the bottom of the screen, right side
2. You'll see a "+" icon next to the page tabs
3. Click the "+" to create a new blank page
4. You now have a blank canvas!

---

#### Step 2: Add First Visual - Bar Chart
1. Go to **Insert tab** (top ribbon)
2. Click **Bar Chart** (horizontal bars work better for countries)
3. A placeholder chart appears on your canvas
4. Resize it by dragging corners to make it bigger

---

#### Step 3: Add Data to Your Chart
You should see a **Visualizations panel** on the right.
Below it, you'll see sections:
- Fields (showing OnlineRetail table columns)
- Axis
- Legend
- Values

**Do this:**
1. In the **Fields** section, find **Country** 
2. Drag **Country** to the **Axis** section
3. Drag **Quantity** to the **Values** section (Power BI will auto-sum it)
4. Now create a calculated field for Sales:
   - Drag **UnitPrice** to **Values** as well
   - We'll multiply Quantity × UnitPrice for total sales

**Result:** You've created your first chart showing countries! 🎉

---

#### Step 4: Customize Your Chart
1. Right-click the chart → **Edit title**
2. Change title to: "Total Sales by Country"
3. Click elsewhere to save

---

#### Step 5: Add a Second Visual - Card
1. Click blank area of canvas
2. Go to **Insert tab** again
3. Click **Card** visual
4. Drag **Quantity** to the Values

**Result:** Shows total quantity sold across all transactions

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
Add Country and Date Range slicers so users can filter the chart interactively.

### Prerequisites
Complete Task 2 first

---

### Step-by-Step Instructions

#### Step 1: Add Country Slicer
1. On your report page, click blank area
2. Go to **Insert tab**
3. Click **Slicer** (looks like a funnel icon)
4. A slicer placeholder appears

---

#### Step 2: Configure Country Slicer
1. In the **Visualizations** panel, look for **Fields**
2. Find the **Country** column (from OnlineRetail table)
3. Drag **Country** to your slicer

**Result:** Slicer shows all available countries

---

#### Step 3: Test the Country Slicer
1. Click a country (e.g., "Netherlands" or "France")
2. Notice: Your bar chart changes to show only that country!
3. Click another country
4. Click "Clear filter" or select multiple to show all again

**This is interactivity!** ✨

---

#### Step 4: Add Date Range Slicer
1. Click blank area of canvas
2. Go to **Insert tab** → **Slicer**
3. Another slicer placeholder appears

---

#### Step 5: Configure Date Slicer
1. In the **Visualizations** panel, find **Fields**
2. Find the **InvoiceDate** column
3. Drag **InvoiceDate** to your new slicer

**Result:** Slicer shows a date range you can filter by

---

#### Step 6: Test Both Slicers Together
1. Select Country = "United Kingdom"
2. Select Date range = Jan 2011 to Jun 2011
3. Your bar chart now shows only UK sales in that date range!
4. Click "Clear" on each slicer to reset

**You now have a fully interactive report!** 🎉

---

#### Step 7: Format the Slicers (Bonus)
1. Click a slicer
2. Click the **Format** icon (paint brush) in Visualizations panel
3. Adjust "Text size" to make text bigger
4. Change colors if you want

---

#### Step 8: Final Save
1. **File** → **Save**
2. This should auto-save as `Day_1_First_Report.pbix`

---

### Testing Your Report
1. Click Country slicer → Select "United Kingdom"
2. Click Date slicer → Select a date range
3. Your bar chart shows only UK sales in that date range!
4. Click "Clear" on slicers to reset all filters

**Congratulations!** You've created an interactive Power BI report! 🎉

---

### Reflection Questions
1. How did having 2 slicers change the user experience?
2. Which slicer is more useful - Country or Date range?
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