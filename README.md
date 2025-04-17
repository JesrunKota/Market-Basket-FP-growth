## 🛒 Market Basket Analysis Using FP-Growth
This project analyzes a retail transaction dataset to identify customer trends, purchasing behavior, and product affinities. Using data transformation, time-based insights, and the FP-Growth algorithm, we uncover actionable market basket rules and business strategies.

## 📌 Project Goals
Clean and transform real-world transactional data

Perform time, country, and product-based sales analysis

Segment customers by behavior

Identify key product associations using FP-Growth

## Project Structure
```
Market-Basket-Analysis/
├── notebooks/
│   └── Market Basket Analysis Jes.ipynb
├── data/
│   └── Assignment-1_Data.csv
├── images/
│   └── *.png (all exported visualizations)
├── requirements.txt
├── LICENSE
└── README.md
```

## 📊 1. Data Cleaning & Transformation
Q: How was the dataset prepared for analysis?


Fixed column names and converted date/time formats

Transformed price strings (comma to float)

Filled missing CustomerID as "Guest"

Removed zero/negative values and extreme outliers in Quantity and Price

Created a Year/Month column for trend analysis

## 📈 2. Time-Based Sales Analysis
Q: When are sales the highest?

![](images/Monthly Quality Trend.png)

Sales peak in November 2011, indicating holiday-driven purchasing

Drop in December likely reflects fewer transaction days (year-end)

![](images/Monthly Revenue Trend.png)

Revenue follows a similar upward trend

Indicates stable pricing: growth is volume-driven, not due to price increases

## 🌍 3. Country-Based Analysis
Q: Where do most sales occur?

![](images/Top 10 Countries by quantity.png)

United Kingdom dominates with over 90% of total quantity sold

International opportunities exist but are limited in current data

## 🛍️ 4. Product-Based Analysis
Q: What products contribute the most to revenue?

![](images/Top 10 Best Selling Products.png)

Top products are gift bags, lunch bags, and decorative items

“JUMBO BAG RED RETROSPOT” is the best-selling product by far

## 👥 5. Customer Behavior
Q: How loyal are customers?

![](images/Repeated Customers.png)

98.2% of transactions are from “repeat” customers
⚠️ However, many of these may have only 2–3 total purchases

![](images/Distribution of Customer Purchase Frequency.png)

Distribution is right-skewed: most customers purchase only once or twice
💡 Opportunity to re-engage one-time buyers

## 💳 6. High-Spending Customers
Q: Who brings in the most revenue?

![](images/Top 10 customers by Total Spend.png)

Guest users lead in total spend

Top customer IDs suggest repeat business from a few high-value accounts

## 🤝 7. Market Basket Analysis (FP-Growth)
Q: What items are often bought together?

![](images/Association Rule Mining.png)

FP-Growth revealed strong rules with:

High confidence

High lift

Low support → rare but powerful combinations

Ideal for cross-selling at checkout

🧠 Example Rule:
Customers who buy "SET/6 RED SPOTTY PAPER PLATES" often also buy "SET/20 RED RETROSPOT NAPKINS"
Confidence: 81% | Lift: 3.12

---

## 📄 License

This project is licensed under the [MIT License](LICENSE.txt).  
You are free to use, modify, and share this project with attribution.


