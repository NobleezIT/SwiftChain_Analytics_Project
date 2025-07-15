# 📦 **SwiftChain Analytics Capstone Project**

## Predictive Modeling for Delivery Delay Classification

---

## 🏢 **About SwiftChain Analytics**

SwiftChain Analytics is a global leader in logistics optimization, leveraging machine learning and data-driven insights to help businesses improve delivery performance, reduce costs, and achieve operational excellence. In 2024, the company initiated a project to predict delivery delays using historical logistics data, aiming to enhance customer satisfaction and streamline operations.

---

## 🎯 **Project Objective**

Develop and evaluate a predictive model to classify delivery delays, using historical order, customer, product, and shipping data. The classification categories include:

* `Late Delivery`
* `On-time Delivery`
* `Early Delivery`

Insights from this project will enable proactive solutions to reduce delays and optimize supply chain performance.

---

## 📊 **Dataset Overview**

* Total Records: 15,549
* Features: 41 original variables, including:
  ✔ Customer demographics
  ✔ Order details
  ✔ Product information
  ✔ Shipping modes
  ✔ Delivery outcomes

**Target Variable:**
`label` → Delivery status:
`-1` = Late | `0` = On-Time | `1` = Early

---

## 🛠 **Methodology**

### ✅ Phase 1: Problem Understanding

* Defined the business impact of delivery delays on operational efficiency and customer satisfaction.
* Reviewed key dataset variables contributing to delivery patterns.

### ✅ Phase 2: Exploratory Data Analysis (EDA)

* Inspected dataset structure, data types, and value distributions.
* Visualized relationships between shipping modes, delivery outcomes, and geographic factors.
* Identified and addressed missing values, unrealistic date entries, and outliers.

### ✅ Phase 3: Data Preprocessing

* Encoded categorical variables using one-hot encoding.
* Removed high-cardinality, non-informative columns (e.g., IDs).
* Created new features:
  ✔ `shipping_duration` (order to shipping time)
  ✔ Scaled profit and sales variables for modeling consistency

### ✅ Phase 4: Feature Engineering & Selection

* Analyzed feature importance to identify top predictors of delays.
* Eliminated redundant or weakly correlated features to enhance model focus.

### ✅ Phase 5: Model Development

* Train-Test Split: 80% training, 20% testing

* Models Evaluated:
  ✔ Logistic Regression
  ✔ Random Forest
  ✔ XGBoost

* Remapped target labels to `[0 = Late, 1 = On-Time, 2 = Early]` for compatibility

* Evaluation Metrics: Accuracy and F1 Score (macro average)

---

## 🧮 **Model Performance Summary**

| Model               | Accuracy | F1 Score (macro) | Key Observations               |
| ------------------- | -------- | ---------------- | ------------------------------ |
| Logistic Regression | 56%      | 0.24             | Limited handling of complexity |
| Random Forest       | 58%      | 0.39             | Stronger baseline performance  |
| XGBoost             | 57%      | 0.45             | Best model overall             |

Real-world logistics involve complex factors; a \~58% accuracy significantly exceeds random classification (33%).

---

## 🔑 **Key Findings: Feature Importance**

Top predictors influencing delivery delay:

* `shipping_mode_Standard Class` — Strongest impact on delay likelihood
* `shipping_duration` — Delays linked to longer/unrealistic shipping times
* `latitude` & `longitude` — Geographic regions show varied delay patterns
* Profit-related variables — High-profit orders may influence prioritization
* Discounts and order size — Promotional or complex orders risk higher delays

---

## 💡 **Recommendations for SwiftChain Analytics**

✔ **Shipping Mode Optimization:**

* Review Standard Class shipping processes and carrier performance
* Explore alternative shipping options for high-delay lanes

✔ **Shipping Duration Management:**

* Clean and validate operational data pipelines
* Reduce delays between order placement and shipment

✔ **Regional Interventions:**

* Target high-delay geographic areas for logistics improvement
* Consider expanding regional distribution hubs

✔ **Product & Order Complexity Handling:**

* Improve resource planning for high-margin or discounted orders
* Align promotional activities with fulfillment capacity

✔ **Time-based Operational Adjustments:**

* Optimize staffing and processes around high-delay periods (specific days or months)

---

## 📈 **Next Steps**

* Pilot operational improvements based on model insights
* Continuously refine the predictive model with additional data
* Explore advanced techniques (balancing, ensemble models) to boost performance

---

# 🏁 **Conclusion**

This project provides SwiftChain Analytics with a data-driven foundation to predict and reduce delivery delays. While classification accuracy presents improvement opportunities, current insights enable actionable steps to enhance logistics efficiency, customer satisfaction, and competitive advantage.
