# BITS Pilani Digital – Advanced Grading Console

A browser-based grading console prototype developed for the **BITS Digital CodeForge Challenge**.

The application allows an instructor to upload student marks, select a course, analyse marks, configure grade ranges, validate grading data, review student grades, and export the final grades as a CSV file.

> **Disclaimer:** This is an independent prototype created for the CodeForge challenge. It is **not an official BITS Pilani Digital grading tool** and is not used for actual academic grading.

---

## ✨ Features

* 📂 Upload student marks through an Excel file (`.xlsx` / `.xls`)
* 📚 Select a course from the uploaded data
* 📊 View course-level marks analytics
* 📈 Visualise marks distribution using a histogram
* 🔢 View minimum, maximum, average and median marks
* 👥 View total number of students
* ✅ Calculate pass rate
* ⚠️ Detect invalid or missing student data
* 🔍 Search students by BITS ID
* 🎓 Filter students by grade
* ⚙️ Configure custom grade ranges
* 🔄 Reset grade ranges to default values
* 🛡️ Validate grade ranges for gaps and overlaps
* 📋 View grade distribution
* 📥 Finalize and download grades as a CSV file
* ⏱️ Track the time taken to complete grading
* 📱 Responsive layout for different screen sizes

---

## 📊 Input Excel Format

The application expects an Excel file containing the following three columns:

| Column        | Description           |
| ------------- | --------------------- |
| `BITS ID`     | Student's BITS ID     |
| `Course`      | Course name           |
| `Total Marks` | Student's total marks |

### Example

| BITS ID  | Course   | Total Marks |
| -------- | -------- | ----------: |
| 2024XXXX | Course A |          82 |
| 2024YYYY | Course A |          71 |
| 2024ZZZZ | Course A |          64 |

### Input Rules

* `BITS ID` should identify the student.
* `Course` should contain the course name.
* `Total Marks` should be numeric.
* Marks are expected on a **0–100 scale**.
* Fractional marks are rounded to the nearest whole number by the application.
* Students receiving an **NC** grade should not be included in the uploaded file.

---

## 🎓 Default Grade Ranges

The application starts with these default grade ranges:

| Grade | Minimum | Maximum |
| ----- | ------: | ------: |
| A     |      80 |     100 |
| A-    |      70 |      79 |
| B     |      60 |      69 |
| B-    |      50 |      59 |
| C     |      40 |      49 |
| C-    |      30 |      39 |
| D     |      20 |      29 |
| E     |       0 |      19 |

The instructor can modify the grade ranges before finalizing the grades.

The application checks that the configured ranges are continuous and do not contain gaps or overlaps.

---

## 🔄 Application Workflow

1. Enter the instructor name.
2. Upload the Excel marks file.
3. Select the required course.
4. Review course analytics.
5. Review the uploaded student records.
6. Configure or confirm the grade ranges.
7. Check data and range validation.
8. Review the grade distribution.
9. Search or filter student records if required.
10. Click **Finalize & Download** to export the grades as a CSV file.

---

## 📊 Analytics

For the selected course, the application displays:

* Minimum marks
* Maximum marks
* Average marks
* Median marks
* Number of students
* Pass rate
* Number of data issues
* Grade-wise student counts
* Marks distribution histogram

---

## 🛡️ Data Validation

The application checks for common data problems, including:

* Missing BITS IDs
* Duplicate BITS IDs
* Missing marks
* Non-numeric marks
* Marks below 0
* Marks above 100

Invalid data prevents the final grade file from being downloaded until the issues are resolved.

---

## ⚙️ Grade Range Validation

The application validates the configured grade ranges.

It checks that:

* Every grade has a valid minimum and maximum.
* Minimum is less than maximum.
* Grade ranges remain continuous.
* There are no gaps or overlaps between consecutive grades.

The **Reset Range** button can be used to restore the default grading ranges.

---

## 📥 CSV Export

After successful validation, the instructor can finalize the grading process and download a CSV file.

The exported file contains:

* Instructor name
* Course
* Student BITS ID
* Total Marks
* Grade

---

## 🛠️ Technology Used

This project is implemented as a **single self-contained HTML file** containing:

* HTML
* CSS
* JavaScript
* HTML5 Canvas for the marks histogram
* SheetJS (`xlsx`) for reading Excel files

The SheetJS library is loaded through a CDN, so no package installation or build process is required.

---

## 🚀 How to Run

No installation is required.

### Option 1 — Open directly

Download or clone the repository and double-click:

```text
index.html
```

The application will open directly in your web browser.

### Option 2 — Run using a local server

You can also serve the HTML file using any simple local HTTP server.

For example, with Python:

```bash
python -m http.server
```

Then open the local address shown by the server in your browser.

---

## 📁 Project Structure

```text
BITS-Digital-CodeForge/
│
├── index.html
└── README.md
```

The application does not require a backend, database, npm installation, or external project framework.

---

## 🔐 Data Handling

The grading interface processes the uploaded grading data directly in the browser.

The prototype does not require a backend server or database for its core grading workflow.

---

## 🎯 Project Objective

The objective of this prototype is to demonstrate how a grading workflow can be made more structured, transparent, and user-friendly while reducing common data-entry and grading-configuration errors.

---

## ⚠️ Disclaimer

This project was created as an educational prototype for the **BITS Digital CodeForge Challenge**.

It is **not an official BITS Pilani Digital grading system** and should not be used for official academic grading or academic records.

---

## 👩‍💻 Author

**Honey Kiran Jain**

BCA Graduate
M.Sc. Data Science & AI Student

GitHub: https://github.com/honeyjain1421
