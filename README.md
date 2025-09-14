# Brazilian E-commerce Data Analysis

**This README includes both English and 中文 versions.** **Click to jump to: [English Version](#english-version) | [中文说明](#中文说明)**

-----

## English Version

An analysis project based on Brazilian e-commerce data. It includes two main parts: **Customer Segmentation** and **User Analysis (Cohort Retention & LTV Prediction)**. This project combines RFM modeling, K-Means clustering, Cohort Analysis, and LightGBM for simulation and prediction.

**Kaggle Notebook Links:**

  * **Part 1 - Customer Segmentation:** [Link](https://www.kaggle.com/code/yiquanxiao/brazilian-e-commerce-customer-segmentation)
  * **Part 2 - User Analysis:** [Link](https://www.kaggle.com/code/yiquanxiao/brazilian-e-commerce-user-analysis-cohort-retenti)

-----

### Purpose

This project helps you:

  - **(Part 1)** Segment users using RFM rules and K-Means clustering.
  - **(Part 1)** Simulate clustering results using LightGBM for real-time labeling.
  - **(Part 2)** Analyze user retention patterns over time through Cohort Analysis.
  - **(Part 2)** Compare behavioral differences across different customer segments.
  - **(Part 2)** Build a simplified model to predict the Lifetime Value (LTV) of customers.
  - Support targeted marketing, customer value analysis, and operational decision-making.

-----

### Directory Structure

```
brazilian-ecommerce-olist/
│   .gitignore
│   LICENSE
│   README.md
│   requirements.txt
│
├───customer segmentation/
│       brazilian-e-commerce-customer-segmentation.ipynb
│
└───user analysis/
        brazilian-e-commerce-user-analysis-cohort-retenti.ipynb
```

-----

### How to Use

#### 1️. Prepare the Dataset

Create a new Kaggle Notebook using the [Olist e-commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) OR download the data to your local directory.

#### 2️. Run the Notebooks

  - For customer segmentation, open `customer segmentation/brazilian-e-commerce-customer-segmentation.ipynb` to run the RFM and K-Means analysis.
  - For user analysis, open `user analysis/brazilian-e-commerce-user-analysis-cohort-retenti.ipynb` to run the cohort retention and LTV prediction analysis.

-----

### Requirements

  - Python 3.8+
  - pandas
  - numpy
  - matplotlib / seaborn
  - scikit-learn
  - lightgbm
  - shap
  - jupyter

Install via:

```bash
pip install -r requirements.txt
```

-----

### Notes

  * The **LightGBM model (Part 1)** is used to approximate K-Means labels, enabling near real-time customer scoring in production. SHAP plots provide insights into what drives customer grouping.
  * **Cohort Analysis (Part 2)** reveals retention trends and is broken down by the customer clusters from Part 1 for deeper comparative insights.
  * The **simplified LTV model (Part 2)** uses an `LGBMRegressor` to predict future 6-month GMV based on historical features (RFM, etc.), with Mean Absolute Error (MAE) as the key evaluation metric.

-----

## 中文说明

一个基于巴西电商数据的分析项目，包含 **用户分层** 与 **用户分析（留存与LTV预测）** 两大部分。项目结合 RFM 规则建模、KMeans 聚类、同期群分析与 LightGBM 模拟及预测。

**Kaggle Notebook 链接:**

  * **第一部分 - 用户分层:** [链接](https://www.kaggle.com/code/yiquanxiao/brazilian-e-commerce-customer-segmentation)
  * **第二部分 - 用户分析:** [链接](https://www.kaggle.com/code/yiquanxiao/brazilian-e-commerce-user-analysis-cohort-retenti)

-----

### 项目目的

该项目旨在：

  * **(第一部分)** 使用 RFM 模型和 K-Means 对用户进行行为分群。
  * **(第一部分)** 利用 LightGBM 模拟聚类结果，实现实时用户打标签。
  * **(第二部分)** 通过同期群分析（Cohort Analysis）洞察用户留存规律。
  * **(第二部分)** 对比不同用户分群的行为模式差异。
  * **(第二部分)** 构建简版模型，预测用户生命周期价值（LTV）。
  * 支持精细化营销、用户价值分析及运营决策。

-----

### 目录结构

```
brazilian-ecommerce-olist/
│   .gitignore
│   LICENSE
│   README.md
│   requirements.txt
│
├───customer segmentation/
│       brazilian-e-commerce-customer-segmentation.ipynb
│
└───user analysis/
        brazilian-e-commerce-user-analysis-cohort-retenti.ipynb
```

-----

### 使用方法

#### 1️. 准备数据

在 [Kaggle 数据源](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) 上新建 Notebook 或者直接下载 Olist 电商数据到本地。

#### 2️. 运行 Notebook

  * 如需进行用户分层，请打开 `customer segmentation/brazilian-e-commerce-customer-segmentation.ipynb` 运行 RFM 与 KMeans 分析。
  * 如需进行用户分析，请打开 `user analysis/brazilian-e-commerce-user-analysis-cohort-retenti.ipynb` 运行留存分析与 LTV 预测。

-----

### 运行环境

  * Python 3.8+
  * pandas
  * numpy
  * matplotlib / seaborn
  * scikit-learn
  * lightgbm
  * shap
  * jupyter

使用以下命令安装依赖：

```bash
pip install -r requirements.txt
```

-----

### 注意事项

  * **LightGBM 模型（第一部分）** 用于拟合聚类标签，可用于线上实时用户评分。使用 SHAP 可视化关键特征，辅助运营人员理解用户画像。
  * **同期群分析（第二部分）** 揭示了用户的留存趋势，并按第一部分的用户分群进行拆解，以获得更深入的对比洞察。
  * **简版LTV模型（第二部分）** 使用 `LGBMRegressor` 基于历史特征（RFM等）预测未来6个月的GMV，并以平均绝对误差（MAE）作为关键评估指标。
