# Zepto Data Analysis Project

A SQL-based data analysis project exploring Zepto's grocery/e-commerce product inventory data. The project covers schema setup, data exploration, data cleaning, and business-driven SQL queries to uncover insights around pricing, discounts, stock availability, and revenue.

## 📊 Dataset

`zepto_v2.csv` contains SKU-level product listing data, loaded into a `zepto` table with the following schema:

| Column | Type | Description |
|---|---|---|
| `sku_id` | SERIAL (PK) | Unique identifier per SKU |
| `category` | VARCHAR(120) | Product category |
| `name` | VARCHAR(150) | Product name |
| `mrp` | NUMERIC(8,2) | Maximum Retail Price |
| `discountPercent` | NUMERIC(5,2) | Discount applied, in % |
| `discountedSellingPrice` | NUMERIC(8,2) | Selling price after discount |
| `availableQuantity` | INTEGER | Units available |
| `weightInGms` | INTEGER | Product weight in grams |
| `outOfStock` | BOOLEAN | Stock status flag |
| `quantity` | INTEGER | Quantity per unit/pack |

## 🔧 What `data_analysis.sql` Does

**1. Schema setup** — drops and recreates the `zepto` table.

**2. Data exploration**
- Row count and sample preview
- Null value checks across all columns
- Distinct product categories
- In-stock vs. out-of-stock breakdown
- Products appearing under multiple SKUs

**3. Data cleaning**
- Removes rows where `mrp = 0` (invalid entries)
- Converts `mrp` and `discountedSellingPrice` from paise to rupees

**4. Business analysis** — answers 8 key questions:
1. Top 10 best-value products by discount percentage
2. High-MRP (>₹300) products that are out of stock
3. Estimated revenue per category
4. Products with MRP > ₹500 and discount < 10%
5. Top 5 categories by average discount percentage
6. Price-per-gram for products ≥100g, ranked by value
7. Weight-based categorization (Low / Medium / Bulk)
8. Total inventory weight per category

## 🛠️ Tools Used

- PostgreSQL

## 🚀 How to Run

1. Create a PostgreSQL database
2. Import `zepto_v2.csv` into a table matching the schema above (or let the script's `CREATE TABLE` statement set it up, then load the CSV via your client's import tool)
3. Run `data_analysis.sql` top to bottom — it will clean the data and then run through all 8 analysis queries

