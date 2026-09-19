# E-commerce Product Data Extraction & Processing Using REST API

## Project Overview

This project demonstrates how to extract e-commerce product data from a REST API, process and clean the JSON response using Python and Pandas, validate the dataset, create derived fields, and export the final dataset as a CSV file ready for data analysis.

## Workflow

REST API → Data Extraction → JSON → Pandas → Data Cleaning & Processing → Data Validation → Feature Engineering → CSV → Analysis-Ready Dataset

## Objectives

- Connect to a REST API and retrieve product data using HTTP GET requests.
- Process JSON API responses using Python and Pandas.
- Profile and inspect the extracted dataset.
- Select relevant fields for analysis.
- Handle missing values and check duplicate records.
- Validate important business fields such as price, stock, discount, rating, and minimum order quantity.
- Create derived fields for downstream analysis.
- Export the processed dataset to CSV format.

## Technologies Used

- Python
- Requests
- Pandas
- REST API
- JSON
- CSV

## Data Source

The project uses the DummyJSON Products REST API to retrieve e-commerce product information.

## Data Processing

The extracted API data contains product-level information such as:

- Product ID
- Product Title
- Category
- Price
- Discount Percentage
- Rating
- Stock
- Brand
- SKU
- Weight
- Availability Status
- Return Policy
- Minimum Order Quantity

### Data Cleaning & Validation

The following checks were performed:

- Missing value handling for the `brand` field
- Duplicate Product ID check
- Duplicate SKU check
- Negative price validation
- Negative stock validation
- Discount percentage validation
- Rating validation
- Minimum order quantity validation

### Feature Engineering

The following derived fields were created:

- `Discount_Amount`
- `Discounted_Price`
- `Inventory_Value`
- `Discounted_Inventory_Value`
- `Discount_Band`
- `Stock_Status`

## Output

The processed dataset is exported as:

`ecommerce_products_cleaned.csv`

The final CSV contains **194 products and 19 columns** and is structured as an analysis-ready dataset that can be used for further analysis in Python, SQL, Excel, or Power BI.

## Project Structure

```text
Ecommerce_Product_Data_Extraction_API/
│
├── Ecommerce_Product_Data_Extraction_API.ipynb
├── ecommerce_products_cleaned.csv
└── README.md
