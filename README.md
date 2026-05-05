# Project Overview: Automated PDF Quiz Extraction & Interactivity

This document summarizes the technical process used to transform a static 700-question English Proficiency Test from PDF format into a fully interactive Offline Web Application (Quiz App).

## 🛠 Tools & Technologies Used
*   **Google Colab:** Cloud-based Python environment for data processing.
*   **Python Libraries:**
    *   `pdfplumber`: For high-precision table and text extraction from PDF.
    *   `re` (Regular Expressions): For pattern matching, text cleaning, and formatting.
    *   `json`: To structure the data for web compatibility.
*   **Web Technologies:** HTML5, CSS3 (Modern UI/UX), and Vanilla JavaScript for interactivity.

## 🚀 Execution Steps

### 1. Data Extraction & Cleaning
We implemented custom Python scripts to parse the PDF. The challenge was splitting long questions and multiple-choice options into distinct lines. We successfully formatted the raw data into:
*   **Questions:** `[Number]- [Question Text]` followed by `a- [Option A] b- [Option B] ...`
*   **Answers:** A clean vertical key formatted as `[Number]- [Letter].`

### 2. Regex Transformation
Using advanced Regular Expressions, we ensured that:
*   Every question is contained in a single line regardless of its original PDF layout.
*   Choice markers were standardized from `a.` to `a-` and ended with a period `.` for consistency.

### 3. Data Integration
The extracted text files were converted into a **JSON-like object**. This allowed us to map each question number to its corresponding correct answer automatically.

### 4. Interactive Product Development
We built a standalone **HTML5 Offline Application** that features:
*   **Dynamic Navigation:** Seamlessly move between 700 questions.
*   **Instant Feedback:** A "Show Answer" toggle for study mode.
*   **Score Calculation:** A final result screen to track performance.
*   **Responsive Design:** Optimized for both Desktop and Mobile devices.

## 📦 Final Product
The end result is **`yehia_quiz.html`**, a lightweight, portable, and professional interactive quiz tool that requires no internet connection to function.

