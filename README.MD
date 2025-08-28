# 📈 Global Raw Material Price Volatility Index  
**Focus: UK-Relevant Commodities (Aluminum, Copper, Iron Ore, Nickel, Zinc)**

---

## 🔎 Project Overview
This project builds a **Volatility Index** for raw materials critical to the UK economy, using **World Bank’s Pink Sheet** monthly price data (1960–2025).  
The goal is to **track fluctuations in commodity prices**, identify historical spikes, and highlight risk patterns that affect supply chains, manufacturing, and industrial policy.

Volatility here is defined as the **rolling standard deviation of monthly returns**, computed using **Pandas / NumPy**, and visualised using **Matplotlib, Seaborn, and Plotly**.

---

## 📊 Why It Matters
For an **Operations / Supply Chain / Strategy** role, understanding volatility in raw materials is critical because:  
- 📉 **Procurement & Risk:** Higher volatility = unpredictable costs, margin risks.  
- 🏭 **Industry Exposure:** UK industries (automotive, aerospace, construction, renewables) rely on Aluminum, Copper, Iron/Steel, Nickel, Zinc.  
- 🔮 **Data-Driven Insight:** Volatility indices reveal periods of systemic stress (oil shocks, 2008 financial crisis, COVID-19).  

This analysis simulates what investment firms, manufacturers, and policymakers look at when assessing **market uncertainty**.

---

## 🛠️ Data Source
- **World Bank CMO “Pink Sheet” (Monthly)**  
  [Download Link](https://thedocs.worldbank.org/en/doc/18675f1d1639c7a34d463f59263ba0a2-0050012025/related/CMO-Historical-Data-Monthly.xlsx)  
- Frequency: Monthly (1960–2025)  
- Units: USD per metric ton (metals), USD per dmtu (iron ore)  

---

## ⚙️ Methodology
1. **Data Cleaning**
   - Extracted from Excel, dropped unit rows.
   - Selected UK-relevant metals: Aluminum, Copper, Iron Ore (cfr spot), Nickel, Zinc.
   - Converted to numeric time series with proper dates.

2. **Return Calculation**
   - Monthly % changes using `pct_change()`.

3. **Volatility Index**
   - Rolling **12-month standard deviation** of returns per commodity.
   - Composite Index = average of the 5 selected commodities.

4. **Visualisation**
   - **Line chart:** Historical trends & composite index.  
   - **Annotated chart:** Top 5 spikes labeled (2008, 2020, etc.).  
   - **Heatmap:** Annual average volatilities per commodity.  
   - **Interactive dashboard:** Plotly with rolling window dropdown (6m/12m/24m).  

---

## 📈 Key Outputs

### 1. Volatility Index (12m Rolling Std Dev)
- Black line = **Composite UK Volatility Index**  
- Colour lines = individual commodities  
- Clear spikes during:  
  - 1970s oil crises  
  - 2008 Global Financial Crisis  
  - 2020 COVID-19 pandemic  
  - 2022–23 Ukraine war / energy crisis  

---

### 2. Heatmap — Annual Average Volatility
| Commodity | Darker red = more volatile year |
|-----------|--------------------------------|
| Aluminum, Copper, Iron ore, Nickel, Zinc |

---

### 3. Summary Stats
- **Top 10 spikes:** highest composite volatility months (with dates).  
- **Decade averages:** long-term trend (1960s → 2020s).  

---

## 📂 Files in Repo
- `uk_raw_material_volatility_12m.csv` — full dataset of 12m rolling volatilities.  
- `uk_volatility_index_12m.png` — polished chart with annotations.  
- `uk_volatility_heatmap.png` — heatmap of annual average volatilities.  
- `uk_volatility_dashboard.html` — interactive Plotly dashboard.  
- `uk_volatility_top10_spikes.csv` — highest volatility events.  
- `uk_volatility_decade_averages.csv` — decade-wise summary.  
- `notebook.ipynb` — full code (cleaning, analysis, visualisation).  

---

## 🚀 Next Steps (Future Improvements)
- Add **steel and polymers** from Trading Economics API.  
- Explore **energy volatility** (natural gas, crude oil) as an overlay.  
- Extend into a **Streamlit app** for recruiters/clients.  

---

## 🧑‍💻 Tech Stack
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Plotly)  
- **Data:** World Bank CMO Pink Sheet (Monthly Prices)  
- **Exports:** CSV, PNG, HTML Dashboard  

---

## 🏁 Takeaway
This project demonstrates the ability to:  
✔ Collect & clean real-world economic data  
✔ Apply **financial/statistical methods** (returns, volatility)  
✔ Build a **composite KPI** relevant to operations & supply chain risk  
✔ Communicate results clearly with **visuals + storytelling**

📌 **Key Insight:**  
The UK Raw Material Volatility Index highlights how crises drive sharp instability in commodity markets — valuable intelligence for **supply chain planning, procurement, and policy decisions**.
