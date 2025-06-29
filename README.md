# McDonald's Market Segmentation Analysis

This project performs an in-depth analysis of a customer survey dataset for McDonald's. The primary goal is to understand customer perceptions, identify distinct market segments through clustering, and create profiles for each segment to inform targeted marketing strategies.

## 📋 Table of contents
- [Goals](#-Project-goals)
- [Dataset](#-Dataset)
- [Methodology](#-Methodology)
- [Key findings](#-Key-findings)
- [Visualizations](#-Visualizations)
- [How to run](#⚙-How-to-run)
- [Files](#-Files)

- License

## 🏆 Project goals

1. Identify the key factors that drive customer perception of McDonald's.

2. Segment customers into distinct groups based on their perceptions and demographics.

3. Profile each segment to understand their unique characteristics.

4. Provide actionable insights for McDonald's to tailor marketing campaigns and product offerings to different customer segments.

## 💾 Dataset

The analysis is based on the `mcdonalds.csv` dataset, which contains survey responses from 1453 individuals. The dataset includes:

- **Perception Attributes (Yes/No):** Customer opinions on attributes like `tasty`, `convenient`, `spicy`, `healthy`, `cheap`, etc.
    
- **Age:** The age of the respondent.
    
- **Visit Frequency:** How often the respondent visits McDonald's.
    
- **Gender:** The gender of the respondent.

![Pasted image 20240617142944](https://github.com/user-attachments/assets/8ed2cbf0-a5ad-419a-905a-322134c56164)


## 🔬 Methodology

The analysis is conducted in a Jupyter Notebook (`McDonald's Data Analysis.ipynb`) and follows a structured data science workflow:

1. **Data Loading and Cleaning:** The dataset is loaded, and the categorical 'Yes'/'No' responses for perception attributes are converted into binary format (1/0) for numerical analysis.
    
2. **Exploratory Data Analysis (EDA):** Initial analysis is performed to understand data distributions, such as the gender and age breakdown of respondents.
    
3. **Dimensionality Reduction (PCA):** Principal Component Analysis (PCA) is applied to the 11 perception attributes to reduce dimensionality and extract the most important underlying factors that explain the variance in customer perceptions.
    
4. **Clustering (K-Means):** The K-Means clustering algorithm is used on the PCA-transformed data to group customers into a set number of segments. The optimal number of clusters is determined using the "Elbow Method".
    
5. **Segment Profiling:** Each cluster (segment) is analyzed in detail. We cross-tabulate the segments with demographic variables (age, gender) and visit frequency to build a comprehensive profile for each customer group.

### 📊 Key findings

The analysis successfully identified four distinct customer segments:

- **Fans:** These customers generally have a positive perception of McDonald's, but visit less frequently. They are typically older and may be more health-conscious.
    
- **Lovers:** This group loves McDonald's, visits frequently, and holds positive views across most attributes. They represent a core, loyal customer base.
    
- **Critics:** This segment holds a strong negative perception of McDonald's, particularly regarding taste and quality. They are the least frequent visitors.
    
- **Practical:** This segment is primarily driven by convenience and speed. They may not love the food but value McDonald's for its practicality. They are often younger.

![Pasted image 20240617143900](https://github.com/user-attachments/assets/ed5de3d0-1f40-4c05-8ff9-3fe76495ee43) 

### 📈 Visualizations

The analysis includes several key visualizations to interpret the data and cluster results: 

- Correlation matrices to show the relationships between the different perception attributes: ![image](https://github.com/user-attachments/assets/16996f1f-aeb2-44f6-a9a1-03d217e1ed77)

- A Biplot which overlays the original perception variables (vectors) on the PCA plot to show how they contribute to the principal components: ![image](https://github.com/user-attachments/assets/b962fe5b-b8a7-4e05-b398-ebf8f46935e6)

- An **Elbow Method plot** to justify the choice of four clusters: ![image](https://github.com/user-attachments/assets/0f2a886e-5872-4646-92db-dce02af10273)
    
- A **Cluster Profile Plot** that shows the average perception scores for each attribute across the four segments, making it easy to compare them: ![image](https://github.com/user-attachments/assets/43f47156-3ac4-4988-aeab-561ed6d97e2c)


## ⚙️ How to run

To replicate this analysis on your local machine, follow these steps:

### 1. Prerequisites

Ensure you have Python 3 installed. You will need the following py libraries:

- [x] pandas
    
- [x] numpy
    
- [x] scikit-learn
    
- [x] matplotlib
    
- [x] seaborn
    
- [x] jupyter
    

### 2. Clone the Repository

```
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 3. Run the Jupyter Notebook

Launch Jupyter Notebook and open the analysis file:

```
jupyter notebook "McDonald's Data Analysis.ipynb"
```

You can then run the cells sequentially to see the full analysis.

## 📂 Files

- **`mcdonalds.csv`**: The raw survey dataset used for the analysis.
    
- **`McDonald's Data Analysis.ipynb`**: The complete Jupyter Notebook containing the Python code for data cleaning, analysis, PCA, clustering, and visualization.
    
- **`McDonalds_analysis_report.md`**: A detailed report summarizing the methodology and findings of the analysis.

- **`McDonalds_analysis_export.pdf`**: Exported Jupyter notebook.
    
- **MIT license**.
    

## 📜 License

This project is licensed under the MIT License. See the [LICENSE.txt](https://github.com/kiycoh/mcdonalds-customer-analysis/blob/main/LICENSE) file for details.
