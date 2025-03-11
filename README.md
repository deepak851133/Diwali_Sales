# 🎇 Diwali Sales Analysis 📊
📌 Project Overview
This project analyzes Diwali sales data to gain insights into customer purchasing behavior, top-selling products, and sales trends. The analysis helps businesses understand how sales perform during the festive season and make data-driven decisions.

# 📂 Dataset
The dataset contains transactional records of Diwali sales, including:

Product_ID – Unique identifier for each product
Orders – Number of orders placed
Category – Product category
Revenue – Total sales revenue generated
Customer_Age, Gender, Location – Customer demographics
# 🛠️ Tech Stack
Python – Data analysis and visualization
Pandas – Data manipulation
Matplotlib & Seaborn – Data visualization
Power BI (optional) – Dashboard creation
# 📊 Key Insights
✔️ Top 10 best-selling products
✔️ Sales trends by category
✔️ Customer demographics analysis
✔️ Revenue distribution across locations

📜 Code Example
python
Copy
Edit
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv("diwali_sales.csv")

# Group and sort top 10 selling products
sales_state = df.groupby(['Product_ID'], as_index=False)['Orders'].sum().sort_values(by='Orders', ascending=False).head(10)

# Plot bar chart
sns.set(rc={'figure.figsize':(20,5)})
sns.barplot(data=sales_state, x='Product_ID', y='Orders', palette='viridis')
plt.xlabel("Product ID")
plt.ylabel("Total Orders")
plt.title("Top 10 Products by Orders")
plt.show()
# 📌 How to Use
1️⃣ Clone the repository
2️⃣ Install dependencies (pip install pandas matplotlib seaborn)
3️⃣ Run the script and analyze results

# 📢 Future Improvements
🔹 Advanced predictive analytics
🔹 Sales forecasting using ML
🔹 Interactive dashboards

