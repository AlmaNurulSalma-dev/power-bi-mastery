# DAY 2: HANDS-ON TASKS
## Task 1 (Easy) → Task 2 (Medium) → Task 3 (Hard)

**Prerequisites:**
- [ ] Power BI Desktop open
- [ ] Day 2 Learning Guide read
- [ ] Sample messy data file (we'll create or download)

---

## TASK 1: LOAD & EXPLORE MESSY DATA (EASY)
**Duration:** 15-20 minutes
**Difficulty:** ⭐ Easy
**What you'll learn:** How to load data and see quality issues

### Objective
Load a messy dataset and identify data quality problems.

### Step-by-Step Instructions

#### Step 1: Get Sample Messy Data

**RECOMMENDED: Download Retail Fashion Data**
- Go to: https://www.kaggle.com/datasets/vanpatangan/retail-fashion-data
- Click "Download" button
- Save to: `00_Resources/Sample_Data/`

**Why this dataset:**
```
✅ Real retail fashion data (messy)
✅ Multiple quality issues
✅ Great for learning transformations
✅ Practical business scenario
✅ Mix of customer, product, and sales data
```

**Alternative if download fails:**
- Dirty Customer Data: https://www.kaggle.com/datasets/thenuclearnexus/dirty-customer-data
- E-Commerce Data: https://www.kaggle.com/datasets/carrie1/ecommerce-data

#### Step 2: Load Data in Power BI
1. **File** → **Get Data** → **Text/CSV**
2. Browse to your CSV file
3. Click **Load**

*Wait for data to load (30-60 seconds)*

#### Step 3: Explore the Data
Power BI will show you the data table. Look for:
- **Column names** - Are they clear?
- **Data types** - Are they correct? (Text looks like text, numbers like numbers?)
- **Duplicates** - Do any rows repeat?
- **Blank cells** - Any empty values?
- **Inconsistencies** - Same data written differently?

#### Step 4: Take Notes
Write down 5 data quality issues you see:
1. ________________________
2. ________________________
3. ________________________
4. ________________________
5. ________________________

#### Step 5: Take Screenshot
Screenshot of the raw data (showing any issues)
Save as: `Day_2_Task_1_Raw_Data.png`

---

### Reflection Question
- What's the biggest data quality issue?
- How would you clean it manually vs with Power Query?

---

## TASK 2: CLEAN DATA WITH POWER QUERY (MEDIUM)
**Duration:** 30-40 minutes
**Difficulty:** ⭐⭐ Medium
**What you'll learn:** Basic Power Query transformations

### Objective
Apply 3-4 Power Query transformations to clean the data.

### Step-by-Step Instructions

#### Step 1: Open Power Query Editor
1. Your data should be loaded in Power BI
2. Right-click the table → **Edit query** (or click **Transform data**)
3. Power Query Editor window opens
4. You see raw data + Applied Steps panel on right

#### Step 2: Remove Duplicates
1. **Home tab** → **Remove Duplicates**
2. Select all columns (or just key columns like InvoiceNo, CustomerID)
3. Click **OK**
4. Notice new Applied Step appears: "Removed Duplicates"

**Result:** Duplicate rows deleted

---

#### Step 3: Remove Blank Rows
1. Click any column header
2. Click **Home** → **Remove Rows** → **Remove Blank Rows**
3. Click **OK**
4. New Applied Step: "Removed Blank Rows"

**Result:** Empty rows deleted

---

#### Step 4: Change Data Types
1. Click **InvoiceDate** column header
2. **Home** → **Data Type** → Select **Date**
3. Click **Replace** when prompted
4. New Applied Step: "Changed Type"

Repeat for other columns as needed:
- **Quantity** → Number
- **UnitPrice** → Decimal Number
- **Country** → Text

**Result:** Correct data types for calculations

---

#### Step 5: Review Applied Steps
On the right side, you should see:
```
Applied Steps
├─ Source
├─ Removed Duplicates
├─ Removed Blank Rows
├─ Changed Type (InvoiceDate)
├─ Changed Type (Quantity)
└─ Changed Type (UnitPrice)
```

**Click any step** to see data at that point!

---

#### Step 6: Load Cleaned Data
1. **Home** → **Close & Apply**
2. Power BI loads cleaned data
3. You're back in Power BI main view

**Result:** Clean data ready for analysis!

---

#### Step 7: Compare Before & After
Take 2 screenshots:
- `Day_2_Task_2_Before_Cleaning.png` (raw data)
- `Day_2_Task_2_After_Cleaning.png` (cleaned data)

Note the difference!

---

### Reflection Questions
1. How many rows were removed as duplicates?
2. How many blank rows were deleted?
3. What data types did you change?
4. Why is changing data type important?

---

## TASK 3: ADVANCED TRANSFORMATIONS (HARD)
**Duration:** 40-50 minutes
**Difficulty:** ⭐⭐⭐ Hard
**What you'll learn:** Complex Power Query operations

### Objective
Apply advanced transformations: split columns, replace values, create custom columns.

### Step-by-Step Instructions

#### Step 1: Open Power Query Again
1. Right-click table → **Edit query**
2. Power Query Editor opens

#### Step 2: Split a Column (if applicable)
If you have a column like "Customer Name" that should be "First Name" + "Last Name":

1. Right-click **Customer Name** column
2. **Transform** → **Split Column** → **By Delimiter**
3. Choose **Space** as delimiter
4. Click **OK**

**Result:** 1 column becomes 2 columns (FirstName, LastName)

---

#### Step 3: Replace Invalid Values
If you have bad values like "N/A", "-", or incorrect text:

1. Click the column with bad values
2. **Home** → **Replace Values**
3. **Value To Find:** "N/A"
4. **Replace With:** (leave blank or 0)
5. Click **OK**

**Result:** Bad values replaced with clean values

---

#### Step 4: Create Custom Column (Optional Advanced)
If you want to calculate something new:

1. **Add Column** tab → **Custom Column**
2. **Column Name:** "TransactionYear"
3. **Custom Column Formula:**
   ```
   = Date.Year([InvoiceDate])
   ```
4. Click **OK**

**Result:** New column with extracted year

---

#### Step 5: Filter Out Unwanted Data
If you want to exclude test records or specific data:

1. Click column you want to filter
2. Click the **filter icon** in column header
3. Uncheck items you don't want (e.g., uncheck "TEST" if that's test data)
4. Click **OK**

