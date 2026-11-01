# Mobile Sales & Revenue Analytics Dashboard

An interactive **Power BI** dashboard that analyses mobile phone sales across brands, countries, payment methods and months. It tracks revenue, units sold, pricing and customer ratings in a single page.

![Mobile Sales & Revenue Analytics Dashboard](images/dashboard.png)

## Key metrics (KPI cards)

| KPI | Value |
|---|---|
| Total Transactions | 500 |
| Units Sold | 5,229 |
| Total Revenue | ~$5M |
| Average Price | $890 |
| Average Customer Rating | 4.02 |

## What the dashboard shows

| Visual | Question it answers |
|---|---|
| Line chart: total revenue by month | How does revenue change through the year? |
| Bar chart: sum of customer rating by brand | Which brands collect the highest customer ratings? |
| Table: brand, sales, price, units, colour | How do individual brands and colours compare? |
| Pie chart: total sales by payment method | How do customers prefer to pay? |
| Bar chart: total sales by country | Which markets sell the most? |
| Colour slicer | Filter the whole page by phone colour |

## Insights from the data

- **Revenue is uneven through the year.** It peaks in March (about $0.51M), dips to its lowest in May (about $0.28M), then recovers in June (about $0.47M).
- **USA is the top market by sales (65),** followed by France (56) and Australia (55).
- **Payment methods are evenly split.** Each method holds roughly 19% to 21% of sales, so no single method dominates.
- **Vivo has the highest total rating score (235),** followed by Motorola (218) and Google (209).

## Data model

Source table: `Sheet1` (500 sales records).

**Columns:** `Sale_ID`, `Brand`, `Model`, `Color`, `Storage`, `Country`, `Payment_Method`, `Price_USD`, `Units_Sold`, `Revenue_USD`, `Customer_Rating`, `Sale_Month`, `Sale_Year`, `Month_Name`, `Month_Number`

**Measures:** `total_sales`, `total revenue`, `unitSold`, `Avg Price`, `Avr-Rating`

## Tools used

- Power BI Desktop (data modelling, DAX measures, visuals, slicers)
- Excel (source data)

## Repository structure

```
mobile-sales-powerbi-dashboard/
├── README.md
├── images/
│   └── dashboard.png      # dashboard screenshot
├── data/                  # source dataset (add your Excel/CSV file here)
├── powerbi/               # Power BI report file (.pbix)
└── .gitignore
```

## How to open the report

1. Download or clone this repository.
2. Open the `.pbix` file in the `powerbi/` folder with Power BI Desktop.
3. If Power BI asks for the data source, point it to the file in `data/`.

## Notes and next steps

- The brand chart uses the **sum** of customer ratings, which favours brands with more sales. An **average rating by brand** would be a fairer comparison.
- Possible additions: year-over-year comparison, a brand slicer, and revenue by storage size.

## Author

**Anuj Kumar** · Aspiring Data / Business Analyst
[LinkedIn](https://www.linkedin.com/in/anuj-kumar-ssm)
