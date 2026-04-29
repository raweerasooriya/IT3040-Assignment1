# IT3040 - ITPM Assignment 1: Transliteration Accuracy Testing

## Student Information
- **Registration Number:** IT23168190
- **Name:** WEERASOORIYA R A
- **Course:** BSc (Hons) in Information Technology - Year 3
- **Assignment:** Option 1 - Singlish to Sinhala Transliteration Testing

## Project Overview
This project automates testing of the Chat Sinhala transliteration tool available at:
https://www.pixelssuite.com/chat-translator

The automation script tests 50 negative test cases across 24 Singlish input types (as specified in Appendix 1 of the assignment) and records results in an Excel spreadsheet.

## Prerequisites

### Required Software
- Python 3.11 or 3.12
- Google Chrome browser

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/raweerasooriya/IT3040-Assignment1.git
   cd IT3040-Assignment1

2. Install dependencies

   ```bash
   pip install -r requirements.txt
   Note: If pip is not recognized, use py -m pip install -r requirements.txt

3. Install Playwright browsers
   ```bash
   playwright install
   
   Note: If playwright is not recognized, use py -m playwright install

## How to Run Tests

### Important Note Before Running:
**Your Excel file should only have columns A-D (Test Case ID, Input length type, Input, Expected output) before running the script.** The script will automatically add columns E (Actual output) and F (Status). After the script completes, you can manually add columns G and H for input types and evidence.

### Run the automation script:

1. Option 1: Using `py` (recommended - works even if Python is not in PATH)**
   ```bash
   py test_automation.py --excel "IT23168190_Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --save-every 5

2. Option 2: Using python (if Python is in your system PATH)**

   ```bash
   python test_automation.py --excel "IT23168190_Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --save-every 5


### Test Coverage
- The 50 test cases cover all 24 Singlish input types from Appendix 1, including:
- Question forms, Command forms, Greetings, Requests, Responses
- Repeated Words, Punctuation Marks, Romanization Variants
- English Word Insertions (isolated, multi-word, digital terms)
- Platform/App Names, Abbreviations, Clipped Forms
- Place Names, Person Names, Numbers, Currency
- Time Formats, Dates, Units of Measurement
- Slang & Casual Phrasing, Online Identifiers, Emojis

### Results
All 50 test cases resulted in FAIL status, correctly identifying inaccuracies in the transliteration tool's output.

### Output
The script automatically:
1. Updates the Excel file with actual outputs
2. Marks each test as PASS or FAIL
3. Results are saved in IT23168190_Assignment 1 - Test cases.xlsx

### Troubleshooting
## Issue: python or pip not recognized
* Use py instead of python in commands
* Or add Python to system PATH

## Issue: Browser doesn't open
* Remove --headless flag to see the browser
* Ensure Chrome is installed or run playwright install

### Author
Registration Number: IT23168190
Name: WEERASOORIYA R A

### License
This project is for educational purposes as part of the IT3040 - ITPM course assignment.