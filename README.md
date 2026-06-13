# GridSage AI ⚡

### Hybrid Deep Learning Framework for Robust Electricity Demand Forecasting

GridSage AI is a hybrid AI-powered electricity demand forecasting system designed to improve forecasting accuracy, peak-hour stability, and operational efficiency in modern power grids.

The project combines the temporal sequence-learning capability of **Long Short-Term Memory (LSTM)** networks with the nonlinear residual correction power of **XGBoost** to create a robust hybrid forecasting architecture capable of handling seasonal variations, nonlinear demand trends, and extreme grid events.

---

# 🚀 Key Features

✅ Hybrid Deep Learning Architecture
✅ Multivariate Time-Series Forecasting
✅ LSTM + XGBoost Residual Learning
✅ 10 Years of Hourly Grid Simulation Data
✅ Extreme Event & Demand Spike Simulation
✅ Peak-Hour Robustness Analysis
✅ Energy Misallocation Evaluation
✅ Research-Style Visualizations & Metrics
✅ Realistic Utility-Scale Forecasting Pipeline

---

# 🧠 Problem Statement

Accurate electricity demand forecasting is critical for:

* Grid stability
* Power generation scheduling
* Peak-load management
* Energy cost optimization
* Preventing overproduction and underproduction

Traditional forecasting systems often struggle during:

* seasonal transitions
* volatile demand periods
* heatwaves
* sudden industrial surges
* peak-hour stress conditions

GridSage AI addresses these challenges using a hybrid residual-learning forecasting framework.

---

# ⚙️ Proposed Hybrid Architecture

The project uses a two-stage forecasting pipeline:

## Stage 1 — LSTM Forecasting

The LSTM network learns:

* temporal dependencies
* daily usage patterns
* seasonal behavior
* long-term trends

It generates the **base electricity demand prediction**.

---

## Stage 2 — XGBoost Residual Learning

After LSTM prediction:

Residual Error = Actual Demand − LSTM Prediction

XGBoost then learns:

* systematic forecasting mistakes
* nonlinear residual behavior
* sudden spikes and irregular patterns

Final Hybrid Prediction:

Hybrid Forecast = LSTM Prediction + XGBoost Residual Correction

This improves:

* robustness
* forecasting stability
* operational reliability

---

# 📊 Dataset Characteristics

The project uses a realistic synthetic electricity demand dataset containing:

* 10 years of hourly data
* nonlinear long-term growth
* yearly seasonality
* daily seasonality
* temperature-driven load behavior
* stochastic noise
* rare extreme grid events
* cyclical temporal encoding

### Input Features

* Demand
* Temperature
* Hour (sin/cos)
* Day-of-week (sin/cos)
* Month (sin/cos)

---

# 🧪 Machine Learning Pipeline

## 1️⃣ Data Generation

Synthetic utility-scale electricity demand simulation.

## 2️⃣ Preprocessing

* MinMax scaling
* multivariate feature engineering
* 24-hour sliding window sequences

## 3️⃣ LSTM Training

* 2-layer stacked LSTM
* 64 hidden units
* Adam optimizer
* MSE loss

## 4️⃣ Residual Learning

XGBoost learns structured forecasting residuals.

## 5️⃣ Hybrid Forecast Generation

Final prediction fusion:
LSTM Output + XGBoost Correction

## 6️⃣ Evaluation & Robustness Analysis

Performance measured using:

* MAE
* RMSE
* MAPE
* SMAPE
* NRMSE
* R² Score
* Peak-Hour MAE
* 95th Percentile Error
* Maximum Error
* Energy Misallocation (GWh/year)

---

# 📈 Results

The hybrid architecture consistently outperformed:

* heuristic forecasting baselines
* standalone LSTM forecasting

### Key Improvements

✅ Reduced forecasting error
✅ Better peak-hour stability
✅ Lower cumulative energy misallocation
✅ Improved robustness during extreme events

---

# 📉 Energy Misallocation Analysis

Unlike traditional forecasting projects that only evaluate MAE or RMSE, GridSage AI also measures:

## Annual Energy Misallocation (GWh/year)

This metric estimates how much electrical energy would be:

* overallocated
* underallocated
* incorrectly scheduled

due to forecasting inaccuracies.

This makes the project more aligned with real-world grid operations and utility-scale decision-making.

---

# 🛠️ Technologies Used

### Programming & Libraries

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

### Deep Learning

* PyTorch

### Machine Learning

* XGBoost

### Visualization

* Matplotlib
* Graphviz

---

# 📂 Project Structure

```bash
GridSage-AI/
│
├── data/
│   └── synthetic_electricity_demand.csv
│
├── notebooks/
│   └── GridSage_AI.ipynb
│
├── results/
│   ├── graphs/
│   └── evaluation_tables/
│
├── paper/
│   └── GridSage_AI_Research_Paper.pdf
│
├── README.md
└── requirements.txt
```

---

# 📌 Research Contributions

### 🔹 Hybrid Residual Learning Framework

Combines deep temporal learning with structured nonlinear correction.

### 🔹 Utility-Oriented Evaluation

Focuses not only on prediction accuracy but also operational energy impact.

### 🔹 Robustness Under Extreme Events

Simulates realistic grid stress conditions including demand spikes and volatility.

### 🔹 Peak-Hour Reliability

Evaluates forecasting performance during high-stress evening demand periods.

---

# 🔮 Future Improvements

Possible future extensions include:

* Real utility-grid datasets
* Transformer-based forecasting
* Real-time deployment pipelines
* Explainable AI for grid forecasting
* Probabilistic forecasting
* Renewable energy integration
* Smart-grid optimization

---

# 👨‍💻 Team

* Vansh Baraswal
* Hitesh Verma
* Alok Kumar Gujar
* Nitesh Shrivas
* Satyam Tripathi
* Suryansh Kesarwani

Harcourt Butler Technical University (HBTU), Kanpur

---

# 📜 License

This project is developed for academic research, learning, and hackathon purposes.

---

# ⭐ Final Note

GridSage AI demonstrates how hybrid AI architectures can improve electricity demand forecasting reliability by combining temporal deep learning with residual error correction.

The project prioritizes:

* realism
* robustness
* operational relevance
* energy-efficiency impact

making it suitable for research-oriented smart-grid forecasting applications.
