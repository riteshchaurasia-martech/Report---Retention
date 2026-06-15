# ✅ Getting Started Checklist

## 📌 Before You Start
- [ ] Have a GitHub account (or sign up at github.com)
- [ ] Have your Excel data ready
- [ ] Have 30 minutes for setup

---

## 🎯 STEP 1: GitHub Repository Setup (5 min)

### 1.1 Create GitHub Repository
```
Step-by-step:
□ Go to github.com (login if needed)
□ Click "+" → "New repository"
□ Name: analytics-dashboard
□ Choose: PUBLIC
□ Check: Add README file
□ Click: Create repository
```

### 1.2 Copy Your Repository URL
```
□ Go to your new repository
□ Click CODE (green button)
□ Copy the HTTPS URL
□ Save it somewhere - you'll need it
```

**Your URL will look like:**
```
https://github.com/YOUR-USERNAME/analytics-dashboard.git
```

---

## 📤 STEP 2: Upload Files (5 min)

### Using GitHub Web (Easiest)

**Upload index.html:**
```
□ In your repository, click "Add file" → "Create new file"
□ Name it: index.html
□ Paste the HTML code
□ Scroll down → "Commit new file"
```

**Upload data.json:**
```
□ Click "Add file" → "Upload files"
□ Select data.json from your computer
□ Click "Commit changes"
```

**Upload other guides:**
```
□ Repeat above for:
   - README.md
   - SETUP_GUIDE.md
   - EXCEL_TO_JSON_GUIDE.md
```

---

## 🌐 STEP 3: Enable GitHub Pages (3 min)

```
□ Go to your repository
□ Click "Settings" (gear icon)
□ Click "Pages" (left sidebar)
□ Under "Source":
  □ Select "main" branch
  □ Click "Save"
□ Wait 1-2 minutes
□ Look for: "Your site is live at: https://..."
```

**Important:** Update line 34 in index.html before enabling Pages:
```javascript
// Change this line with YOUR actual values:
const GITHUB_REPO = 'your-username/analytics-dashboard';
```

---

## 📊 STEP 4: Prepare Your Data (5 min)

### From Excel to JSON:

```
□ Open your Excel file with monthly data
□ Select all data (Ctrl+A)
□ Copy it (Ctrl+C)
□ Go to: https://www.convertcsv.com/csv-to-json.htm
□ Paste your data
□ Click "Convert"
□ Copy the JSON result
□ Paste into GitHub's data.json file
```

**Checklist for your Excel:**
```
Columns: (MUST be exact spelling)
□ Journey Name
□ Journey ID
□ Node ID
□ Node Name (OS / Type)
□ Deliver Rate - March
□ Viewed Count - March
□ Click - March
□ Conversion - March
□ (repeat for other months)
```

---

## ✨ STEP 5: Test Your Dashboard (2 min)

```
□ Visit: https://YOUR-USERNAME.github.io/analytics-dashboard/
□ You should see:
   □ Dashboard header
   □ 4 statistics cards
   □ 4 charts
   □ Data table below
□ Click "Refresh Data" button
□ Verify your data appears in table
□ Check if numbers look correct
```

---

## 🔄 STEP 6: Monthly Updates (5 min)

### Every month, do this:

```
Month: _____________ (e.g., April)

□ Add new columns to Excel:
   "Deliver Rate - April"
   "Viewed Count - April"
   "Click - April"
   "Conversion - April"

□ Fill in your data

□ Convert to JSON:
   1. Select all data in Excel
   2. Copy (Ctrl+C)
   3. Go to https://www.convertcsv.com/csv-to-json.htm
   4. Paste and click Convert
   5. Copy JSON result

□ Update GitHub:
   1. Go to your data.json file
   2. Click edit (pencil icon)
   3. Delete old content
   4. Paste new JSON
   5. Commit changes

□ Refresh dashboard:
   1. Visit your website
   2. Click "Refresh Data"
   3. Verify numbers appear
```

---

## 📋 Monthly Checklist Template

Print this for each month:

```
MONTH: ___________

Data Preparation:
□ Excel file ready with all columns
□ All 4 metrics filled in for each journey
□ No blank cells (use 0 if no data)

Conversion:
□ Excel data copied
□ Converted to JSON (validator shows green)
□ JSON looks correct

GitHub Upload:
□ data.json file updated
□ Commit message added
□ Wait 2 minutes

Testing:
□ Website visited
□ "Refresh Data" clicked
□ All numbers appear in table
□ Charts show new data

Done! ✅
Date completed: _______________
```

---

## 🆘 Troubleshooting Quick Links

If something doesn't work:

```
□ Data not showing?
   → Check: https://jsonlint.com/ to validate JSON
   
□ Website shows 404?
   → Go to Settings → Pages → Verify main branch selected
   
□ Column names not matching?
   → See: EXCEL_TO_JSON_GUIDE.md
   
□ Need complete instructions?
   → See: SETUP_GUIDE.md
   
□ Can't convert Excel to JSON?
   → Use: https://www.convertcsv.com/csv-to-json.htm
```

---

## 📚 Files You Have

```
✅ index.html
   → Your dashboard website
   
✅ data.json
   → Sample data (replace with yours)
   
✅ README.md
   → Project overview
   
✅ SETUP_GUIDE.md
   → Complete step-by-step setup
   
✅ EXCEL_TO_JSON_GUIDE.md
   → How to convert Excel data
   
✅ .gitignore
   → Ignore unnecessary files
```

---

## 🎓 Quick Tips

1. **Keep Your Excel File**
   ```
   Save a template so next month is faster
   ```

2. **Column Names Matter**
   ```
   MUST be exactly: "Deliver Rate - March" (with hyphen and space)
   NOT: "Deliver Rate March" or "DeliverRate-March"
   ```

3. **Validate Before Upload**
   ```
   Always check JSON at https://jsonlint.com/
   This saves hours of debugging!
   ```

4. **Backup Your Data**
   ```
   GitHub keeps history, but keep your Excel safe
   ```

5. **Share Easily**
   ```
   Just send your GitHub Pages URL to anyone
   No login needed (since repo is public)
   ```

---

## 🚀 Success Checklist

When you're done, you should be able to:

```
□ Visit your dashboard at GitHub Pages URL
□ See all your journey data in a table
□ See 4 different charts with trends
□ See summary statistics at top
□ Click "Refresh Data" button
□ Update data monthly without rebuilding
□ Share URL with your team
□ Monitor metrics over time
```

---

## ⏱️ Time Summary

| Task | Time |
|------|------|
| Setup GitHub & Repo | 5 min |
| Upload Files | 5 min |
| Enable GitHub Pages | 3 min |
| Prepare Data | 5 min |
| Test Dashboard | 2 min |
| **Total First Time** | **20 min** |
| Monthly Updates | 5 min |

---

## 🎉 You're Ready!

Follow the steps above and you'll have a professional analytics dashboard in under 30 minutes.

**Questions?** See the detailed guides:
- **SETUP_GUIDE.md** - Full instructions with screenshots
- **EXCEL_TO_JSON_GUIDE.md** - Data format help

**Happy tracking! 📊**
