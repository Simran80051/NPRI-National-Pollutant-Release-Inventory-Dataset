#
</p>

<p align = "center" draggable=”false” ><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8HNB-ex4xb4H3-PXRcywP5zKC_3U8VzQTPA&usqp=CAU" 
     width="200px"
     height="auto"/>
</p>

<h1 align="center" id="heading">
<h1 align="center" id="heading">  🏭 National Pollutant Release Inventory Dataset

<p align = "center" draggable=”false” ><img src="https://th.bing.com/th/id/R.9e234304d59bac1062f396d79c82b5c5?rik=BGXFD8Xeut6hew&pid=ImgRaw&r=0" 
     width="200px"
     height="auto"/>
</p>

## 🌎 NPRI Environmental Impacts Prediction Project

### 🔬 Project Overview

This project involves the exploration, cleaning, and analysis of data from the **National Pollutant Release Inventory (NPRI)**. The NPRI is Canada’s public inventory of pollutant releases, disposals, and transfers, helping ensure transparency and environmental accountability. This project is a collaboration between **CMPT 2400 (Data Analytics & Preparation)** and **CMPT 3510 (Machine Learning I)**, focusing on predicting environmental trends using Canada's **National Pollutant Release Inventory (NPRI)** dataset (2000–2022). The goal is to transform environmental data into time-series-compatible formats, enabling meaningful **classification and regression modeling**.

> 🧠 **Team Focus:**  
>  **Predicting trends of criteria air contaminants (Sulphur dioxide, Nitrogen oxides, volatile organic compounds, particulate matter, and carbon monoxide) for the next five years.**

---

## 📁 Dataset

- **Source**: [Environment Climate Change Canada](https://www.canada.ca/en/environment-climate-change.html)
- **Time Range**: 2000 to 2022
- **Scope**: Pollutant releases across various industries and provinces
- **Focus Pollutants**:
  - Sulphur Dioxide (SO₂)
  - Nitrogen Oxides (NOₓ)
  - Volatile Organic Compounds (VOCs)
  - Particulate Matter (PM)
  - Carbon Monoxide (CO)

---

## 🛠️ Project Phases

### 🔹 Phase 1: Data Cleaning, Classification & Time Series Preparation

#### **Understanding the Data**
- The dataset consists of **Releases** and **Disposals** datasets, with data on pollutant releases, disposals, and transfers from different sectors and regions.
- **Releases Dataset**: Contains pollutant release information.
- **Disposals Dataset**: Includes disposal and transfer details for pollutants.
  
- **Exploratory Data Analysis**:
  - The data structure includes year, pollutant type, industry, province, and quantity released.
  - Research into health/environmental impacts of target pollutants.
  - Linked pollutant patterns with policy events (e.g., 2019 Carbon Pricing Policy).

#### **Issue Detection**
- Identified:
  - Inconsistent naming formats
  - Missing values for smaller facilities and city data
  - Outliers in emissions due to extreme reporting events

#### **Data Cleaning & Preparation**
- Renamed columns for clarity.
- Converted measurement units for consistency.
- Removed rows with inconsistent facility IDs.

#### **Handling Outliers**
- Identified extreme values using IQR and Z-scores.

#### **Handling Missing Values**
- Applied interpolation for time-series gaps.
- Used mean imputation for facilities with sparse data.

#### **Time-Series Preparation & Classification**
- Transformed raw data into a time-series structure.
- Created pollutant categories (e.g., low, medium, high) for classification.
- Built and evaluated classification models to detect pollutant trends.
- Documented assumptions and preprocessing strategies for classification.

---

### 🔹 Phase 2: Regression & Prediction

#### **Aligning & Merging Datasets**
- Cleaned and merged the Releases dataset (2000–2020) with the Disposals dataset.
- Ensured consistency in time intervals and grouped data by year, pollutant, and sector.

#### **Feature Engineering**
- Encoded categorical features like **industry** and **province**.
- Normalized pollutant release quantities using **MinMaxScaler**.
- Added new features:
  - Rolling averages
  - Lag features
  - Policy-year flags (e.g., carbon pricing start in 2019)

#### **Feature Selection**
- Used techniques like:
  - Pearson Correlation
  - Correlation filtering
- Justified the inclusion of key predictors based on pollutant behavior.

#### **Regression Modeling**
- Developed regression models to forecast pollutant releases over the next 5 years.
- Employed techniques such as:
  - Time-series windowing
  - Trend decomposition
- Evaluated model performance with metrics like RMSE and R².

---

## 🔧 Tools & Technologies

- **Python** (Pandas, NumPy, Scikit-learn)
- **Jupyter Notebook**
- **Matplotlib , Seaborn, Plotly** – for visualization
- **Google Colab** – for collaborative model development

---

## 👏 Acknowledgements

Special thanks to **Environment and Climate Change Canada (ECCC)** for giving us such an amazing project to work on, and   
**Instructor Nasimeh Asgarian and Mohammad Ajallooeian** for their guidance and support.

