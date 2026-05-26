# DAY 2: POWER QUERY BASICS
## Complete Learning Guide

---

## 🎯 TODAY'S OBJECTIVES

By end of Day 2, you will understand:
- [ ] What Power Query is and why it's critical
- [ ] The difference between Power Query and DAX
- [ ] Common data cleaning tasks (duplicates, blanks, types)
- [ ] How to create and modify queries
- [ ] Applied Steps and how to navigate them
- [ ] Query Folding concept
- [ ] Real-world data transformation scenarios

**Time commitment:** 2-3 hours (including hands-on tasks)

---

## SECTION 1: WHAT IS POWER QUERY?

### Simple Definition
Power Query is **the ETL tool in Power BI** that:
- **E**xtracts data from sources
- **T**ransforms (cleans & shapes) data
- **L**oads data into Power BI model

### Why It Matters
**The 80/20 Rule:**
- 80% of BI work is data cleaning
- 20% is visualization & analysis

Power Query saves hundreds of hours by automating the 80%.

---

## SECTION 2: POWER QUERY VS DAX

### Key Difference

| Aspect | Power Query | DAX |
|--------|-------------|-----|
| **When** | Before loading data | After data is loaded |
| **Purpose** | Clean & transform | Calculate & analyze |
| **Example** | Remove duplicates | Calculate profit margin |
| **Language** | M (visual/code) | DAX formulas |
| **Runs on** | Source system or Power BI | Power BI model |

### Mental Model
```
Raw Data
   ↓
Power Query ← "Make data clean"
   ↓
Clean Data
   ↓
DAX ← "Calculate insights"
   ↓
Business Metrics
```

---

## SECTION 3: THE DATA CLEANING CHALLENGE

### Scenario: Messy Sales Data
Imagine you get a CSV file:

```
Customer,Product,Amount,Date,Notes
JOHN DOE,Laptop,$1200,2024-01-15,Good customer
john doe,LAPTOP,1200,01/15/2024,
John Doe,Laptop,$1200.00,1/15/2024,Good customer
JANE SMITH,Phone,,2024-01-16,
jane smith,Phone,$800,01/16/2024,High value
```

**Problems:**
- Inconsistent capitalization (JOHN, john, John)
- Inconsistent product names (LAPTOP, Laptop)
- Inconsistent amount formats ($1200, 1200, $1200.00)
- Inconsistent date formats (2024-01-15, 01/15/2024, 1/15/2024)
- Missing values (empty Amount for JANE)
- Duplicate rows

**Without Power Query:** Manual cleanup in Excel = 4-6 hours
**With Power Query:** Click button to clean = 15 minutes

---

## SECTION 4: COMMON POWER QUERY TASKS

### Task 1: Remove Duplicates
**Problem:** Same customer appears twice
**Solution:** Power Query → Remove Duplicates
**Result:** Clean customer list

---

### Task 2: Remove Blank Rows
**Problem:** Empty rows between data
**Solution:** Filter out blanks
**Result:** Only valid rows remain

---

### Task 3: Change Data Types
**Problem:** Dates stored as text, numbers as text
**Solution:** Change column type to Date, Number
**Result:** Correct data types for calculations

---

### Task 4: Split Columns
**Problem:** "John Doe" in one column, need separate First/Last
**Solution:** Split by delimiter (space)
**Result:** FirstName, LastName columns

---

### Task 5: Merge/Combine Data
**Problem:** Customer data in one table, Orders in another
**Solution:** Merge tables on CustomerID
**Result:** Combined customer + order data

---

### Task 6: Handle Null/Blank Values
**Problem:** Missing values in Amount column
**Solution:** Replace nulls with 0 or remove rows
**Result:** No gaps in data

---

### Task 7: Standardize Text
**Problem:** "JOHN", "john", "John" inconsistent
**Solution:** Apply Text.Proper() function
**Result:** Consistent capitalization

---

## SECTION 5: APPLIED STEPS

### What Are Applied Steps?
Power Query **records every transformation** you make.

