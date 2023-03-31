This is my last project from Practicum Program


Its about doing product range analysis at a Ecommerce shop

Its done in Jupyter

Language: Python

Source file: ecommerce_dataset_us.csv



# E-commerce: Analyzing the product range

👉 View the `notebook` **[here](https://nbviewer.org/github/AviVolah/AviVolah/blob/Practicum/Projects/15th%20Project/15th%20Project%20-%20Final%20Clean.ipynb)** using **nbviewer**.


# Product Range Analysis

This project analyzes the product range of an ecommerce store using one year of invoice data to explore buyer habits, create and analyze categories, and explore possible seasonal trends. The project includes a detailed analysis of the research in the `product_range_final.ipynb` notebook.

## Data Description
- `ecommerce_dataset_us.csv`: invoice log
    - InvoiceNo: order identifier
    - StockCode: item identifier
    - Description: item name
    - Quantity: quantity ordered
    - InvoiceDate: order date
    - UnitPrice: price per item
    - CustomerID: customer identifier

### Libraries to run the notebook locally
***Python version 3.8.8***
|Library| Version|
|---|---|
|Pandas | 1.3.5 |
|NumPy | 1.20.1 |
|SciPy | 1.6.2 |
|Sidetable | 0.9.0 |
|InteractiveShell| x |
|reduce | x |
|Matplotlib.pyplot | 3.5.2 |
|stats | x |
|apriori | x |
|association_rules | x |

## Dashboard
The dashboard can be viewed on Tableau Public [here](https://public.tableau.com/app/profile/avi2714/viz/TopItemsByProfit/EcommerceProductRange).


## Summary
### Methodology
- Data cleaning & processing
    - Identified stock code with multiple descriptions and vice versa.
    - Remaining descriptions were cleaned and used to create 1:1 table of stock codes and product names. This table was used to populate the "name" column with clean product names.
    - Removed all irrelevant data from the data frame.
- Invoice analysis
    - Aggregated invoice data to understand which item is most popular in invoices, what is the biggest and smallest purchase, how many quantity are usually present in an invoice, how many unique items are usually present in an invoice.
- Hypothesis testing
    - Checked if longer description affects the item sales

### Conclusions
Based on the data and the analysis i did there are 3 points i arrived at:

- Best remove all the items in the bad_sc list and double down on the top_sc list
- Make reccomendations to buy other cake cases when there is a purchase of a cake case
- There is no significant correlation between the desc length and any sale metric, but the highest is to profit, and from conducting a statistical test, its better to shorten the descriptions
