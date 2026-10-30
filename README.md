# India-Stocks-2311-2340-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2311 to 2340)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2311-2340-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2311 to 2340)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2311 | `SUMIT` | Sumit Woods Limited | `SUMIT.NS` |
| 2312 | `SUMMITSEC` | Summit Securities Limited | `SUMMITSEC.NS` |
| 2313 | `SUNCLAY` | Sundaram Clayton Limited | `SUNCLAY.NS` |
| 2314 | `SUNDARAM` | Sundaram Multi Pap Limited | `SUNDARAM.NS` |
| 2315 | `SUNDRMBRAK` | Sundaram Brake Linings Limited | `SUNDRMBRAK.NS` |
| 2316 | `SUNDRMFAST` | Sundram Fasteners Limited | `SUNDRMFAST.NS` |
| 2317 | `SUNDROP` | Sundrop Brands Limited | `SUNDROP.NS` |
| 2318 | `SUNFLAG` | Sunflag Iron And Steel Company Limited | `SUNFLAG.NS` |
| 2319 | `SUNLOC` | Sunil Healthcare Limited | `SUNLOC.NS` |
| 2320 | `SUNRAKSHAK` | Sunrakshakk Industries India Limited | `SUNRAKSHAK.NS` |
| 2321 | `SUNSHIEL` | Sunshield Chemicals Limited | `SUNSHIEL.NS` |
| 2322 | `SUNSHINE` | Sunshine Pictures Limited | `SUNSHINE.NS` |
| 2323 | `SUNTECK` | Sunteck Realty Limited | `SUNTECK.NS` |
| 2324 | `SUPERHOUSE` | Superhouse Limited | `SUPERHOUSE.NS` |
| 2325 | `SUPERSPIN` | Super Spinning Mills Limited | `SUPERSPIN.NS` |
| 2326 | `SUPRAJIT` | Suprajit Engineering Limited | `SUPRAJIT.NS` |
| 2327 | `SUPREME` | Supreme Holdings & Hospitality (India) Limited | `SUPREME.NS` |
| 2328 | `SUPREMEENG` | Supreme Engineering Limited | `SUPREMEENG.NS` |
| 2329 | `SUPREMEINF` | Supreme Infrastructure India Limited | `SUPREMEINF.NS` |
| 2330 | `SUPRIYA` | Supriya Lifescience Limited | `SUPRIYA.NS` |
| 2331 | `SUPTANERY` | Super Tannery Limited | `SUPTANERY.NS` |
| 2332 | `SURAJEST` | Suraj Estate Developers Limited | `SURAJEST.NS` |
| 2333 | `SURAJLTD` | Suraj Limited | `SURAJLTD.NS` |
| 2334 | `SURAKSHA` | Suraksha Diagnostic Limited | `SURAKSHA.NS` |
| 2335 | `SURANASOL` | Surana Solar Limited | `SURANASOL.NS` |
| 2336 | `SURANAT&P` | Surana Telecom and Power Limited | `SURANAT&P.NS` |
| 2337 | `SURYALA` | Suryalata Spinning Mills Limited | `SURYALA.NS` |
| 2338 | `SURYALAXMI` | Suryalakshmi Cotton Mills Limited | `SURYALAXMI.NS` |
| 2339 | `SURYAROSNI` | Surya Roshni Limited | `SURYAROSNI.NS` |
| 2340 | `SURYODAY` | Suryoday Small Finance Bank Limited | `SURYODAY.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SUMIT 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2311-2340-Historical-Data/main/SUMIT/1m/2026/10/SUMIT_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
