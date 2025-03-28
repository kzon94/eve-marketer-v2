# 🚀 EVE Marketer v2

![EVE Marketer Logo](eve.jpg)

**Advanced Market Analysis Tool for EVE Online**  
*Built for Google Colab. Designed for industrialists and traders.*

---

## 📈 Project Goal

EVE Marketer v2 is a Python-based tool designed for use in **Google Colab**. It allows capsuleers to:

- 🔎 Query **market prices** in **Jita 4-4**
- 📊 Analyze **historical buy trends** over the past **7 and 31 days**
- 📉 Calculate **percentage price changes**
- 🧮 Compare profitability of selling raw materials vs. manufacturing

> 🧪 **Note:** Jita 4-4 is currently used as the default trade hub for testing, as it's my primary buying/selling location.  
> ⚙️ Future versions will support **Amarr, Dodixie, Rens, Hek**, and other hubs.

---

## 🧩 How It Works

1. **Input**  
   Upload the file [`materials_id_classified.csv`](https://github.com/kzon94/eve-marketer-v2), which includes:

   - `type_id` — EVE Online's item ID  
   - `name` — Item name  
   - `material_type` — Category (Ore, Gas, Ice...)  
   - `tier` — Tier classification (T1–T7)

   <a href="https://imgbb.com/"><img src="https://i.ibb.co/20sntMGx/materials-id-classified.png" alt="materials-id-classified" border="0"></a>

   > 🧠 **Data source**: Special thanks to [Adam4EVE.eu](https://www.adam4eve.eu/info_types.php) — a fantastic resource whose data helped build the base classification list.

2. **API Query**  
   The script calls the **ESI API** to retrieve:

   - Current buy/sell prices at Jita 4-4
   - Max historical buy prices (7d & 31d)
   - % price change over time

3. **Output**  
   Generates a ready-to-use CSV file:

   ```
   mining_market_jita_v3.csv
   ```

   <a href="https://ibb.co/3ytPsvfP"><img src="https://i.ibb.co/pvCkPQWk/mining-market-jita-v3.png" alt="mining-market-jita-v3" border="0"></a>
  
   - Uses `;` as the delimiter and `,` as the decimal symbol
   - Compatible with Excel, Google Sheets, and other spreadsheet tools

---

## 📊 Market Visualizer

Once the CSV is generated, you can run the **graph generator notebook** to visualize the data:

- 📉 **Bar chart**: Current buy prices by tier/material type  
  <a href="https://ibb.co/hJYyXYJz"><img src="https://i.ibb.co/39R7fR9Z/chart1.png" alt="chart1" border="0"></a>

- 📈 **Logarithmic line chart**: Price evolution over time (31d, 7d, Now)  
  <a href="https://ibb.co/yFKdCXNp"><img src="https://i.ibb.co/s9cb42gC/chart2.png" alt="chart2" border="0"></a>

*Still working on logarithmic chart :(

📸 Both graphs are exported as **one downloadable image** automatically.


---

## ⚙️ Setup & Requirements

Designed to run entirely in **Google Colab**. No local setup required.

Install `jedi` to enable smart notebook functionality:
```python
!pip install jedi
```

> ⚠️ Yes, just **jedi**.  
> You don't need the whole Jedi Council to analyze the market.

---

## 🧠 Features

- ✅ Jita 4-4 market scraping (buy & sell)
- ✅ Historical max buy (7d, 31d)
- ✅ Price delta calculation
- ✅ Multithreaded queries
- ✅ Comma-based decimals for Excel compatibility
- ✅ Colab-ready graphing tool
- ✅ Auto-download of CSV and graph image

---

## 🔮 Next Goals

- 🔁 Support **all major trade hubs**
- 💰 PI production profitability calculator
- ⚙️ ESI authentication for increased API limits
- 📦 Manufacturing cost analysis

---

## 🛡 Disclaimer

**This project is not affiliated with CCP Games.**  
It’s a personal tool for data-driven market decisions.

MIT License © [kzon94](https://github.com/kzon94)

---

💬 *Fly safe. Mine rich. Sell smart.*
