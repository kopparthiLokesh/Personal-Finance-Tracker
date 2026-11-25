# Personal Finance Tracker | Excel Dashboard

An Excel dashboard that turns a log of income and expense transactions into a clear view of monthly income, expenses, savings, and overall financial performance.

<img width="977" height="607" alt="Screenshot (981)" src="https://github.com/user-attachments/assets/8676511f-879d-40d2-8bdc-5b335ff39bb5" />


## What It Does

- Records **92 income and expense transactions** (January to early September 2022) in an `Inputs` sheet, each with a date, category, description, and amount.
- Summarizes them automatically in a `Dashboard` sheet by **month** and **category**, with year-to-date (YTD) totals.
- Shows **month-over-month (MoM) % growth** for total income, total expenses, and savings.
- Visualizes the **income breakdown** and **expense breakdown** with pie charts.

## How It Works

The `Dashboard` sheet pulls every figure from the `Inputs` sheet with `SUMIFS` formulas, so adding a transaction updates the whole dashboard automatically.

```excel
=SUMIFS(Inputs!$F:$F, Inputs!$C:$C, <month>, Inputs!$D:$D, <category>)
```

- The `Month` column in `Inputs` is derived from each date with `TEXT(date, "MMMM")`.
- Income categories: Base Salary, Bonus, Side Hustle, Investments.
- Expense categories: Rent, Utilities, Transport, Groceries, Leisure, Other.

## Key Figures (YTD)

| Metric | Amount (USD) |
| --- | --- |
| Total income | $44,691 |
| Total expenses | $17,865 |
| Savings | $26,826 |
| Largest income source | Base Salary, $28,000 (62.7% of income) |
| Largest expense | Rent, $8,750 (49.0% of expenses) |

## Notes

- Transactions run from January to early September 2022. August and September are only partly recorded (for example, there is no rent entry for August), so savings for those months are not comparable with earlier months.

## Repository Contents

| File | Description |
| --- | --- |
| `README.md` | Project overview |
| `Dashboard.png` | Screenshot of the dashboard |
| `Personal_Finance_Tracker.xlsx` | Excel workbook with the `Inputs` and `Dashboard` sheets |

## Tools

- Microsoft Excel (SUMIFS, aggregation formulas, charts)

## Author

**Kopparthi Lokesh**
[LinkedIn](https://www.linkedin.com/in/kopparthilokesh/) | [GitHub](https://github.com/kopparthiLokesh)
