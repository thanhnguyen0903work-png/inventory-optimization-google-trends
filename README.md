## 📦 Inventory Optimization & Demand Forecasting  
Using Google Trends Data

## 📌 Project Overview
This project demonstrates how demand forecasting can be translated into **cost-optimised inventory decisions** under real-world operational constraints. Using Google Trends data as a demand signal, the analysis focuses on converting forecasts into actionable ordering strategies that balance fixed ordering costs, inventory holding costs, and capacity limits.

## 🧠 Business Problem
A laptop retailer faces fluctuating demand driven by consumer interest. The business incurs:
- A **fixed ordering cost** of $2,000 per order  
- A **holding cost** of $1 per unit per month  
- A maximum order capacity of **6,000 units per month**

The objective is to determine an ordering strategy for the next four months that satisfies demand while **minimising total operational cost**.

## 📊 Data Source
Demand signals are captured using **Google Trends** search interest for the keyword *“laptop”*. Monthly trend data is collected using the `pytrends` library and used as a proxy for consumer demand.

## 🔍 Analytical Approach

### 1️⃣ Demand Forecasting
Demand is estimated using the following relationship: Demand = 100 + 20 × Google Trends Index
Historical trend data is cleaned, visualised, and projected forward to generate demand forecasts for the planning horizon.

### 2️⃣ Inventory Decision Logic
The ordering strategy considers forecasted demand, ordering costs, holding costs, and capacity constraints. The model evaluates the trade-off between placing frequent small orders versus fewer larger orders while holding inventory to meet future demand.

### 3️⃣ Cost Evaluation
Total cost is decomposed into:
- **Ordering Cost**: number of orders × $2,000  
- **Holding Cost**: inventory held × $1 × time  

This allows for clear comparison of alternative ordering strategies and their cost implications.

## 📈 Key Insights
- High fixed ordering costs incentivise batch ordering.
- Holding limited excess inventory can be more cost-effective than frequent reordering.
- External demand signals such as search trends can improve inventory planning decisions.
- Cost-based reasoning leads to more practical and scalable operational strategies.

## 🛠 Tools & Technologies
- Python  
- pandas, numpy  
- matplotlib  
- pytrends  
- Google Colab 



