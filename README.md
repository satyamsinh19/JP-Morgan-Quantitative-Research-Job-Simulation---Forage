<h1 align="center">JPMorgan Chase Quantitative Research Vitual Job Simulation — Full Solution (Forage)</h1>
<h2 align="center">Natural Gas Pricing • Storage Contract Valuation • Credit Risk Modeling • FICO Bucketing</h2>

A complete, end-to-end quantitative analytics project implementing time-series price estimation, commodity storage valuation, credit risk modeling, and FICO score quantization.

---

## 💡 Overview

This project simulates quantitative research work within JPMorgan's Global Commodities and Risk divisions.  
It integrates:

- Natural gas forward curve analysis  
- Storage contract valuation  
- Probability of Default (PD) modeling  
- FICO score bucketing via data-driven quantization  

All implementations are provided in the `.ipynb` files.

---

## 📁 Project Deliverables

| Task | Focus Area | File |
|------|------------|------|
| **Task 1** | Natural Gas Price Analysis & Extrapolation | `Task 1.ipynb` |
| **Task 2** | Storage Contract Valuation | `Task 2.ipynb` |
| **Task 3** | PD Model & Expected Loss | `Task 3.ipynb` |
| **Task 4** | FICO Score Quantization | `Task 4.ipynb` |

---

# ✅ Task 1: Natural Gas Price Analysis & Extrapolation

Using monthly price data (Oct 2020 → Sep 2024), a forecasting function was built to estimate:

- Price at any given historical date  
- Price 12 months into the future  
- Trend and seasonality in the gas market  

### Key Insights

**Market Behavior Observed**

- **2020–2021:** Low and stable  
- **2022:** Significant upward spike in prices  
- **2023–2024:** Gradual decline but still above pre-spike levels  
- Seasonal winter effects visible  

**Data Characteristics**

- Clean monthly time series with no missing values  
- Extrapolation provides a smooth forward curve  
- Function created:
    predict_price(date) → estimated natural gas price

---

# 📈 Task 2: Commodity Storage Contract Valuation

A flexible pricing engine was developed using:

- Injection and withdrawal schedules  
- Purchase/sale prices on given dates  
- Maximum storage volume  
- Injection/withdrawal rates  
- Storage operating costs  

The model calculates total cash flows and outputs contract value.

### Key Model Output

**Contract Value:**  
-9900.0


**Interpretation:**  
The sample scenario results in a **net loss**, driven by:

- High operating/injection costs  
- Price spread insufficient to offset storage expenses  
- Negative net cash-flow across the cycle  

---

# 💳 Task 3: PD Model & Expected Loss Estimation

A supervised machine learning model predicts borrower **Probability of Default (PD)**.  
Expected loss is computed using:
 Expected Loss = PD × Exposure × (1 − Recovery Rate)


Recovery rate used: **10%**

### Key Output

**Expected Loss:**  
22497.71


**Interpretation:**  
The borrower used in the test example shows:

- Meaningful default risk  
- Significant exposure driving a high loss estimate  
- Model correctly capturing financial risk factors  

---

# 📚 Task 4: FICO Score Quantization

A quantization algorithm was implemented to bucket borrowers by FICO score.  
The output segmentation:

| FICO Range | Count | Defaults | Default Rate |
|-----------|-------|----------|--------------|
| 300–579 | 354 | 58 | 0.1638 |
| 580–669 | 904 | 124 | 0.1372 |
| 670–739 | 1095 | 98 | 0.0895 |
| 740–799 | 850 | 43 | 0.0505 |
| 800–850 | 1657 | 77 | 0.0465 |

### Insights

- Default risk decreases sharply with higher FICO scores  
- Buckets clearly separate high-risk and low-risk groups  
- Supports credit scoring, loan pricing, and portfolio analytics  

---

# 🙋‍♂️ About Me

👤 **Satyam Kumar**  
🔍 Data Analyst  
📧 *satyamkv123@gmail.com*  
🔗 [LinkedIn](https://www.linkedin.com/in/satyam-kumar-5a229222b)


