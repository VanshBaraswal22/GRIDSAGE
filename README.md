# GridSageAI ⚡

### AI-Powered Hybrid Smart Grid Electricity Demand Forecasting System

GridSageAI is a research-oriented hybrid AI framework for intelligent electricity demand forecasting in smart-grid environments. It combines **LSTM** for temporal sequence learning with **XGBoost residual learning** for nonlinear error correction to improve forecasting accuracy, peak-hour stability, and operational energy efficiency.

---

## Overview

Electricity demand forecasting is essential for reliable power-system planning and operation. In large-scale grids, even small forecasting errors can accumulate into significant energy misallocation, higher operational cost, and grid stress during peak-demand periods.

GridSageAI is designed to reduce these risks by learning:
- long-range temporal patterns,
- daily and seasonal demand cycles,
- temperature-driven load variation,
- and structured residual errors left by the base model.

The project uses a hybrid architecture to improve both point-wise accuracy and real-world operational usefulness.

---

## Why GridSageAI?

Traditional forecasting models often struggle with:
- nonlinear demand behavior,
- sudden spikes,
- seasonal shifts,
- and peak-hour stress.

Standalone deep learning models can capture temporal structure well, but they may still leave systematic forecasting errors. GridSageAI solves this by adding a residual correction stage, where XGBoost learns the remaining error after LSTM prediction.

This makes the system more robust for deployment-oriented electricity forecasting.

---

## Key Features

- Multivariate electricity demand forecasting
- Hourly smart-grid demand simulation
- LSTM temporal sequence modeling
- XGBoost residual correction
- Peak-hour forecasting evaluation
- Energy misallocation analysis
- Research-style metric reporting
- Scalable design for multiple grid sizes

---

## System Architecture

**Input Features**  
Historical demand, temperature, and cyclical time encodings

**Preprocessing**  
Scaling, sequence generation, and time-aware train-test split

**Stage 1: LSTM Forecasting**  
Learns demand trends, daily cycles, and seasonal structure

**Stage 2: Residual Learning**  
XGBoost learns the remaining forecast error

**Final Output**  
Hybrid prediction = LSTM forecast + residual correction

---

## Dataset and Preprocessing

The project uses a synthetic **10-year hourly electricity demand dataset** designed to emulate realistic grid behavior. The dataset includes:
- nonlinear long-term growth,
- daily usage cycles,
- seasonal variation,
- temperature effects,
- random fluctuations,
- and rare extreme events.

A chronological split is used so the final year is reserved for testing, preserving realistic forecasting conditions. Inputs are normalized using MinMax scaling, and a 24-hour sliding window is used to create multivariate sequences.

---

## Evaluation Metrics

GridSageAI is evaluated using both standard and operational metrics:

- MAE
- RMSE
- MAPE
- SMAPE
- NRMSE
- R² Score
- 95th Percentile Error
- Maximum Error
- Peak-Hour MAE
- Annual Energy Misallocation (GWh)

These metrics help measure not only average accuracy but also performance during critical load periods and cumulative operational impact.

---

## Results Summary

The hybrid model outperforms both the heuristic baseline and standalone LSTM on the test year.

### Reported test results
- **Hybrid MAE:** 244.40 MW  
- **Hybrid RMSE:** 329.78 MW  
- **Hybrid Peak-Hour MAE:** 243.91 MW  
- **Hybrid Energy Misallocation:** 2140.94 GWh/year  

Compared with the standalone LSTM, the hybrid model improves:
- average error,
- peak-hour stability,
- and annual energy misallocation.

Compared with the heuristic baseline, the improvement is substantially larger.

---

## Current Applications

- Smart-grid demand forecasting
- Utility load balancing
- Peak-hour power planning
- Reserve scheduling
- Industrial electricity optimization

---

## Future Applications

- Renewable energy integration
- Real-time adaptive forecasting
- IoT-based grid intelligence
- AI-assisted national smart grids
- Autonomous energy optimization systems

---

## Why the Hybrid Model Is Stronger

### Standalone LSTM
Good at learning temporal patterns, but may miss structured nonlinear errors and spike behavior.

### Hybrid LSTM + XGBoost
Adds a correction stage that learns residual error patterns, improving robustness during peak demand and reducing cumulative forecasting error.

This makes the hybrid version more suitable for real-world grid operation.

---

## Tech Stack

- Python
- PyTorch
- XGBoost
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Streamlit

---

## Project Structure

