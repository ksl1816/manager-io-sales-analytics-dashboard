# 📊 Manager.io — Sales Analytics Dashboard

> A free, self-contained extension for [Manager.io](https://www.manager.io) that turns your sales invoice data into a fully interactive daily analytics dashboard — no backend, no setup, just install and go.

![Manager.io Extension](https://img.shields.io/badge/Manager.io-Extension-blue?style=flat-square)
![License](https://img.shields.io/badge/License-Free-green?style=flat-square)
![Currency](https://img.shields.io/badge/Currency-Auto--detected-orange?style=flat-square)
![No Dependencies](https://img.shields.io/badge/Dependencies-Chart.js%20only-lightgrey?style=flat-square)

---

## ✨ Features

- **Day-by-day sales breakdown** — see exactly how much was sold on every single day of any month
- **Multi-month comparison** — overlay and compare any two or more months side-by-side, day by day
- **KPI summary cards** — grand total, average per month, average per day, best month, and active days at a glance
- **Interactive charts** — line charts per month and an overlay comparison chart powered by Chart.js
- **Smart insights** — automatically generated analysis including trend detection (upward / declining / volatile), best and worst months, and consistently strong or weak days across months
- **Flexible filters** — filter by year, individual months, or a custom date range
- **Auto currency detection** — reads the currency from your Manager.io data automatically; works for any country and any currency (USD, EUR, GBP, KWD, SAR, and more)
- **Table / Chart / Both toggle** — switch views per month without losing your place
- **Best and worst day highlighting** — 🏆 best day and ⚠ worst day are visually marked in every monthly table
- **Fully paginated data fetch** — loads every invoice across all API pages; never misses a record

---

## 🖼️ Screenshots

> <img width="1482" height="576" alt="image" src="https://github.com/user-attachments/assets/67bc00b1-131f-472a-b63d-edd0486183d3" />

> <img width="1477" height="657" alt="image" src="https://github.com/user-attachments/assets/e38430f0-47ee-474b-b896-5d4c22a6433e" />

>  <img width="267" height="178" alt="image" src="https://github.com/user-attachments/assets/c069aa7a-82b1-44d1-a3d1-a1cbdfc7b41d" />


><img width="1463" height="468" alt="image" src="https://github.com/user-attachments/assets/7733e4d1-3724-4ff9-874f-2e2eab56118b" />

---

## 🚀 Installation

### Option 1 — Install directly from GitHub Pages

1. Enable GitHub Pages on this repo *(Settings → Pages → Deploy from main branch)*
2. Your extension URL will be:
   ```
   https://ksl1816.github.io/manager-io-sales-analytics-dashboard/
   ```
3. In Manager.io go to **Settings → Extensions → Add Custom Extension**
4. Paste the URL above and save

### Option 2 — Download and host yourself

1. Download `index.html` from this repository
2. Host it on any static hosting service:
   - **GitHub Pages** — upload to any public repo and enable Pages
   - **Netlify** — drag and drop the file at [netlify.com](https://netlify.com)
   - **Vercel** — drag and drop at [vercel.com](https://vercel.com)
3. Copy the public URL and add it as a custom extension in Manager.io

---

## 🧭 How to Use

Once installed inside Manager.io:

1. Click **⬇ Load All Records** — the extension fetches all your sales invoice data automatically across all pages
2. Use the **filter panel** to select a year, specific months, or a custom date range
3. Click **Apply Filters** to refresh the dashboard
4. Switch between **Table**, **Chart**, and **Both** views for each month
5. Scroll down to see the **Month-to-Month Comparison** (appears when 2+ months are loaded) and the **Insights & Analysis** section

---

## ⚙️ Technical Details

| Property | Detail |
|---|---|
| File type | Single self-contained `.html` file |
| External library | [Chart.js 4.4.1](https://www.chartjs.org/) via CDN |
| API used | `GET /api4/batch-sales-invoice` |
| Pagination | Full — loops all pages via `next_page_token` |
| Currency | Auto-detected from invoice data (`baseCurrency` / `currency` field) |
| Framework | Vanilla HTML / CSS / JavaScript — no build step required |
| Manager.io communication | `postMessage` API (standard extension protocol) |

---

## 🌍 Currency Support

This extension **does not hardcode any currency**. On load, it reads the currency code directly from your Manager.io invoice data. If no currency is found in the data, it falls back to your browser's locale currency. This means it works correctly for businesses in any country.

---

## ⚠️ Disclaimer

This extension is an independent, community-built tool and is **not officially affiliated with or endorsed by Manager.io**. It is provided free of charge, as-is. Always verify financial figures against your official Manager.io reports before making business decisions.

This extension only **reads** data — it makes no write, edit, or delete calls to the Manager.io API.

---

## 🛠️ Built With

This extension was built using the **[Manager.io Developer Toolkit](https://github.com/ksl1816/manager-developer-toolkit-extenstion)** — and AI tools a companion extension that lets you explore Manager.io API endpoints and generate AI prompts for building extensions like this one.

---

## 📄 License

Free to use, modify, and share. Attribution appreciated but not required.

---

## 👤 Author

**ksl1816** — [github.com/ksl1816](https://github.com/ksl1816)

*Contributions, bug reports, and feature suggestions are welcome — open an issue or pull request.*
