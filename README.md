Exp 3 :  Working with NumPy Arrays, Pandas DataFrames & Basic Plots using Matplotlib

AIM:
To perform data analysis using NumPy arrays and Pandas DataFrames and visualize the data using basic plots in Matplotlib.

EQUIPMENTS REQUIRED:
Python 3.x
Jupyter Notebook / Google Colab / VS Code
Libraries: numpy, pandas, matplotlib

ALGORITHM:
Import required libraries: NumPy, Pandas, and Matplotlib
Create and manipulate NumPy arrays
Create a Pandas DataFrame from the array
Perform data operations like filtering and summarizing
Visualize the data using basic plots (bar chart, histogram, line plot)

Program:
# Step 1: Import required libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Step 2: Create NumPy arrays
sales_data = np.array([[230, 210, 190], [300, 340, 280], [150, 180, 200]])
months = ['January', 'February', 'March']
products = ['Product_A', 'Product_B', 'Product_C']

# Step 3: Create DataFrame from NumPy array
df = pd.DataFrame(sales_data, columns=products, index=months)
print("Sales Data:\n", df)

# Step 4: Basic statistical summary
print("\nMean Sales per Product:\n", df.mean())
print("\nTotal Sales per Month:\n", df.sum(axis=1))

# Step 5: Data Filtering Example
high_sales = df[df['Product_A'] > 200]
print("\nFiltered Data (Product_A > 200):\n", high_sales)

# Step 6: Visualization - Bar Plot for Sales per Product
df.plot(kind='bar', figsize=(10, 6))
plt.title("Monthly Sales of Products")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.grid(True)
plt.tight_layout()
plt.show()

# Step 7: Line Plot for Product A
df['Product_A'].plot(kind='line', marker='o', color='green', figsize=(8, 5))
plt.title("Product A Sales Over Months")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.grid(True)
plt.tight_layout()
plt.show()

# Step 8: Histogram of all product sales
df.plot(kind='hist', bins=5, alpha=0.7, figsize=(10, 5))
plt.title("Histogram of Sales for All Products")
plt.xlabel("Sales")
plt.grid(True)
plt.tight_layout()
plt.show()


EXPECTED OUTPUT:
A DataFrame displaying sales data for 3 products across 3 months
Summary statistics (mean and total sales)
Filtered records where Product_A sales > 200
Bar chart: Monthly sales for each product
Line plot: Sales trend of Product_A
Histogram: Distribution of all product sales

RESULT:
Successfully created NumPy arrays and converted them into a Pandas DataFrame. Performed basic data analysis and visualized the results using various Matplotlib plots.
