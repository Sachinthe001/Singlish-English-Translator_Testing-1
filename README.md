# Option 1: Transliteration Accuracy Testing

This project contains an automated test suite using Playwright to evaluate the transliteration accuracy of `https://www.pixelssuite.com/chat-translator`. The testing is targeted at evaluating how accurately the application converts chat-style Singlish into Sinhala. The results are recorded directly into the Excel spreadsheet provided.

## Prerequisites
- **Python**: Version 3.11 or 3.12 is recommended.
- **Google Chrome**: Recommended, or let Playwright install its default Chromium browser.

## Installation Instructions

1. Clone this repository or download the ZIP file and extract it.
2. Open a Command Prompt or Terminal and navigate to the extracted folder:
   ```cmd
   cd path/to/test_automation
   ```
3. Install the required dependencies by running:
   ```cmd
   pip install -U pip
   pip install playwright openpyxl
   playwright install
   ```

## Running the Tests

To run the Playwright test automation script and record the results into the Excel spreadsheet, execute the following command in your terminal from the project root:

```cmd
python test_automation.py --excel "IT23318502_Test_cases.xlsx" --input-col "Input" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Note on Configuration Arguments
- `--excel`: The Excel spreadsheet containing the test cases.
- `--url`: The target Chat Translator URL.
- `--wait-ms`: Amount of time to wait after typing input to fetch the output (5000 ms = 5s).
- `--type-delay-ms`: Controls the simulated typing speed of Singlish characters.

## Test Results
After execution, the `IT23318502_Test_cases.xlsx` file will automatically be updated with the generated transliteration values under the **Actual output** and **Status** columns.
