# 🛍️ Customer Segmentation Using Clustering

A machine learning project that applies unsupervised clustering algorithms — **K-Means** and **Hierarchical Clustering** — to segment mall customers based on their spending behavior and income. Results are visualized using PCA and evaluated with the Elbow Method and Silhouette Score.

---

## 📁 Repository Structure

```
Customer_Segmentation_Clustering/
│
├── data/
│   ├── Mall_Customers.csv       # Raw dataset (200 customers, 5 features)
│   └── df_scaled.csv            # Preprocessed & scaled dataset
│
├── notebooks/
│   ├── 01_eda.ipynb             # Exploratory Data Analysis
│   ├── 02_preprocessing.ipynb   # Data Cleaning & Feature Scaling
│   └── 03_clustering.ipynb      # Clustering Algorithms & Evaluation
│
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

---

## 📊 Dataset

- **Source:** Mall Customers dataset (`Mall_Customers.csv`)
- **Records:** 200 customers
- **Features:**
  | Column | Description |
  |---|---|
  | CustomerID | Unique customer identifier |
  | Genre | Gender of the customer |
  | Age | Age of the customer |
  | Annual Income (k$) | Annual income in thousands |
  | Spending Score (1-100) | Mall-assigned spending score |

---

## 📓 How to Run the Notebooks

### 1. Clone / Open the Project

Open the project folder in VS Code or your preferred environment.

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter

```bash
jupyter notebook
```

Or use **VS Code** with the Jupyter extension — simply click on any `.ipynb` file to open it.

### 4. Run Notebooks in Order

| Step | Notebook | Description |
|------|----------|-------------|
| 1️⃣ | `01_eda.ipynb` | Load data, explore distributions, visualize correlations |
| 2️⃣ | `02_preprocessing.ipynb` | Handle missing values, encode categories, scale features |
| 3️⃣ | `03_clustering.ipynb` | Apply K-Means & Hierarchical Clustering, evaluate & visualize |

> ⚠️ **Run notebooks in order (01 → 02 → 03)**, as each notebook depends on outputs from the previous one. `02_preprocessing.ipynb` generates `df_scaled.csv` used by `03_clustering.ipynb`.

---

## 🔍 Key Conclusions

1. **Optimal Clusters:** The **Elbow Method** and **Silhouette Score** both confirmed that **5 clusters** is the optimal number of customer segments.

2. **K-Means vs Hierarchical:**
   - Both algorithms produced consistent and comparable cluster structures.
   - K-Means was faster; Hierarchical clustering provided a useful **dendrogram** for visual interpretation.

3. **Identified Customer Segments:**
   | Cluster | Profile |
   |---------|---------|
   | 1 | High income, High spending — 🌟 Target VIPs |
   | 2 | Low income, High spending — ⚠️ Potential risk group |
   | 3 | High income, Low spending — 💡 Upsell opportunity |
   | 4 | Low income, Low spending — 📉 Budget-conscious |
   | 5 | Medium income, Medium spending — 🔄 Average customers |

4. **PCA Visualization** confirmed well-separated clusters in 2D space, validating the quality of segmentation.

5. **Gender & Age** had minor influence on cluster formation; **Annual Income** and **Spending Score** were the primary drivers.

---

## ⏱️ Time Spent Per Task

| Task | Description | Time Spent |
|------|-------------|------------|
| Dataset Research & Setup | Finding dataset, setting up folder structure | 9:00 AM – 9:30 AM |
| EDA (`01_eda.ipynb`) | Exploring distributions, correlation heatmap, pair plots | 9:30 AM – 11:00 AM |
| Preprocessing (`02_preprocessing.ipynb`) | Encoding, scaling, saving `df_scaled.csv` | 11:00 AM – 12:00 PM |
| Lunch Break | — | 12:00 PM – 1:00 PM |
| Clustering (`03_clustering.ipynb`) | K-Means, Elbow method, Silhouette score | 1:00 PM – 2:30 PM |
| Hierarchical Clustering & Dendrogram | Agglomerative clustering, dendrogram visualization | 2:30 PM – 3:30 PM |
| PCA Visualization | Reducing to 2D, plotting cluster results | 3:30 PM – 4:15 PM |
| README & Cleanup | Writing documentation, requirements.txt | 4:15 PM – 5:00 PM |
| **Total** | | **~7 hrs (9 AM – 5 PM)** |

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Jupyter Notebook**
- `pandas`, `numpy` — Data manipulation
- `matplotlib`, `seaborn` — Visualization
- `scikit-learn` — Clustering & preprocessing
- `scipy` — Hierarchical clustering & dendrogram

---

## 👤 Author

**Muhammed Riswan P**  
*Bridgeon Solutions — Weekly Task Submission*  
*Date: February 25, 2026*
