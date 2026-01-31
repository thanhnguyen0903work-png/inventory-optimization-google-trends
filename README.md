📌 Project Overview

This project demonstrates how demand forecasting can be translated into cost-optimised inventory decisions under real-world constraints.

Using Google Trends data as a demand signal, I built a demand forecasting model and developed an inventory ordering strategy that balances fixed ordering costs and holding costs, with the objective of minimising total operational cost while meeting customer demand.

This project reflects a typical business analytics / operations analyst workflow:

Data → Forecast → Decision → Cost impact

🧠 Business Problem

A laptop retailer faces the following challenge:

Demand fluctuates with online search interest

Ordering inventory incurs:

Fixed ordering cost: $2,000 per order

Holding cost: $1 per unit per month

Monthly order capacity is capped at 6,000 units

Objective

Determine an optimal ordering strategy for the next 4 months that satisfies demand while minimising total cost.

📊 Data Source

Google Trends: Search interest for the keyword “laptop”

Time granularity: Monthly

Tooling: pytrends

Google Trends is used as a leading indicator of consumer demand, a common technique in retail and demand sensing.

🔍 Analytical Approach
1️⃣ Demand Forecasting

Demand is modelled using the following relationship:

Demand = 100 + 20 × Google Trends Index


This reflects the assumption that online search interest has a linear relationship with purchase demand.

Steps:

Collected historical Google Trends data

Cleaned and visualised the time series

Generated demand forecasts for the next 4 months

2️⃣ Inventory Decision Logic

The ordering strategy considers:

Forecasted monthly demand

Fixed cost per order

Inventory holding cost

Order capacity constraint

Rather than ordering every month, the model evaluates when it is more cost-effective to:

Place fewer large orders (saving fixed costs)

Hold inventory to cover future demand

3️⃣ Cost Evaluation

Total cost is decomposed into:

Ordering Cost = Number of orders × $2,000

Holding Cost = Inventory held × $1 × months

This enables clear trade-off analysis between:

Order frequency

Inventory levels

Cost efficiency

📈 Key Insights

High fixed ordering costs incentivise batch ordering

Ordering too frequently significantly increases total cost

Holding limited excess inventory is often cheaper than placing additional orders

Demand sensing using external data (Google Trends) can meaningfully improve planning decisions

🛠 Tools & Technologies

Python

pandas, numpy

matplotlib

pytrends

Jupyter Notebook
