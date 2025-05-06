# IB Data Science Coursework: Time-Series Analysis & Regression

## 📖 Project Overview
This repository contains a comprehensive coursework project for an IB Data Science class, focused on time-series analysis and regression techniques. Over three core notebooks and a set of targeted exercises, you will learn to:

- Load, visualize, and preprocess real-world time-series data.  
- Fit and evaluate simple linear and polynomial regression models.  
- Detect, model, and interpret periodic (seasonal) components using spectral analysis.  
- Build exponential-growth and Fourier‐augmented models.  
- Perform model selection to balance fit quality against overfitting risk.  

## 📂 Repository Structure
├── 01 Introduction to Time series and Linear regression.ipynb
├── 02 Time series analysis –– capturing periodic components.ipynb
├── 03 Model selection [Optional].ipynb
├── README.md
├── Data/
│ ├── CO2_data_full.npy
│ ├── CO2_training_data.npy
│ ├── CO2_test_data.npy
│ └── CO2_levels.png
└── Exercises/
├── 01 Exercise Notebook 1.ipynb
├── 01 Exercise Notebook 1.pdf
├── 02 Exercise Notebook 2.ipynb
├── 02 Exercise Notebook 2.pdf
├── 03 Exercise Notebook 3.ipynb
├── 03 Exercise Notebook 3.pdf
├── Ex1_polyreg_data.npy
├── hospital_cases_2023-02-16.csv
└── tfl_ridership.csv

## 🗃️ Data Description

### CO₂ Atmospheric Data
- **CO2_data_full.npy**: Monthly measurements of atmospheric CO₂ concentration.  
- **CO2_training_data.npy & CO2_test_data.npy**: Pre‐split subsets for model fitting and validation.  
- **CO2_levels.png**: Visualization highlighting the “sawtooth” seasonal pattern.  

### Example Toy Datasets
- **example_training_data.npy & example_test_data.npy**: Synthetic data to practice model‐selection workflows.  

### Exercises Datasets
- **Ex1_polyreg_data.npy**: Synthetic (x, y) pairs for polynomial regression.  
- **hospital_cases_2023-02-16.csv**: Daily U.K. COVID-19 hospital admissions (Mar 2020–Feb 2023).  
- **tfl_ridership.csv**: Annual London Underground ridership (2000–2019).  

## 📓 Core Notebooks

1. **Introduction to Time Series & Linear Regression**  
   - Load and plot time-series and scatter data.  
   - Build design matrices for linear and polynomial fits using Vandermonde matrices.  
   - Solve least‐squares problems with `np.linalg.lstsq`.  
   - Compute SSE and R² for model assessment.  

2. **Time Series Analysis – Capturing Periodic Components**  
   - Load full CO₂ series; visualize long‐term trend and seasonality.  
   - Compute periodogram to identify dominant frequencies.  
   - Augment linear trend with sine and cosine terms (“Fourier regression”).  
   - Validate seasonally‐adjusted models on held‐out test data.  

3. **Model Selection [Optional]**  
   - Demonstrate train/test splits for unbiased evaluation.  
   - Compare model complexity vs. predictive performance.  
   - Use error metrics (MSE, R²) to guide model choice and avoid overfitting.  

## ✏️ Exercises

- **Exercise 1: Polynomial Regression**  
  Fit polynomials of increasing degree to synthetic data, plot fits, and choose the optimal degree by trading off SSE reduction against model complexity.

- **Exercise 2: Exponential Growth in COVID Hospital Admissions**  
  Subset the Omicron‐surge window (late Dec 2021–early Jan 2022), log-transform counts, fit a linear model to estimate exponential growth rate, and interpret weekly growth percentage.

- **Exercise 3: Seasonal Analysis of London Underground Ridership**  
  Fit a baseline linear trend to ridership data, analyze residuals to detect holiday dips, compute the periodogram for annual cycles, and build a hybrid trend + Fourier model.

## ⚙️ Requirements

- Python 3.7+  
- NumPy  
- pandas  
- Matplotlib  
- Jupyter Notebook  

Install dependencies via:
```bash
pip install numpy pandas matplotlib jupyter
