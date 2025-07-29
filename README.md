# 🛒 Shopper Spectrum: Customer Segmentation & Product Recommendation

## 📌 Domain
This project falls under the domain of **E-Commerce and Retail Analytics**. It leverages customer transaction data to uncover purchasing patterns. These insights support strategic decisions such as personalized marketing and product recommendations.

## 🎯 Project Introduction
This machine learning project segments customers and recommends products using clustering and collaborative filtering techniques. It is implemented in Python and deployed using Streamlit.

## 🚀 Objective
- Segment customers using RFM (Recency, Frequency, Monetary) analysis and KMeans clustering  
- Recommend similar products using item-based collaborative filtering

---

## 📁 Dataset
- **Source**: UCI Online Retail Dataset
- **Columns**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

---

## 🧠 Workflow Summary

### 1. Data Preprocessing
- Remove missing CustomerIDs and cancelled transactions
- Compute `TotalPrice` = `Quantity × UnitPrice`

### 2. RFM Feature Engineering
- **Recency**: Days since last transaction  
- **Frequency**: Number of unique purchases  
- **Monetary**: Total money spent

### 3. Clustering (KMeans)
- Scale RFM data using StandardScaler
- Apply Elbow Method + Silhouette Score to choose optimal clusters
- Assign clusters and interpret as High-Value, Regular, Occasional, At-Risk

### 4. Product Recommendation
- Create Customer-Product matrix
- Use cosine similarity to identify product similarity
- Recommend top 5 similar products

---

## 💾 Model Saving
- `kmeans_model.pkl`: Trained clustering model
- `scaler.pkl`: RFM scaler
- `item_similarity.pkl`: Cosine similarity matrix for product recommendation

---

## 🖥️ Web Application
- Built using **Streamlit**
- Features:
  - 📊 Input RFM values for customer segmentation
  - 🔍 Input product code for recommendations

---

## ✅ Conclusion
This project enables businesses to identify valuable customer segments and provide personalized product suggestions. KMeans and item-based filtering were chosen for their scalability and interpretability on structured transaction data.

---