```text
GridSageAI/
│
├── GridSageAI.ipynb
├── app.py
├── README.md
└── requirements.txt
* nonlinear demand behavior,
* sudden demand spikes,
* seasonal fluctuations,
* and operational peak-hour stress.

Standalone deep learning models may learn temporal trends well, but they often fail to fully correct localized forecasting residuals.

GridSageAI addresses this problem through:

# Hybrid Residual Learning

The architecture combines:

* sequential deep learning
  with
* gradient-boosted residual correction

to improve robustness and forecasting precision.

---

# Core Features

## Intelligent Hybrid Forecasting

* LSTM temporal sequence learning
* XGBoost residual correction
* final hybrid prediction fusion

---

## Realistic Smart-Grid Simulation

The system models:

* hourly electricity demand
* seasonal variations
* daily usage cycles
* temperature-driven demand
* random operational fluctuations
* extreme heatwave/grid-stress events

---

## Research-Oriented Evaluation

GridSageAI evaluates forecasting quality using operational smart-grid metrics including:

* MAE
* RMSE
* MAPE
* SMAPE
* NRMSE
* R² Score
* Peak-Hour MAE
* 95th Percentile Error
* Maximum Forecasting Error
* Energy Misallocation (GWh)

---

## Operational Smart-Grid Relevance

The forecasting system is designed around real operational challenges such as:

* reserve scheduling
* generation balancing
* peak-hour demand stability
* energy efficiency optimization
* smart-grid planning
* renewable energy integration

---

# Hybrid Forecasting Architecture

## Stage 1 — LSTM Forecasting

The LSTM network learns:

* long-term temporal dependencies
* electricity usage behavior
* sequential demand evolution
* seasonal and daily demand patterns

This stage captures the primary forecasting structure.

---

## Stage 2 — Residual Learning using XGBoost

Residual learning calculates:

Residual = Actual Demand − LSTM Prediction

The XGBoost model then learns the remaining forecasting error patterns.

This improves:

* nonlinear correction capability
* anomaly handling
* peak-demand forecasting
* operational robustness

---

## Final Hybrid Prediction

Final Forecast =
LSTM Forecast + Residual Correction

This two-stage architecture allows GridSageAI to outperform standalone forecasting models.

---

# Scalability

One of the key strengths of GridSageAI is scalability.

The same framework can be adapted for:

## Small-Scale Systems

Examples:

* university campuses
* hospitals
* microgrids
* industrial facilities

Typical Demand:
5–100 MW

---

## Medium-Scale Systems

Examples:

* smart cities
* industrial zones
* utility districts

Typical Demand:
500–5000 MW

---

## Large-Scale Systems

Examples:

* state power grids
* national smart-grid systems
* renewable-integrated utility networks

Typical Demand:
10–100+ GW

The framework can scale simply by:

* adjusting baseline demand,
* retraining models,
* and adapting operational variability.

---

# Why Peak-Hour Forecasting Matters

Peak demand periods place maximum stress on electrical infrastructure.

Poor forecasting during peak hours may cause:

* transformer overload,
* emergency power procurement,
* voltage instability,
* and increased operational cost.

GridSageAI separately evaluates:

# Peak-Hour MAE (6 PM – 10 PM)

to better simulate real-world operational forecasting requirements.

---

# Energy Misallocation Analysis

Even small hourly forecasting errors accumulate over time.

GridSageAI evaluates:

# Yearly Energy Misallocation (GWh)

to estimate cumulative operational inefficiency.

Lower energy misallocation implies:

* better grid efficiency,
* reduced energy wastage,
* lower balancing cost,
* and improved reserve planning.

---

# Why Hybrid Models Perform Better

## Standalone LSTM

Good at:

* temporal learning
* trend understanding
* sequence modeling

Limitations:

* struggles with localized nonlinear errors
* smooths sudden spikes
* weaker anomaly correction

---

## Hybrid LSTM + XGBoost

Advantages:

* better nonlinear correction
* improved spike handling
* reduced cumulative forecasting error
* stronger peak-hour robustness
* lower operational energy deviation

The hybrid system combines:

* temporal intelligence
  with
* residual optimization.

---

# Technologies Used

* Python
* PyTorch
* XGBoost
* Streamlit
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---

# Deployment

The project frontend is deployed using Streamlit for interactive visualization and demonstration.

---

# Future Improvements

Potential future extensions include:

* real-world utility datasets
* transformer-based forecasting
* probabilistic forecasting
* renewable energy balancing
* reinforcement learning optimization
* IoT-integrated smart-grid systems
* edge AI deployment
* real-time adaptive forecasting

---

# Results Summary

Experimental evaluation showed that the hybrid framework:

* reduced forecasting error,
* improved peak-hour prediction,
* lowered yearly energy misallocation,
* and demonstrated stronger robustness against nonlinear demand spikes

compared to:

* heuristic baselines
* standalone LSTM forecasting systems.

---

# Authors

### Vansh Baraswal

### Moksh Malik
