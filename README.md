# Zepto Data Analysis Project

A SQL-based data analysis project exploring Zepto's e-commerce/grocery product inventory data. This project covers data cleaning, exploratory data analysis (EDA), and business-driven SQL queries to uncover insights around pricing, discounts, stock availability, and revenue.

## 📊 Dataset

The dataset (`zepto_v2.csv`) contains SKU-level product listing data, including:

| Column | Description |
|---|---|
| `category` | Product category (e.g., Snacks, Beverages) |
| `name` | Product name |
| `mrp` | Maximum Retail Price |
| `discountPercent` | Discount applied, in % |
| `discountedSellingPrice` | Selling price after discount |
| `availableQuantity` | Units available |
| `outOfStock` | Stock status flag |
| `weightInGms` | Product weight in grams |
| `quantity` | Quantity per unit/pack |

## 🔧 What's in `data_analysis.sql`

- **Data cleaning**: handling null/zero values, converting prices from paise to rupees, removing invalid entries
- **Exploratory analysis**: row counts, distinct categories, in-stock vs. out-of-stock breakdowns
- **Business insights**:
  - Most discounted products
  - Category-wise average discount
  - High-MRP products currently out of stock
  - Estimated revenue per category
  - Price-per-gram value comparison across products

## 🛠️ Tools Used

- SQL (MySQL / PostgreSQL — *update to match what you actually used*)

## 🚀 How to Run

1. Import `zepto_v2.csv` into your SQL database
2. Run the queries in `data_analysis.sql` to reproduce the cleaning steps and analysis

## 📌 Key Insights

*(Add 2–3 bullet points here summarizing your most interesting findings — e.g., top-performing category by revenue, average discount trends, etc.)*
