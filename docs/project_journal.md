# Dataset Overview

How many rows? - 9,994 data rows (plus 1 header row, making 9,995 rows in Excel)
How many columns? - 21
What is each row?
    One row represents a single line item within a customer's order. An order can contain multiple products, so the same Order ID may appear in multiple rows if multiple products were purchased.

=================================================================================================
| Column         | Meaning                                                                      |
| -------------- | ---------------------------------------------------------------------------- |
| Order ID       | Unique identifier for an order                                               |
| Order Date     | Date the order was placed                                                    |
| Ship Date      | Date the order was shipped                                                   |
| Ship Mode      | Shipping method used for the order                                           |
| Customer ID    | Unique identifier for a customer                                             |
| Customer Name  | Name of the customer                                                         |
| Segment        | Customer market segment (Consumer, Corporate, or Home Office)                |
| Country/Region | Country where the order was placed (all entries are United States)           |
| City           | City where the order was delivered                                           |
| State          | U.S. state where the order was delivered                                     |
| Postal Code    | ZIP/postal code of the delivery location                                     |
| Region         | Geographic sales region (East, West, South, Central)                         |
| Product ID     | Unique identifier for a product                                              |
| Category       | Main product category (e.g., Furniture, Technology, Office Supplies)         |
| Sub-Category   | More specific product category within a category                             |
| Product Name   | Name of the product sold                                                     |
| Sales          | Revenue generated from the sale before considering profit                    |
| Quantity       | Number of units sold                                                         |
| Discount       | Discount applied to the product (expressed as a decimal, e.g., 0.20 = 20%)   |
| Profit         | Profit earned from the sale (can be negative if the sale resulted in a loss) |
=================================================================================================

- Order ID is not unique because one order can contain multiple products.
- Product ID will appear multiple times because the same product is sold to many customers.
- Customer ID repeats because customers place multiple orders over time.
- Country/Region contains only United States, so it probably won't be useful for analysis.
- Discount is stored as a decimal (for example, 0.20 means a 20% discount).
- Profit can be negative, meaning the company lost money on that sale.

# Data Types
Order ID - Int
Order Date - Date
Ship Date - Date
Ship Mode - Text
Customer ID - Int
Customer Name - Text
Segment - Text
Country/Region - Text
City - Text
State - Text
Postal Code - Int
Region - Text
Product ID - Int
Category - Text
Sub-Category - Text
Product Name - Text
Sales - Int
Quantity - Int
Discount - Decimal
Profit - Int

## Data Quality Assessment

### Missing Values

- Postal Code contains 11 missing values.

### Duplicate Rows

- No obvious duplicate records found.

### Data Types

- Sales and Profit are decimal values.
- Quantity is an integer.
- Dates are stored correctly.

### Interesting Observations

- Some orders resulted in negative profit.
- Discounts range from 0% to 80%.
- The dataset spans four years.