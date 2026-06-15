# 📊 Journey Analytics Dashboard - Complete Setup Guide

## Overview
This guide shows you how to:
1. Create a GitHub repository
2. Upload your HTML dashboard and data files
3. Enable GitHub Pages (free hosting)
4. Update your data every month from Excel
5. Generate automatic reports

---

## ✅ Step 1: Create a GitHub Account & Repository

### If you don't have GitHub:
1. Go to **https://github.com**
2. Click "Sign up"
3. Create a free account
4. Verify your email

### Create a New Repository:
1. Log in to GitHub
2. Click the **"+" icon** (top right) → **New repository**
3. Repository name: `analytics-dashboard` (or any name)
4. Description: "Monthly Journey Analytics Reports"
5. Select **Public** (so it can be accessed by your website)
6. ✅ Check **"Add a README file"**
7. Click **"Create repository"**

---

## 📁 Step 2: Upload Your Files to GitHub

### Method A: Using GitHub Web Interface (Easiest)

**Upload the HTML Dashboard:**
1. Go to your repository
2. Click **"Add file"** → **"Create new file"**
3. Name it: `index.html`
4. Copy & paste the HTML code from `index.html` file
5. Scroll down → Click **"Commit new file"**

**Upload the Data File:**
1. Click **"Add file"** → **"Upload files"**
2. Select the `data.json` file from your computer
3. Click **"Commit changes"**

### Method B: Using Git Desktop (Faster for recurring updates)

**Install Git Desktop:**
1. Download from: https://desktop.github.com
2. Install and login with your GitHub account
3. Click **"Clone a repository"**
4. Select your `analytics-dashboard` repository
5. Choose where to save it on your computer

**To add/update files:**
1. Copy `index.html` and `data.json` to the folder
2. In Git Desktop, you'll see the files listed
3. Click **"Commit to main"**
4. Click **"Push origin"**

---

## 🌐 Step 3: Enable GitHub Pages (Free Hosting)

### Activate GitHub Pages:
1. Go to your repository
2. Click **Settings** (top right)
3. Click **"Pages"** (left sidebar)
4. Under "Source", select **"main"** branch
5. Click **Save**
6. Wait 1-2 minutes for deployment
7. Your site will be live at: `https://YOUR-USERNAME.github.io/analytics-dashboard/`

**Important:** Update the repository name in `index.html`:
- Line 34: Change `YOUR-USERNAME/YOUR-REPO-NAME` to your actual values
- Example: `john-doe/analytics-dashboard`

---

## 📊 Step 4: Prepare Your Excel Data for Upload

### Format Your Data (Important!)

Use this exact format in Excel:

| Journey Name | Journey ID | Node ID | Node Name (OS / Type) | Deliver Rate - March | Viewed Count - March | Click - March | Conversion - March | ... (repeat for other months) |
|---|---|---|---|---|---|---|---|---|
| 1.0 [LBS] User SignUp | 123 | 4 | Push #1 | 95.50 | 71.43 | 1.60 | 4.65 | ... |
| 2.0 [LBS] User Login | 124 | 5 | Email | 98.20 | 85.30 | 3.45 | 6.20 | ... |

### Convert Excel to JSON (3 Methods)

#### **Method 1: Easy - Use Online Tool (Recommended)**
1. Go to: **https://www.convertcsv.com/csv-to-json.htm**
2. Copy your Excel data (Ctrl+A → Ctrl+C)
3. Paste into the website
4. Click **"Convert"**
5. Copy the JSON output
6. Update your GitHub `data.json` file (see Step 5)

#### **Method 2: Manual - Using Excel "Save As"**
1. Open your Excel file
2. **File** → **Save As**
3. Format: **CSV (Comma delimited) (.csv)**
4. Save as `data.csv`
5. Use the online converter above to convert CSV to JSON

#### **Method 3: Python Script (Advanced)**
```python
import pandas as pd
import json

# Read Excel file
df = pd.read_excel('your_data.xlsx')

# Convert to JSON
data = df.to_dict('records')

# Save JSON
with open('data.json', 'w') as f:
    json.dump(data, f, indent=2)
```

---

## 🔄 Step 5: Update Your Data Every Month

### Monthly Update Process:

**1. Prepare your data in Excel** (following the format above)

**2. Convert to JSON:**
   - Use the online converter: https://www.convertcsv.com/csv-to-json.htm
   - Copy the Excel data → Convert → Get JSON

**3. Update on GitHub:**

#### Using Web Interface:
1. Go to your repository
2. Click on `data.json` file
3. Click the **pencil icon** (Edit file)
4. Delete the old content
5. Paste your new JSON data
6. Scroll down → Click **"Commit changes"**

