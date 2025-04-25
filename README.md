# Demo Selenium Python

Demonstration of:

* [Selenium](https://www.selenium.dev/) browser automation testing
* [Python](https://en.wikipedia.org/wiki/Python_(programming_language)) programming language
* [ChromeDriver](https://developer.chrome.com/docs/chromedriver) extends Webdriver by adding Chromium-specific capabilities

Many more examples are here:

* [SeleniumHQ examples](https://github.com/SeleniumHQ/seleniumhq.github.io/tree/trunk/examples)

## Install

### Install Python

Install Python from <https://www.python.org/>

Run this to confirm your version:

```sh
python -v
```

Output should be at least:

```stdout
Python 3.13.1
```

### Install uv

Install uv from <https://github.com/astral-sh/uv>

Run this to confirm your version:

```sh
uv version
```

Output should be at least:

```stdout
uv 0.6.14
```

### Install Selenium

Install Selenium WebDriver:

```sh
uv add selenium
```

### Update

Run:

```sh
uv self update
uv lock --upgrade
uv sync
```

## Run

Run:

```sh
uv run main.py
```

The script will do three things:

1. Launch your local Chrome web browser to view the free open source testing examples web page <https://testingexamples.github.io>.

2. Interact with the web page in various ways, such as finding elements, clicking on elements, filling in form inputs, etc.

3. Print some typical HTML tag output that demonstrates the program is running successfully.

### Troubleshooting “chromedriver” Not Opened

If you get this kind of error message:

```txt
“chromedriver” Not Opened. Apple could not verify “chromedriver”
is free of malware that may harm your Mac or compromise your privacy.
```

Or this kind of error message:

```txt
Apple is not able to verify that it is free from malware that could harm your
Mac or compromise your privacy. Don’t open this unless you are certain it is
from a trustworthy source.
```

Then click "Done".

Try this command line solution:

```sh
xattr -d com.apple.quarantine $(which chromedriver) 2>/dev/null
```

Try adjusting your system settings:

* Apple menu -> Settings -> Security & Privacy -> General

* See the entry that says: "chromedriver" was blocked to protect your Mac.

* Click the button "Allow Anyway".

### Troubleshooting "This version of ChromeDriver …"

If you get this kind of error message:

```txt
UnhandledPromiseRejectionWarning:
SessionNotCreatedError: session not created:
This version of ChromeDriver only supports Chrome version …
```

Then you may need to harmonize your Chrome browser app and your Chrome webdriver.

If you use macOS brew, then upgrade chromedriver:

```sh
brew upgrade chromedriver
```

To update your Chrome browser app:

* On your computer, open Chrome.

* Find your current Chrome version by typing in the URL bar: `chrome://version/`.

* You should see a web page with many details, and you should see the first line with the version number, such as: "Google Chrome 135.0.7049.86 (Official Build)".

* At top right, tap the "More" icon, which is 3 vertical dots.

* You see the "More" menu. If you see a menu item "Update", then choose it. If you don't see a menu item "Update", then  you're on the current version.

To update your Chrome webdriver:

* Go to https://chromedriver.chromium.org/downloads

* Download the version that matches your Chrome browser app.


## Tracking

* Package: demo-selenium-python
* Version: 1.4.0
* Created: 2019-11-02T00:00:00Z
* Updated: 2025-04-24T13:58:02Z
* License: GPL-2.0-or-greater or for custom license contact us
* Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
