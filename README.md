# 🛒 E-commerce Analysis and Seller Churn Prediction
<img width="225" height="225" alt="olist" src="https://github.com/user-attachments/assets/e5c55437-6b64-4c03-a199-ead414592c85" />

**Olist Store**

### Contributor :
- [Kirana Shely](https://github.com/celiii26)
- [Naufal Fajar Revanda](https://github.com/nrevanda)
- [Yanfa Anandika](https://github.com/yanfa121)

### Link
- Tableau Dashboard : [Link](https://public.tableau.com/app/profile/naufal.revanda/viz/dashboard_finpro_Alpha/Dashboard1?publish=yes)
- Streamlit App : [Link](https://olist-churn-predictor.streamlit.app/)

## 1. Project Overview

Olist is a Brazilian e-commerce enablement platform that connects small and medium-sized sellers with major online marketplaces. Since Olist’s primary revenue comes from seller subscription fees and sales commissions, **seller retention becomes a critical business priority**.

However, not all sellers remain active. Many stop selling due to low sales performance, delivery issues, poor profitability, or operational challenges. Seller churn directly impacts Olist’s revenue and platform sustainability.

Therefore, this project aims to **analyze seller behavior, identify churn drivers, and build a machine learning model to predict seller churn using LRFM (Length, Recency, Frequency, Monetary) analysis**.

**Key Objectives:**

1. Identify key factors influencing seller churn.
2. Segment sellers using LRFM behavior analysis.
3. Develop a machine learning model to predict seller churn.
4. Provide actionable business recommendations for seller retention strategies.

---

## 2. Dataset Overview

This project uses the **Olist Store Dataset** from Kaggle, which contains Brazilian e-commerce transaction data from 2016–2018.

The dataset includes multiple relational tables, such as:

- Orders
- Order Items
- Payments
- Sellers
- Products
- Customers
- Reviews
- Geolocation

After data cleaning and merging, the dataset is transformed into a **seller-level dataset** with behavioral and transactional features based on LRFM analysis.

### Key Feature Groups

**Behavioral Features (LRFM):**
- Length (seller lifetime)
- Recency (last transaction)
- Frequency (number of orders)
- Monetary (total revenue)

**Operational Features:**
- Average delivery time
- On-time delivery rate
- Cancellation rate
- Review score

**Financial Features:**
- Average order value
- Total sales revenue
- Freight cost impact

**Target Variable:**
- `churn` → 0 (Active Seller), 1 (Churned Seller)

**Main Challenge:**
- Class imbalance between active and churned sellers.

---

## 3. Technologies Used

- **Programming Language**: Python  
- **Data Processing**: Pandas, NumPy  
- **Visualization**: Matplotlib, Seaborn  
- **Machine Learning**: scikit-learn, imbalanced-learn  
- **Modeling Environment**: Jupyter Notebook  
- **Model Saving**: Pickle / Joblib  

---

## 4. Project Structure

```bash
📁 olist-seller-churn/
├── 📂 dataset/
│   ├── Brazilian Ecommerce Cleaned.csv
│   ├── Brazilian Ecommerce Combined.csv
│   ├── Churn Data.csv
├── 📂 streamlit/
│   ├── app.py
│   ├── bestmodel.mdl
│   ├── requirements.txt
├── 📓 Olist Seller Churn Notebook.ipynb
├── 📝 README.md
├── 📦 paramsxgb.hyp
```

Dashboard Screenshots
<img width="1182" height="815" alt="dashboard1" src="https://github.com/user-attachments/assets/7b6161eb-0f75-49f5-9dd2-ff90e3fd8941" />

Streamlit App Screenshots
<img width="1917" height="912" alt="streamlit1" src="https://github.com/user-attachments/assets/ab610f7d-d31b-461f-9ecd-48d3407b74a8" />

### Deliverables

* Machine Learning Notebook (EDA + Feature Engineering + Modeling)
* Trained Seller Churn Prediction Model
* Business Insight & Recommendation Report

## 5. Summary of Findings

### 5.1 Business Insights

* Seller churn is strongly influenced by **recency of transactions, sales frequency, and total monetary contribution**.
* Sellers with **long inactive periods and low frequency orders** show significantly higher churn probability.
* Delivery performance and customer review scores also contribute to churn risk.
* LRFM features provide strong explanatory power for seller behavior patterns.
* Tree-based models outperform linear models for capturing complex seller behavior dynamics.

---

### 5.2 Actionable Recommendations

#### From the Modeling Perspective

* Experiment with advanced models such as Random Forest, Gradient Boosting, and XGBoost to improve predictive performance.
* Apply additional imbalance handling techniques such as ADASYN and cost-sensitive learning.
* Implement automated retraining to handle changes in seller behavior over time.
* Perform feature expansion such as seasonal sales pattern, promotion participation, and seller response time.

#### From the Business Perspective

* Implement **early-warning churn detection** for high-risk sellers.
* Launch **targeted retention programs** such as fee discounts, logistics support, or promotional boosts for at-risk sellers.
* Develop **loyalty and incentive programs** for top-performing and long-term sellers.
* Improve logistics coordination in regions with poor delivery performance.
* Continuously monitor seller KPIs through business dashboards integrated with the churn model.

---

## 6. Conclusion

This project demonstrates that **machine learning combined with LRFM behavioral analysis can effectively predict seller churn on the Olist platform**. The model provides valuable insights into seller engagement, financial contribution, and operational performance.

The results can support Olist’s business team in designing **data-driven retention strategies**, minimizing revenue loss, and strengthening long-term seller relationships. This project also serves as a strong foundation for further development of more advanced seller analytics systems.

---

## 7. References

* Olist Brazilian E-Commerce Dataset – Kaggle
  [https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
* Olist Business Model & Pricing
  [https://olist.com/planos/](https://olist.com/planos/)