#### Using Git Desktop:
1. Open the `data.json` file in a text editor (Notepad, VS Code)
2. Replace the content with your new JSON data
3. Save the file
4. In Git Desktop, click **"Commit to main"**
5. Click **"Push origin"**

---

## 🎯 Step 6: View Your Dashboard

1. Go to: `https://YOUR-USERNAME.github.io/analytics-dashboard/`
2. Your data will automatically load
3. Click **"Refresh Data"** to reload if you updated the data

---

## ❓ Troubleshooting

### "Data file not found" Error
- **Problem:** The `data.json` file path is wrong
- **Solution:** 
  1. Check repository name matches in `index.html` line 34
  2. Make sure `data.json` exists in the repository
  3. Wait 5 minutes after uploading for GitHub Pages to update

### Data Not Showing
- **Problem:** JSON format is incorrect
- **Solution:** 
  1. Validate JSON at: https://jsonlint.com/
  2. Make sure column names match exactly (case-sensitive)
  3. Check that numbers are valid (no special characters)

### GitHub Pages Not Working
- **Problem:** Site shows 404 error
- **Solution:**
  1. Go to **Settings** → **Pages**
  2. Verify "Source" is set to "main" branch
  3. Verify `index.html` is in the root folder
  4. Wait 2-3 minutes for deployment

### How to Get Your GitHub API (Not needed for this setup, but for reference)

This dashboard uses **direct file access**, so you don't need an API key. But if you want one for future features:

1. Go to: https://github.com/settings/tokens
2. Click **"Generate new token"** → **"Generate new token (classic)"**
3. Name: `analytics-dashboard`
4. Select scopes: **repo** (full control)
5. Click **"Generate token"**
6. Copy and save the token safely (you won't see it again)
7. Use it in your code: `Authorization: token YOUR-TOKEN`

---

## 📋 Your Monthly Checklist

Every month, follow this:

- [ ] **Prepare Excel with new data**
  - Add columns for the new month
  - Calculate/enter metrics (Deliver Rate, View Ratio, Click Ratio, Conversion Ratio)

- [ ] **Convert to JSON**
  - Use: https://www.convertcsv.com/csv-to-json.htm
  - Copy Excel → Convert → Get JSON

- [ ] **Update GitHub**
  - Upload/update `data.json` file
  - Verify file is saved correctly

- [ ] **Verify Dashboard**
  - Visit your website
  - Click "Refresh Data"
  - Check that all numbers appear correctly

---

## 🎓 Understanding Your Data Format

### Column Names (Must be EXACT):
```
"Journey Name" - Name of the customer journey
"Journey ID" - Unique ID for the journey
"Node ID" - ID of the node in the journey
"Node Name (OS / Type)" - Channel type (Email, Push, SMS, etc.)
"Deliver Rate - [Month]" - Percentage of messages delivered
"Viewed Count - [Month]" - Percentage of messages viewed
"Click - [Month]" - Percentage of messages clicked
"Conversion - [Month]" - Percentage of messages that converted
```

### Example Row:
```json
{
  "Journey Name": "1.0 [LBS] User SignUp",
  "Journey ID": "123",
  "Node ID": "4",
  "Node Name (OS / Type)": "Push #1",
  "Deliver Rate - March": "95.50",
  "Viewed Count - March": "71.43",
  "Click - March": "1.60",
  "Conversion - March": "4.65"
}
```

---

## 🚀 Quick Start Summary

```
1. Create GitHub Account → https://github.com
2. Create Repository → `analytics-dashboard`
3. Upload `index.html` → Your dashboard
4. Upload `data.json` → Your data
5. Enable GitHub Pages → Settings → Pages → main branch
6. Visit → https://YOUR-USERNAME.github.io/analytics-dashboard/
7. Every month: Update data.json + Push to GitHub
```

---

## 📞 Support Resources

- **GitHub Help:** https://docs.github.com
- **JSON Validator:** https://jsonlint.com/
- **CSV to JSON Converter:** https://www.convertcsv.com/csv-to-json.htm
- **GitHub Pages Guide:** https://pages.github.com

---

## ✨ Advanced Features (Optional)

### Auto-Calculate Ratios
If you want the dashboard to calculate ratios automatically:
- Provide raw counts instead of percentages
- Modify the `updateStats()` function in `index.html`
- Add calculation logic: `(clicks / views) * 100`

### Add More Metrics
1. Edit `data.json` to include new columns
2. Update the JavaScript in `index.html` to reference new columns
3. Add new chart if needed

### Custom Branding
Edit these lines in `index.html`:
- Line 6: Change `<title>` for browser tab name
- Line 12: Change gradient colors (look for `#667eea` and `#764ba2`)
- Line 55: Change dashboard title

---

**Happy Reporting! 📊**
