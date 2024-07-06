# Diwali Sales Analysis

## Overview
This project analyzes sales data from a Diwali sales event to identify trends and insights. The analysis is conducted using Python and various data analysis libraries.

## Project Structure
Diwali_Sales_Analysis/
│
├── Diwali Sales Data.csv
├── Diwali_Sales_Analysis.ipynb
├── README.md
└── requirements.txt

markdown
Copy code

## Dataset
The dataset used in this project is a CSV file containing 11,251 entries and 15 columns. It includes information about customer demographics, product details, and sales amounts.

### Columns:
- `User_ID`: Unique identifier for each customer
- `Cust_name`: Name of the customer
- `Product_ID`: Unique identifier for each product
- `Gender`: Gender of the customer
- `Age Group`: Age group of the customer
- `Age`: Age of the customer
- `Marital_Status`: Marital status of the customer (0 for single, 1 for married)
- `State`: State from which the purchase was made
- `Zone`: Geographical zone of the state
- `Occupation`: Occupation of the customer
- `Product_Category`: Category of the product purchased
- `Orders`: Number of orders placed
- `Amount`: Total amount spent
- `Status`: Status of the transaction (not used in analysis)
- `unnamed1`: Unused column

## Libraries Used
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

## Installation
To run this project, you'll need to have Python installed along with the required libraries. You can install the required libraries using the following command:

```bash
pip install -r requirements.txt
Usage
Clone this repository.
Ensure you have the necessary libraries installed.
Open and run the Jupyter Notebook (Diwali_Sales_Analysis.ipynb) to see the analysis.
Analysis Steps
Data Import: Load the dataset using pandas.
Data Inspection: Examine the structure and contents of the data.
python
Copy code
df.shape
df.head()
df.info()
Data Cleaning: Handle missing values and irrelevant columns.
python
Copy code
df.drop(['Status', 'unnamed1'], axis=1, inplace=True)
df.dropna(inplace=True)
Data Visualization: Use matplotlib and seaborn to visualize sales trends, customer demographics, and product preferences.
python
Copy code
plt.figure(figsize=(10,6))
sns.countplot(x='Gender', data=df)
plt.title('Gender Distribution')
plt.show()
Conclusion
This analysis helps in understanding the purchasing behavior during the Diwali sales event, identifying key demographics, and popular product categories. Such insights can inform marketing strategies and inventory management for future sales events.
