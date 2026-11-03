# 🏫 Mount Carmel International School – Attendance Register

A simple, lightweight web app for marking and tracking daily student attendance. It runs entirely in the browser as a single HTML file, with no backend, no installation and no database needed.

## ✨ Features

- **Mark Attendance** – Pick a class and date, mark each student Present or Absent, or use "Mark all Present" for a quick start.
- **Student Management** – Add or remove students with roll number, name and class.
- **Date-wise Reports** – View a table of P/A marks for every date, with each student's total Present, total Absent and Attendance %.
- **Colour-coded Attendance %** – Green (90% and above), orange (75–89%) and red (below 75%) for quick scanning.
- **Excel Export** – Download the report for one class, or all classes as separate sheets in one workbook (CSV fallback if the Excel library cannot load).
- **Sample Data Included** – Comes pre-loaded with Class 1 to Class 10, 20 students each, so you can try it right away.
- **Responsive Design** – Works on desktop, tablet and mobile.

## 🚀 Getting Started

1. Download or clone this repository.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).

That's it. No build step required.

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
# then open index.html in your browser
```

> **Note:** An internet connection is needed for Excel (`.xlsx`) export, since the SheetJS library is loaded from a CDN.

## 📖 How to Use

### Mark Attendance
1. Open the **Mark Attendance** tab.
2. Select the **Class** and **Date**.
3. Click **Present** or **Absent** for each student (or **Mark all Present**).
4. Click **Save Attendance**.

### Manage Students
1. Open the **Students** tab.
2. Enter Roll No., Name and Class, then click **Add Student**.
3. Use the class filter to view a class, and **Remove** to delete a student (their attendance records are deleted too).

### View and Export Reports
1. Open the **Reports** tab.
2. Choose a **Class** and a **From / To** date range.
3. Review the table, then click **Excel (this class)** or **Excel (all classes)** to download.

## 💾 Data Storage

All data is saved in your browser's **localStorage**:

| Key | Contents |
|-----|----------|
| `att_students` | List of students |
| `att_records` | Attendance records by date |
| `att_seed_v2` | Flag marking that sample data was loaded |

Things to keep in mind:
- Data stays on the device and browser where it was entered.
- Clearing browser data will erase all records. Export to Excel regularly for backups.
- Data is not shared between devices.

## 🛠️ Tech Stack

- HTML, CSS and vanilla JavaScript (single file)
- [SheetJS (xlsx)](https://sheetjs.com/) for Excel export
- Browser localStorage for persistence

## 📁 Project Structure

```
.
├── index.html    # The complete app (HTML + CSS + JS)
└── README.md
```

## 🔮 Possible Future Improvements

- Cloud or database storage for multi-device access
- Teacher login and role-based access
- Printable PDF reports
- Bulk student import from Excel/CSV
- Parent notifications for absences

## 📄 License

Free to use for educational purposes. Add a license of your choice (for example MIT) before publishing.
