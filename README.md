# IT23588578

# IT23588578 - Assignment 1: Transliteration Accuracy Testing
## IT3040 – IT Project Management | BSc (Hons) in Information Technology | Year 3

---

## 📌 Project Overview

This project automates the testing of the **Chat Sinhala transliteration function** available at:
🔗 [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator)

The automation script tests **50 negative test cases** covering **24 Singlish input types** to evaluate how accurately the application converts chat-style Singlish input into Sinhala output.

---

## 📁 Project Structure

```
IT23588578/
│
├── test_automation.py        # Main Playwright automation script
├── IT23588578.xlsx           # Test cases Excel file (input + results)
└── README.md                 # Project documentation (this file)
```

---

## ⚙️ Prerequisites

Before running the project, make sure the following are installed:

| Requirement | Version |
|-------------|---------|
| Python | 3.12.x (recommended) |
| Google Chrome | Latest |
| pip | Latest |

---

## 🚀 Installation Guide

### Step 1: Clone or Download the Repository

```bash
git clone <your-repository-url>
cd IT23588578
```

### Step 2: Install Python Dependencies

Run the following commands **one by one** in Command Prompt or Terminal:

```bash
py -3.12 -m pip install -U pip
```

```bash
py -3.12 -m pip install playwright openpyxl
```

```bash
py -3.12 -m playwright install
```

> ✅ This installs Playwright, OpenPyXL, and all required browser binaries.

---

## ▶️ How to Run the Tests

### Step 1: Navigate to the Project Folder

```bash
cd C:\Users\<your-username>\Desktop\IT23588578
```

### Step 2: Run the Automation Script

```bash
py -3.12 test_automation.py --excel "IT23588578.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Command Parameters Explained

| Parameter | Description |
|-----------|-------------|
| `--excel` | Path to the Excel test cases file |
| `--url` | URL of the application under test |
| `--wait-ms` | Wait time in milliseconds after each input |
| `--type-delay-ms` | Delay between each keystroke in milliseconds |
| `--slow-mo-ms` | Slow motion delay for browser actions |
| `--save-every` | Save results to Excel after every N test cases |
| `--keep-open` | Keep browser open after tests complete |

---

## 📊 How It Works

```
1. Script opens Chrome browser automatically
        ↓
2. Navigates to https://www.pixelssuite.com/chat-translator
        ↓
3. Reads each test case from Excel (Column C - Input)
        ↓
4. Types the Singlish input into the chat translator
        ↓
5. Captures the Sinhala output from the application
        ↓
6. Saves the output to Excel (Column E - Actual output)
        ↓
7. Compares Expected output vs Actual output
        ↓
8. Records Pass/Fail in Excel (Column F - Status)
        ↓
9. Repeats for all 50 test cases
```

---

## 📋 Excel File Structure

| Column | Header | Description |
|--------|--------|-------------|
| A | Test Case ID | Unique ID (Neg_0001 to Neg_0050) |
| B | Input length type | S (≤30 chars), M (31–299 chars), L (300–450 chars) |
| C | Input | Singlish input text |
| D | Expected output | Correct Sinhala translation |
| E | Actual output | Auto-filled by script |
| F | Status | Auto-filled: Pass / Fail |
| G | Singlish input types covered | Input type category |
| H | Evidence or rationale | Justification for input type |

> ⚠️ **DO NOT** enter values in Column E (Actual output) or Column F (Status) manually. These are automatically filled by the script.

---

## 🧪 Test Cases Coverage

The 50 negative test cases cover all **24 Singlish input types**:

| # | Singlish Input Type |
|---|---------------------|
| 1 | Question forms |
| 2 | Command forms |
| 3 | Greetings |
| 4 | Requests |
| 5 | Responses |
| 6 | Repeated Words |
| 7 | Inputs with Punctuation Marks |
| 8 | Romanization / Spelling Variants |
| 9 | Isolated English Word Insertions in Singlish |
| 10 | Multi-Word English Phrases in Singlish |
| 11 | English Digital Terms in Singlish |
| 12 | Platform/App Names in Singlish |
| 13 | English Abbreviations/Acronyms in Singlish |
| 14 | English Clipped Forms in Singlish |
| 15 | Place Names Embedded in Singlish |
| 16 | Person Names Embedded in Singlish |
| 17 | Inputs with Numbers and Numeric Suffixes |
| 18 | Inputs with Currency |
| 19 | Inputs with Time Formats |
| 20 | Inputs with Dates |
| 21 | Inputs with Unit of Measurements |
| 22 | Inputs with Slang and Casual Phrasing |
| 23 | Online Identifiers in Singlish |
| 24 | Inputs Containing Emojis |

---

## ❗ Troubleshooting

### Error: File not found
```
Error: File 'IT23588578.xlsx' not found.
```
✅ Make sure the Excel file is in the **same folder** as `test_automation.py`

---

### Error: Playwright not installed
```
ModuleNotFoundError: No module named 'playwright'
```
✅ Run:
```bash
py -3.12 -m pip install playwright
py -3.12 -m playwright install
```

---

### Python version issues
✅ Always use `py -3.12` instead of `python` to ensure Python 3.12 is used.

---

## 👤 Author

- **Student ID:** IT23588578
- **Module:** IT3040 – IT Project Management
- **Year:** 3 | Semester 1
- **Assignment:** Assignment 1 – Option 1: Transliteration Accuracy Testing