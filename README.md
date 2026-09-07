# 📊 Financial & Operational System Dashboards

A dual-purpose analytics toolkit featuring a **Capital Asset DCF & Rate Sensitivity Engine** for investment appraisal and a **Warehouse Inventory Safety Auditor** for automated supply chain risk mitigation.

---

## 🚀 Visual Outputs & System Dashboards

### 1. Capital Asset DCF & Rate Sensitivity Dashboard (`dcf_engine.py`)
Evaluates a $\$250,000$ initial capital expenditure stream against multi-year returns, plotting cumulative cash flow payback alongside discount rate risk curves.
![Asset Analysis Dashboard](outputs/asset_analysis_dashboard.png)

### 2. Warehouse Inventory vs. Safety Threshold Auditor (`inventory_auditor.py`)
Parses stock positions against minimum safety thresholds, automatically isolating critical shortages (e.g., Bolts and Circuit Boards) with color-coded conditional logic.
![Inventory Status](outputs/inventory_status.png)

---

## 📂 Repository Layout & Architecture

* **`dcf_engine.py`**: Object-oriented class (`AssetEvaluator`) implementing Net Present Value (NPV), Internal Rate of Return (IRR) via `numpy-financial`, and automated risk sensitivity profiling across varying discount rate arrays.
* **`inventory_auditor.py`**: Modular inventory management class (`StockAuditor`) that filters stock counts below safety thresholds and exports production-ready status charts.

---

## 📐 Mathematical Foundations & Governing Equations

### 1. Discounted Cash Flow (DCF) & Net Present Value (NPV)
Sums the present value of future cash inflows against initial capital expenditure:

$$\text{NPV} = \sum_{t=0}^{n} \frac{\text{CF}_t}{(1 + r)^t} - \text{Initial Capex}$$

*Where $\text{CF}_t$ = cash flow at year $t$, and $r$ = hurdle discount rate.*

### 2. Internal Rate of Return (IRR)
Computes the annualized effective compound return rate by locating the root where NPV equals zero:

$$0 = \sum_{t=0}^{n} \frac{\text{CF}_t}{(1 + \text{IRR})^t} - \text{Initial Capex}$$

### 3. Inventory Safety Stock Threshold Logic
Monitors current unit allocations on hand to trigger automated replenishment flags:

$$\text{Shortage Flag} = \text{Units On Hand} \leq \text{Safety Threshold}$$

---

## 🛠️ Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/financial-operational-dashboards.git](https://github.com/your-username/financial-operational-dashboards.git)
   cd financial-operational-dashboards