**Result:** Only desired data remains

---

#### Step 6: Review All Applied Steps
Your Applied Steps might now look like:
```
Applied Steps
├─ Source
├─ Removed Duplicates
├─ Removed Blank Rows
├─ Changed Type (multiple)
├─ Split Column
├─ Replaced Value
├─ Added Custom Column
└─ Filtered Rows
```

**Each step is reversible!** Click any step to backtrack.

---

#### Step 7: Save & Load
1. **Home** → **Close & Apply**
2. Cleaned, transformed data loads in Power BI

#### Step 8: Take Final Screenshot
Screenshot of Power Query Editor showing:
- Final data
- All Applied Steps visible on right
Save as: `Day_2_Task_3_Applied_Steps.png`

---

### Reflection Questions
1. Which transformation saved you the most manual work?
2. What happens if you click an earlier Applied Step?
3. How would you reuse this query for next week's data?
4. What other transformations might be useful?

---

## TASK COMPLETION CHECKLIST

### Task 1: Load & Explore
- [ ] Loaded messy dataset
- [ ] Identified 5 data quality issues
- [ ] Took screenshot of raw data
- [ ] Answered reflection questions

**Time spent:** _____ minutes
**Confidence:** ⭐⭐⭐⭐⭐

---

### Task 2: Clean Data
- [ ] Removed duplicates
- [ ] Removed blank rows
- [ ] Changed data types (4+ columns)
- [ ] Reviewed Applied Steps
- [ ] Loaded cleaned data
- [ ] Took before/after screenshots

**Time spent:** _____ minutes
**Confidence:** ⭐⭐⭐⭐⭐

---

### Task 3: Advanced Transformations
- [ ] Split column (if applicable)
- [ ] Replaced invalid values
- [ ] Created custom column (or filtered)
- [ ] Applied all transformations
- [ ] Reviewed complete Applied Steps
- [ ] Took final screenshot

**Time spent:** _____ minutes
**Confidence:** ⭐⭐⭐⭐⭐

---

## TROUBLESHOOTING

### Problem: "Applied Steps panel not visible"
**Solution:** 
- Right side of Power Query Editor should show it
- If hidden, click View → Applied Steps

---

### Problem: "Can't change data type"
**Solution:**
- Some columns have mixed types (text & numbers)
- First use Home → Replace Values to clean
- Then change type

---

### Problem: "Remove Duplicates removes too much"
**Solution:**
- Select specific columns (not all)
- Right-click column → Remove Duplicates
- Only removes exact duplicates in those columns

---

### Problem: "Lost my changes"
**Solution:**
- Click earlier Applied Step to see data at that point
- You can undo by deleting steps
- Always save PBIX before closing

---

## KEY LEARNINGS TODAY

You've learned:
1. ✅ How to identify data quality issues
2. ✅ How to use Power Query for cleaning
3. ✅ How Applied Steps work & are reversible
4. ✅ Basic transformations (remove, split, replace)
5. ✅ How to handle different data types

**This is foundational work!** Everything depends on clean data.

---

## NEXT: SAVE YOUR WORK

1. **File** → **Save**
2. Save as: `Day_2_Power_Query_Practice.pbix`
3. Location: `01_Week_1_Beginner/Day_2_Power_Query/Projects/`

---

## FINAL NOTES

**Remember:**
- ❌ Don't overthink it - just follow steps
- ❌ Don't worry about M language yet - visual tools are enough
- ✅ Do experiment - click around, see what happens
- ✅ Do save often - in case of crashes
- ✅ Do ask questions - Power Query is deep!

**You're now a data cleaner!** 🧹✨