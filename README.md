# 🎁 Discord Trial Checker

**Discord Trial Checker** is a multi-threaded command-line tool designed to **check Discord tokens for trial eligibility, discount offers, and billing-related status**, using Discord’s internal API endpoints.

---

## ⚙️ Features

* 🧵 **Multi-threaded checker** – configurable thread count (up to 500)
* 🎯 **Token queue system** – processes tokens from file automatically
* 🌐 **Proxy support** – optional HTTP proxy rotation
* 🎁 **Trial detection** – identifies 1 month & 2 week trial offers
* 💸 **Discount detection** – detects special discount eligibility
* 📊 **Status categorization** – separates results into multiple outputs
* 💾 **Auto saving results** – writes instantly to output files
* 📁 **Sorted trial output** – sorts results by expiry date at the end

---

## 🧠 How It Works

The tool processes tokens from `input/tokens.txt` and sends requests to Discord’s billing API:

- `/users/@me/billing/user-offer` → checks trial availability
- `/users/@me/billing/subscriptions/preview` → checks discount eligibility

Each token is classified into:

- Valid trial (1 month / 2 week)
- No trial available
- Discount eligible
- Invalid token
- Error / rate limited

---

## 🧰 Installation

```bash
git clone https://github.com/imlittledoo/trial-checker.git
cd trial-checker
pip install -r requirements.txt
````

---

## 📁 Input Setup

Create the following files:

### `input/tokens.txt`

```
email:password:token
token
```

### Optional `input/proxies.txt`

```
username:password@ip:port
```

---

## ⚙️ Configuration

Create `config.json`:

```json
{
  "use_proxies": false
}
```

---

## ▶️ Usage

```bash
python main.py
```

Then enter:

* Number of threads (1–500)
* Tool will automatically start processing tokens

---

## 📤 Output Structure

All results are saved in the `output/` folder:

```
output/
│
├── trial.txt
├── 1_month_trial.txt
├── 2_week_trial.txt
├── no_trial.txt
├── invalid.txt
├── errors.txt
├── discount_tokens.txt
```

---

## 📊 Result Types

* **1 Month Trial** → long-term Discord trial offer
* **2 Week Trial** → short trial offer
* **Discount Tokens** → accounts with 40% discount eligibility
* **No Trial** → valid token but no offer
* **Invalid** → expired or broken token
* **Errors** → rate limits, connection issues, parsing failures

---

## 🧵 Performance

* Fully multi-threaded (configurable up to 500 threads)
* Uses TLS client sessions for request handling
* Auto retry system for API failures & rate limits
* Thread-safe file writing

---

## ⚠️ Disclaimer

This tool is for **educational and research purposes only**.
Use at your own risk. The developer is not responsible for misuse or violations of Discord’s Terms of Service.

---

## 🧑‍💻 Author

Made by **ImLittledoo**.
If you like this project, consider giving it a ⭐
