# WEBTest-Pro

#### EMPOWERING SEAMLESS AUTOMATION FOR FLAWLESS PERFORMANCE

## Table of Contents

- [About](#about)
- [Features](#features)
- [Demo](#demo)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
  - [1. Generate Test Cases](#1-generate-test-cases)
  - [2. Run Test Cases](#2-run-test-cases)
  - [3. Schedule Automated Testing](#3-schedule-automated-testing)
- [Test Case & Report Files](#test-case--report-files)
- [Customization and Extending](#customization-and-extending)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## About

**WEBTest-Pro** is a powerful, user-friendly, and extensible automation tool for web application QA. With a single interface, users can auto-generate test cases, execute them, and schedule repeat test runs—all **without writing any code**.

Built on [Streamlit](https://streamlit.io/), [Selenium](https://www.selenium.dev/), and [OpenPyXL](https://openpyxl.readthedocs.io/en/stable/), WEBTest-Pro is ideal for testers, developers, and QA teams looking for rapid automation, regression testing, and even CI/CD integration.

## Features

- 🧪 **Automated Test Case Generation**: Generate UI test cases from any URL with one click. Supports auto-scrolling and clickable element detection.
- 🔐 **Login Support**: Handles authentication via login forms (email+password).
- **No-Code Interface**: Control test runs, schedules, and management in an intuitive Streamlit app.
- 📜 **JSON Test Storage**: Stores test cases and credentials (safely) in per-website JSON files.
- 📊 **Excel Report Export**: Each test run produces detailed `.xlsx` reports (pass/fail, timestamps, and actions).
- ⏰ **Scheduled Testing**: Run your test suite periodically—to catch issues and regressions early.
- ⚙️ **Easy Customization**: Built from Python with modular, readable code.

## Demo

([WEBTest-Pro Interface Screenshot](https://github.com/Akshat-0208/WEBTest-Pro/tree/4c3e13e7787e2d3198e565b9615646d0323cd04c/Application%20Visuals))

- Python 3.8+
- **Google Chrome** browser installed
- **ChromeDriver** matching your Chrome version ([download here](https://chromedriver.chromium.org/downloads))
- The following Python libraries:
  - streamlit
  - selenium
  - openpyxl

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/webtest-pro.git
    cd webtest-pro
    ```

2. **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    If a requirements.txt isn't present, run:

    ```bash
    pip install streamlit selenium openpyxl
    ```

3. **Download and setup [ChromeDriver](https://chromedriver.chromium.org/downloads):**

    - Ensure `chromedriver` is in your `PATH` or same folder as your script.

## Usage

### 1. **Start the Application**

```bash
streamlit run your_script.py
```

_Note:_ Replace `your_script.py` with your actual filename (e.g., `webtestpro.py`).

### 2. **Using the Interface**

#### **A. Generate Test Cases**

- Enter the URL of the website to test.
- Enter a unique name for the website (used for saving files).
- If login is required, provide email and password.
- Click **Generate**. Test cases will be parsed and saved automatically.

#### **B. Run Test Cases**

- Enter the website name (as previously saved).
- Click **Run**. Test cases will be executed and a `.xlsx` report will be generated.

#### **C. Schedule Automated Testing**

- Enter the website name.
- Specify the time interval in seconds.
- Click **Schedule** to periodically run tests in the background.

## Test Case & Report Files

- Test cases are stored as: `your_website_name_testcases.json`
- Test execution reports are saved as: `your_website_name_test_reports.xlsx`
- Both are stored in the project root by default.

## Customization and Extending

- **Add more test actions:** Extend the logic in `generate_test_cases` and `run_tests`.
- **Advanced reporting:** Modify `log_result` to include more context or details.
- **Element matchers/selectors:** Tweak or extend the XPaths as necessary.
- Want to support more login flows? Extend the `perform_login` methods.

## Troubleshooting

- **ChromeDriver Errors:** 
  - Ensure your ChromeDriver version matches your Chrome browser.
- **Element Not Found/Timeout:** 
  - Check the site loads correctly; increase Selenium wait times if necessary.
- **File Not Found:** 
  - Ensure the website name is entered exactly as when generated.
- **Streamlit Port In Use:** 
  - Use `streamlit run your_script.py --server.port=8502` (or another free port).

## Contributing

Contributions, bug reports, and feature requests are welcome!  
Please open an issue or submit a pull request via [GitHub](https://github.com/Akshat-0208/WEBTest-Pro).

## License

[MIT License](LICENSE)

## Acknowledgements

- [Python](https://python.org/)
- [Streamlit](https://streamlit.io/)
- [Selenium](https://selenium.dev/)
- [OpenPyXL](https://openpyxl.readthedocs.io/)

**WEBTest-Pro** - _Empowering seamless automation for flawless performance_
