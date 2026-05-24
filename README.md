# 🎁 Trial Checker

**Trial Checker** is a command-line utility designed to **check, validate, and verify trial / account access status** in an automated and efficient way.

---

## ⚙️ Features

* 🔍 **Account Checker** – Verify trial or account validity in seconds
* ⚡ **Fast Processing** – Lightweight and optimized for speed
* 🔁 **Batch Checking** – Process multiple inputs at once
* 📊 **Clear Output** – Shows status results in a clean format
* 🌐 **Proxy Support** – Optional proxy integration for requests
* 🧩 **Simple CLI Interface** – Easy to use with minimal setup

---

## 🧠 Requirements

* Python 3.9+
* Stable internet connection
* Valid input list (emails / accounts / tokens depending on config)

---

## 🧰 Installation

```bash
# Clone this repository
git clone https://github.com/imlittledoo/trial-checker.git

# Navigate to the folder
cd trial-checker

# Install dependencies
pip install -r requirements.txt
````

---

## ⚙️ Configuration

If your tool uses config files, create or edit:

```json
{
  "proxyless": true,
  "timeout": 10
}
```

Optional:
Add proxies in `input/proxies.txt` (one per line) if proxy mode is enabled.

---

## ▶️ Usage

```bash
python main.py
```

Follow the menu / CLI prompts to:

1. Start account / trial checking
2. Load input list
3. View results (valid / invalid / expired)
4. Save outputs automatically

Results are stored in the `output/` directory.

---

## 📊 Output Example

```
VALID   | user@email.com
INVALID | test@email.com
EXPIRED | old@email.com
```

---

## ⚠️ Disclaimer

This tool is intended for **educational and testing purposes only**.
The developer is not responsible for any misuse or damage caused by this tool.

Use responsibly and follow applicable terms of service.

---

## 🧑‍💻 Author

Developed by **ImLittledoo**
If you like this project, consider giving it a ⭐
