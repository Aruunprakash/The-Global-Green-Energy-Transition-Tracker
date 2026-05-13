# Global Green Energy Transition Tracker (2023)

A professional end-to-end data science pipeline that simulates, cleans, and visualizes a national energy grid's transition toward renewable sources. This project demonstrates the integration of **NumPy** for complex simulation, **Pandas** for statistical data surgery, and **Matplotlib** for executive-level dashboarding.

---

## 🏗️ Project Architecture

The project is built using a **3-Layer Architecture** to ensure clean separation between raw data generation and final business insights.

### Layer 1: Synthetic Data Simulation (NumPy)
* **Trigonometric Seasonality:** Modeled Solar and Wind production using sine-wave transformations to reflect summer and winter peaks.
* **Chaos Injection:** Simulated real-world hardware issues by injecting random sensor failures (error codes) and massive voltage spikes (outliers).
* **Vectorization:** Used NumPy broadcasting for high-performance calculations across 365 days of data.

### Layer 2: The Data Hospital (Pandas)
* **Time-Series Structuring:** Converted raw matrices into a Datetime-indexed DataFrame for time-based analysis.
* **Statistical Surgery:**
    * **99th Percentile Clipping:** Used quantile-based filtering to "cap" impossible sensor spikes without deleting data.
    * **Rolling Mean Imputation:** Healed data gaps using a 7-day centered window to maintain seasonal trends.
* **Feature Engineering:** Calculated "Green Share %" and total grid load to assess transition reliability.

### Layer 3: Executive Insights Dashboard (Matplotlib)
* **Multi-Axes Layout:** Built a 2x2 grid using the `ax` object-oriented interface for surgical layout control.
* **Visual Analytics:**
    * **Trend Analysis:** Combined daily fluctuations with a 30-day moving average.
    * **Energy Mix:** A yearly distribution pie chart with "exploded" focus on renewable growth.
    * **Grid Stability:** Histogram analysis of total production frequency.
    * **Resource Correlation:** Scatter mapping of Solar vs. Wind reliability using color-mapped gradients.

---

## 🚀 Key Features
* **Reproducible Results:** Hard-coded `np.random.seed(42)` ensures consistent debugging and analysis.
* **Dynamic Scaling:** Quantile-based cleaning allows the pipeline to adapt to any dataset without hard-coded limits.
* **Professional Visualization:** Utilizes transparency (alpha), colormaps (viridis), and custom layout adjustments for presentation-ready output.

## 🛠️ Tech Stack
* **Language:** Python 3.14+
* **Libraries:** NumPy, Pandas, Matplotlib
* **Environment:** PyCharm / Virtual Environments (.venv)

---
*Developed as part of a Python Data Science study module focusing on software development and data normalization.*Tracker