### Visual Example
```
Source (Original data from CSV)
   ↓
Removed Duplicates (Step 1)
   ↓
Changed Column Type (Step 2)
   ↓
Removed Blanks (Step 3)
   ↓
Split Columns (Step 4)
   ↓
Final Result (Ready for Power BI)
```

### Key Benefit
You can **click any step** to see data at that point. Easy to debug!

---

## SECTION 6: QUERY FOLDING

### What Is Query Folding?
Whether Power Query runs transformation on **source system** (fast) or **in Power BI** (slow).

### Example

**Folds (fast):**
```
Filter data where Amount > 1000
→ SQL Server processes it → only 5K rows sent to Power BI
```

**Doesn't Fold (slow):**
```
Filter data with custom function
→ All 500K rows sent to Power BI → Power BI filters it
```

### Why It Matters
Query Folding = faster refresh times = better performance

---

## SECTION 7: REAL-WORLD SCENARIO

### You Receive This Every Week:
A CSV file with:
- 50K+ transaction records
- Multiple data quality issues
- Inconsistent formats
- Missing values

### Without Power Query
```
Open Excel → Sort by Customer → Find duplicates → Manually remove
→ Fix capitalization → Convert dates → 4+ hours of work
→ Repeat every week = 200+ hours/year
```

### With Power Query
```
Set up once → Click "Refresh" → Done in 30 seconds
→ Repeat every week = 15 minutes/year
→ Save 185+ hours/year!
```

---

## SECTION 8: POWER QUERY INTERFACE

In Power BI Desktop:

```
┌─────────────────────────────────────┐
│  Home Tab                            │
│  ├─ Get Data (load data)            │
│  ├─ Recent Sources                  │
│  └─ Refresh                         │
│                                      │
│  Transform Tab (appears after data) │
│  ├─ Remove Duplicates               │
│  ├─ Remove Errors                   │
│  ├─ Change Type                     │
│  ├─ Split Column                    │
│  ├─ Replace Values                  │
│  └─ [Many more options]             │
└─────────────────────────────────────┘
```

---

## SECTION 9: M LANGUAGE (Optional)

Power Query has 2 ways to work:

### Method 1: Visual (No Coding)
- Click buttons in ribbon
- No coding needed
- Good for basic transformations

### Method 2: M Language (Advanced)
- Write formulas (like DAX but different)
- More control
- For complex transformations

**For Day 2:** We'll use Visual method (Method 1)

---

## SECTION 10: BEST PRACTICES

### ✅ DO THIS
1. **Load raw data first** - Don't clean before Power Query
2. **Document assumptions** - Why did you remove rows?
3. **Test on sample** - Try transformation on small dataset first
4. **Save queries** - You can reuse for next data load
5. **Monitor performance** - Check refresh time

### ❌ DON'T DO THIS
1. **Clean in Excel first** - Power Query can do it faster
2. **Delete source data** - Keep original for auditing
3. **Make assumptions** - Ask if unsure what data means
4. **Mix transformations** - One step at a time
5. **Forget to save** - Regularly save your PBIX file

---

## KEY TAKEAWAYS

By now you should know:

1. **What:** Power Query cleans & transforms data
2. **Why:** 80% of BI work is data prep
3. **When:** Before loading into Power BI model
4. **How:** Using visual tools or M language
5. **Impact:** Saves hours of manual work

---

## GLOSSARY

| Term | Definition |
|------|-----------|
| **ETL** | Extract-Transform-Load process |
| **Applied Steps** | Record of all transformations |
| **Query Folding** | When transformation happens at source |
| **Duplicate** | Same row appears multiple times |
| **Null/Blank** | Missing value in a field |
| **Data Type** | What kind of data (text, number, date, etc.) |
| **Transform** | Change or clean data |
| **Source** | Where data comes from |
| **M Language** | Programming language for Power Query |

---

## READY FOR HANDS-ON?

Now let's get practical with real data transformation tasks!

Move to: **Day_2_Hands_On_Tasks.md**