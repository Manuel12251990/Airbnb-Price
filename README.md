# 🏙️ Airbnb Price Trends in NYC

## 📌 Summary
This Python-based project explores Airbnb pricing trends across New York City boroughs using real-world-inspired data to identify how location, room type, and reviews impact nightly rates.

---

## 🎯 Objective
To analyze Airbnb listings in NYC and answer key questions:
- Which boroughs have the highest and lowest average Airbnb prices?
- How does room type affect price?
- Is there a relationship between number of reviews, availability, and price?

---

## ⚙️ Tools & Environment
- Python 3.11+
- Jupyter Notebook (or Google Colab)
- Libraries: Pandas, Matplotlib, Seaborn

---

## 🧠 Techniques Demonstrated
- Data cleaning and formatting with `pandas`
- Grouping and aggregation
- Visual analysis with `matplotlib` and `seaborn`
- Correlation insights using scatter plots
- Exporting and saving visualizations
---

## 🧾 Code Sample
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Sample Airbnb NYC dataset
data = {
    'neighbourhood_group': ['Manhattan', 'Brooklyn', 'Queens', 'Manhattan', 'Brooklyn'],
    'neighbourhood': ['Harlem', 'Williamsburg', 'Astoria', 'Midtown', 'Bushwick'],
    'room_type': ['Entire home/apt', 'Private room', 'Entire home/apt', 'Private room', 'Entire home/apt'],
    'price': [150, 80, 90, 100, 120],
    'number_of_reviews': [100, 230, 45, 80, 190],
    'availability_365': [200, 300, 150, 180, 220]
}
df = pd.DataFrame(data)

# Average price by borough
avg_price = df.groupby('neighbourhood_group')['price'].mean().reset_index()
sns.barplot(x='neighbourhood_group', y='price', data=avg_price)
plt.title('Average Airbnb Price by Borough')
plt.ylabel('Average Price ($)')
plt.xlabel('Borough')
plt.show()

# Price vs number of reviews
sns.scatterplot(x='number_of_reviews', y='price', hue='room_type', data=df)
plt.title('Price vs Number of Reviews')
plt.xlabel('Number of Reviews')
plt.ylabel('Price ($)')
plt.show()


---

## 🖼️ Output Preview

**📊 Average Airbnb Price by Borough**  
![image](https://github.com/user-attachments/assets/b3ef5e24-1d34-479d-b61b-dd95755a524d)


**📈 Price vs. Number of Reviews**  
![image](https://github.com/user-attachments/assets/08eab8e2-7a13-4a4e-8597-a4bc6a34c1a4)


🔄 Next Steps
Use a full NYC dataset from Inside Airbnb or Kaggle

Incorporate geospatial visuals using folium or plotly

Add boxplots and statistical summaries

Explore simple regression or classification models to predict price or churn



