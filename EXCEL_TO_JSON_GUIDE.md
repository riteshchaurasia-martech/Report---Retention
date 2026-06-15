# 🔄 Excel to JSON Conversion - Quick Guide

## Your Excel Data (Example)

```
Journey Name          | Journey ID | Node ID | Node Name     | Deliver Rate-March | Viewed Count-March | Click-March | Conversion-March
1.0 [LBS] User SignUp | 123        | 4       | Push #1       | 95.50             | 71.43             | 1.60        | 4.65
2.0 [LBS] User Login  | 124        | 5       | Email         | 98.20             | 85.30             | 3.45        | 6.20
```

---

## ⚡ FASTEST METHOD (30 seconds)

### Step 1: Copy Your Excel Data
- Select all your data in Excel (Ctrl+A)
- Copy it (Ctrl+C)

### Step 2: Use Online Converter
- Go to: **https://www.convertcsv.com/csv-to-json.htm**
- Paste your data into the text box
- Click "Convert"

### Step 3: Copy JSON Output
- Copy the JSON result
- Paste into your `data.json` file on GitHub

---

## 📝 What the JSON Should Look Like

Your Excel table converts to this JSON format:

```json
[
  {
    "Journey Name": "1.0 [LBS] User SignUp",
    "Journey ID": "123",
    "Node ID": "4",
    "Node Name (OS / Type)": "Push #1",
    "Deliver Rate - March": "95.50",
    "Viewed Count - March": "71.43",
    "Click - March": "1.60",
    "Conversion - March": "4.65",
    "Deliver Rate - April": "96.20",
    "Viewed Count - April": "72.15",
    "Click - April": "1.85",
    "Conversion - April": "4.90"
  },
  {
    "Journey Name": "2.0 [LBS] User Login",
    "Journey ID": "124",
    "Node ID": "5",
    "Node Name (OS / Type)": "Email",
    "Deliver Rate - March": "98.20",
    "Viewed Count - March": "85.30",
    "Click - March": "3.45",
    "Conversion - March": "6.20",
    "Deliver Rate - April": "98.50",
    "Viewed Count - April": "86.10",
    "Click - April": "3.65",
    "Conversion - April": "6.50"
  }
]
```

---

## ✋ IMPORTANT RULES

1. **Column Names Must Match Exactly:**
   - ✅ Correct: `"Deliver Rate - March"`
   - ❌ Wrong: `"Deliver Rate March"` (missing hyphen)
   - ❌ Wrong: `"deliver rate - march"` (wrong case)

2. **Numbers Must Be Strings (In Quotes):**
   - ✅ Correct: `"95.50"`
   - ❌ Wrong: `95.50` (no quotes)

3. **All Rows Must Have Same Columns:**
   - Every journey must have data for all months
   - If data missing, use `null` or `""`

4. **Special Characters:**
   - If your text contains quotes: use `\"` or change to single quotes
   - Example: `"Node Name: \"Push #1\""`

---

## 🔍 Validate Your JSON

Before uploading to GitHub:

1. Copy your JSON
2. Go to: **https://jsonlint.com/**
3. Paste your JSON
4. If green checkmark → ✅ Ready to upload
5. If red error → ❌ Fix the format

---

## 💾 Monthly Update Workflow

### Every Month (Takes 5 minutes):

```
1. Add new columns to Excel for the new month
   Example: "Deliver Rate - April", "Viewed Count - April", etc.

2. Fill in your data

3. Select all data → Copy (Ctrl+C)

4. Go to https://www.convertcsv.com/csv-to-json.htm

5. Paste data → Click "Convert" → Copy JSON

6. Open data.json on GitHub

7. Replace old content with new JSON

8. Commit changes

9. Wait 1 minute, visit your dashboard

10. Click "Refresh Data" - Done! 🎉
```

---

## 🎓 Understanding Each Column

| Column | Description | Example |
|--------|-------------|---------|
| Journey Name | Name of the customer journey | "1.0 [LBS] User SignUp" |
| Journey ID | Unique journey identifier | "123" |
| Node ID | Node/step within journey | "4" |
| Node Name (OS / Type) | Channel type | "Push #1", "Email", "SMS" |
| Deliver Rate | % successfully delivered | "95.50" |
| Viewed Count | % messages viewed | "71.43" |
| Click | % links clicked | "1.60" |
| Conversion | % led to conversion | "4.65" |

---

## 📊 Real Excel Data Example

Here's what your Excel file should look like:

```
Row 1 (Headers):
A: Journey Name
B: Journey ID
C: Node ID
D: Node Name (OS / Type)
E: Deliver Rate - March
F: Viewed Count - March
G: Click - March
H: Conversion - March
I: Deliver Rate - April
J: Viewed Count - April
... and so on

Row 2 (Data):
A: 1.0 [LBS] User SignUp
B: 123
C: 4
D: Push #1
E: 95.50
F: 71.43
G: 1.60
H: 4.65
I: 96.20
J: 72.15
... and so on

Row 3 (More Data):
A: 2.0 [LBS] User Login
B: 124
... etc
```

---

## ❗ Common Mistakes & How to Fix

### ❌ Mistake #1: Wrong Column Names
```json
// WRONG
{
  "Deliver Rate March": "95.50"  // Missing hyphen and "Month" format
}

// CORRECT
{
  "Deliver Rate - March": "95.50"
}
```

### ❌ Mistake #2: Numbers Without Quotes
```json
// WRONG
{
  "Deliver Rate - March": 95.50  // Number, not string
}

// CORRECT
{
  "Deliver Rate - March": "95.50"  // String with quotes
}
```

### ❌ Mistake #3: Missing Months for New Data
```json
// WRONG
{
  "Journey Name": "User SignUp",
  "Deliver Rate - March": "95.50"
  // Missing April, May data!
}

// CORRECT
{
  "Journey Name": "User SignUp",
  "Deliver Rate - March": "95.50",
  "Deliver Rate - April": "96.20",
  "Deliver Rate - May": "97.10"
}
```

---

## 🛠️ Troubleshooting

### "JSON is invalid" Error
1. Check for missing quotes around text values
2. Check for missing commas between key-value pairs
3. Verify column names are EXACTLY spelled correctly
4. Use https://jsonlint.com/ to find the exact error

### Dashboard Shows Empty Table
1. Go to https://jsonlint.com/
2. Validate your `data.json`
3. Check column names in JSON match what's in `index.html`
4. Refresh browser (Ctrl+F5 on Windows, Cmd+Shift+R on Mac)

### "Data loaded successfully" but table is empty
1. The JSON format is valid but column names might be slightly different
2. Compare your JSON column names with the examples above
3. Update data.json with correct column names

---

## ✨ Pro Tips

1. **Keep a Template:** Save your Excel file format as a template for next month
2. **Auto-Format:** Use Excel's table feature for consistent formatting
3. **Quick Validate:** Before converting, check that:
   - All rows have the same number of columns
   - No empty cells that should have values
   - Numbers are consistent (no text like "N/A")
4. **Backup:** Keep a copy of your monthly data before updating GitHub

---

## 📋 Checklist Before Uploading

- [ ] All columns have correct names (with hyphens and spaces)
- [ ] All values are in quotes (numbers as strings)
- [ ] JSON is valid (tested on jsonlint.com)
- [ ] All rows have the same columns
- [ ] Numbers are percentages (0-100)
- [ ] Journey data is complete (no blank rows)

---

**You're all set! Happy updating! 📊**
