# Report---Retention
# 📊 Journey Analytics Dashboard

A beautiful, free, self-updating analytics dashboard that automatically calculates and displays your journey metrics with charts and reports.

![Dashboard Features](https://img.shields.io/badge/Features-Charts%2C%20Tables%2C%20Auto--Calculate-blue)
![Hosting](https://img.shields.io/badge/Hosting-GitHub%20Pages%20(FREE)-green)
![Data](https://img.shields.io/badge/Data-JSON-orange)

---

## ✨ Features

- 📊 **Beautiful Dashboard** - Professional analytics interface
- 📈 **Auto-Calculated Metrics** - View Ratio, Click Ratio, Conversion Ratio
- 📉 **Interactive Charts** - Visualize trends across months
- 📋 **Detailed Table** - See all metrics in one place
- 🔄 **Easy Updates** - Add monthly data with simple JSON file
- 🚀 **Free Hosting** - GitHub Pages (no costs!)
- 📱 **Responsive Design** - Works on mobile, tablet, desktop
- ⚡ **Real-time Sync** - Updates automatically when you push new data

---

## 📁 Project Structure

```
your-repo/
├── index.html          # Main dashboard (your website)
├── data.json          # Monthly data file (you update this)
├── README.md          # Project info (this file)
├── SETUP_GUIDE.md     # Complete setup instructions
└── EXCEL_TO_JSON_GUIDE.md  # How to convert Excel data
```

---

## 🚀 Quick Start (5 minutes)

### 1. Create GitHub Account & Repo
```
- Sign up at github.com
- Create new repository: "analytics-dashboard"
- Choose "Public"
```

### 2. Upload Files
```
- Upload index.html (your dashboard)
- Upload data.json (your monthly data)
```

### 3. Enable GitHub Pages
```
Settings → Pages → Select "main" branch → Save
```

### 4. Visit Your Dashboard
```
https://YOUR-USERNAME.github.io/analytics-dashboard/
```

---

## 📊 What You'll See

### Dashboard Includes:

1. **Summary Stats**
   - Total Journeys
   - Average Deliver Rate
   - Average View Ratio
   - Average Click Ratio

2. **Interactive Charts**
   - Deliver Rate by Journey (bar chart)
   - View Ratio Trends (line chart)
   - Click Ratio Trends (line chart)
   - Conversion Ratio Trends (line chart)

3. **Detailed Data Table**
   - All journeys and nodes
   - Metrics for each month
   - Organized by metric type
   - Color-coded by month

---

## 📝 How to Update Your Data

### Every Month:

**1. Prepare Your Data in Excel**
```
Columns: Journey Name, Journey ID, Node ID, Node Name, 
         Deliver Rate-March, Viewed Count-March, Click-March, 
         Conversion-March, ... (repeat for other months)
```

**2. Convert to JSON** (Using https://www.convertcsv.com/csv-to-json.htm)
```
- Copy Excel data
- Paste into converter
- Click "Convert"
- Copy JSON output
```

**3. Update GitHub**
```
- Go to data.json in your repo
- Click edit (pencil icon)
- Replace with new JSON
- Commit changes
```

**4. Refresh Dashboard**
```
- Visit your website
- Click "Refresh Data"
- Done! ✅
```

---

## 📖 Data Format

### Excel Structure:
```
Journey Name       | Journey ID | Node ID | Node Name | Deliver-March | Viewed-March | Click-March | Conversion-March
User SignUp        | 123        | 4       | Push #1   | 95.50         | 71.43        | 1.60        | 4.65
User Login         | 124        | 5       | Email     | 98.20         | 85.30        | 3.45        | 6.20
```

### JSON Structure:
```json
[
  {
    "Journey Name": "User SignUp",
    "Journey ID": "123",
    "Node ID": "4",
    "Node Name (OS / Type)": "Push #1",
    "Deliver Rate - March": "95.50",
    "Viewed Count - March": "71.43",
    "Click - March": "1.60",
    "Conversion - March": "4.65"
  }
]
```

---

## 🔧 How It Works

### Frontend (index.html)
- **HTML**: Structure of dashboard
- **CSS**: Styling and layout
- **JavaScript**: 
  - Fetches data.json from GitHub
  - Calculates statistics
  - Renders charts using Chart.js
  - Displays table with formatted data

### Backend (data.json)
- Stores your monthly metrics
- JSON format for easy parsing
- Automatically loaded by the dashboard
- No database or API required

---

## 🎨 Customization

### Change Dashboard Colors
Edit these lines in `index.html`:
```javascript
// Line 12 - Change gradient
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

// Line 114 - Stat cards gradient
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Dashboard Title
Edit line 55 in `index.html`:
```html
<h1>📊 Journey Analytics Dashboard</h1>
```

### Add New Metrics
1. Add columns to `data.json`
2. Update the chart code in `index.html`
3. Add references in JavaScript

---

## ❓ Troubleshooting

### "Data file not found"
- Verify `data.json` exists in repo
- Check repository name in `index.html` line 34
- Wait 5 minutes for GitHub Pages to update

### Dashboard shows empty table
- Validate JSON at https://jsonlint.com/
- Check column names match exactly (case-sensitive)
- Verify numbers are in quotes: `"95.50"` not `95.50`

### Charts not showing
- Refresh browser (Ctrl+F5)
- Check browser console for errors (F12)
- Verify data.json has valid JSON format

### GitHub Pages 404 error
- Go to Settings → Pages
- Ensure "Source" is set to "main" branch
- Verify `index.html` is in root folder
- Wait 2-3 minutes for deployment

---

## 📚 Guides Included

1. **SETUP_GUIDE.md**
   - Complete step-by-step setup instructions
   - GitHub account creation
   - Repository setup
   - GitHub Pages activation
   - Monthly update process
   - Troubleshooting

2. **EXCEL_TO_JSON_GUIDE.md**
   - How to convert Excel to JSON
   - Data format specifications
   - Validation steps
   - Common mistakes and fixes

---

## 🆓 Free Tools Used

- **GitHub** - Free repository & hosting
- **GitHub Pages** - Free website hosting
- **Chart.js** - Free charting library
- **Online Converters** - Free Excel to JSON conversion

---

## 📊 Metrics Explained

| Metric | Description | Example |
|--------|-------------|---------|
| **Deliver Rate** | % of messages successfully delivered | 95.50% |
| **Viewed Count** | % of delivered messages that were viewed | 71.43% |
| **Click** | % of viewed messages that had links clicked | 1.60% |
| **Conversion** | % of clicks that led to conversion | 4.65% |

---

## 🔐 Data Privacy

- Your data stays in your GitHub repository
- Only you can edit the repository
- Data is not sent to any external service
- Everything is open-source and transparent

---

## 🚀 Future Enhancements

Optional features you could add:
- [ ] Authentication (password protection)
- [ ] Download reports as PDF
- [ ] Email notifications on data updates
- [ ] Automated data backup
- [ ] Historical comparison
- [ ] Advanced filtering

---

## 📞 Support

- **GitHub Docs**: https://docs.github.com
- **GitHub Pages**: https://pages.github.com
- **Chart.js Docs**: https://www.chartjs.org
- **JSON Validator**: https://jsonlint.com

---

## 💡 Tips

1. **Template Excel File**
   - Save your Excel format as template
   - Reuse monthly with new data

2. **Version Control**
   - GitHub tracks all changes
   - You can see history of updates
   - Easy to revert if needed

3. **Regular Updates**
   - Update every month on same date
   - Keep data consistent
   - Monitor trends over time

4. **Share Dashboard**
   - Send your GitHub Pages URL to team
   - No login required (public repo)
   - Real-time viewing

---

## 📄 License

This project is open-source and free to use.

---

## 🎉 You're All Set!

Your analytics dashboard is ready to use. Follow the **SETUP_GUIDE.md** for complete instructions.

**Questions?** Check the troubleshooting section or guides.

**Happy Analytics! 📊**

---

*Last Updated: 2024*
*Version: 1.0*
