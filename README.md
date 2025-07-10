# Brazilian E-commerce Customer Segmentation

**This README includes both English and 中文 versions.**  
**Click to jump to: [English Version](#english-version) | [中文说明](#中文说明)**

---

## English Version

A customer segmentation project based on Brazilian e-commerce data, combining RFM modeling, KMeans clustering, and LightGBM simulation. 

[Kaggle Notebook Link](https://www.kaggle.com/code/yiquanxiao/brazilian-e-commerce-customer-segmentation)

---

### Purpose

This project helps you:
- Segment users using RFM rules and KMeans clustering.
- Understand behavioral patterns across different user groups.
- Simulate clustering results using LightGBM for real-time labeling.
- Support targeted marketing and customer value analysis.

---

### Directory Structure

```

brazilian-ecommerce-olist/
│   README.md
│   .gitignore
│   requirements.txt
│
└── customer segmentation/
└── brazilian-e-commerce-customer-segmentation.ipynb

````

---

### How to Use

#### 1️. Prepare the Dataset

Create a new Notebook for [Olist e-commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) on Kaggle OR directly download to local directory.

#### 2️. Run the Notebook

Open `brazilian-e-commerce-customer-segmentation.ipynb` and follow these steps:
- Preprocess order, customer, and payment data.
- Calculate RFM features.
- Apply rule-based segmentation and KMeans clustering.
- Train a LightGBM model to simulate clustering results.
- Interpret clusters using SHAP and visualize key patterns.

---

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
````

---

### Notes

* The LightGBM model is used to approximate KMeans labels, enabling near real-time customer scoring in production.
* Feature importance and SHAP plots provide insights into what drives customer grouping.

---

## 中文说明

一个基于巴西电商数据的用户分层项目，结合 RFM 规则建模、KMeans 聚类与 LightGBM 模拟，实现用户画像构建与实时打标签。

[Kaggle Notebook Link](https://www.kaggle.com/code/yiquanxiao/brazilian-e-commerce-customer-segmentation)

---

### 项目目的

该项目旨在：

* 使用 RFM 模型和 KMeans 对用户进行行为分群。
* 理解不同用户群的消费模式。
* 利用 LightGBM 模拟聚类结果，实现实时用户打标签。
* 支持精细化营销和用户价值分析。

---

### 目录结构

```
brazilian-ecommerce-olist/
│   README.md
│   .gitignore
│   requirements.txt
│
└── customer segmentation/
    └── brazilian-e-commerce-customer-segmentation.ipynb
```

---

### 使用方法

#### 1️. 准备数据

在 [Kaggle 数据源](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) 上新建 Notebook 或者直接下载 Olist 电商数据到本地。

#### 2️. 运行 Notebook

打开 `brazilian-e-commerce-customer-segmentation.ipynb`，依次完成以下步骤：

* 预处理订单、客户和支付数据。
* 计算 RFM 特征。
* 使用规则与 KMeans 进行用户聚类。
* 用 LightGBM 拟合聚类标签，模拟打标签过程。
* 借助 SHAP 工具可视化特征重要性与分群依据。

---

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

---

### 注意事项

* 本项目使用 LightGBM 模拟聚类标签，可用于线上实时标签预测。
* 使用 SHAP 可视化模型关键特征，辅助运营人员理解不同用户群体的画像。
