# End-to-End Finance Analytics with Microsoft Fabric

An end-to-end analytics project demonstrating how Microsoft Fabric can transform finance data into business insights using Lakehouse, Spark SQL, PySpark, and Power BI.

Rather than building a standalone dashboard, this project shows how Power BI fits into a complete analytics workflow within Microsoft Fabric.

---

## Overview

This solution demonstrates a modern analytics architecture.

```
Finance Data (CSV)

        │

        ▼

Microsoft Fabric Lakehouse

        │

        ▼

Spark SQL & PySpark

        │

        ▼

Data Transformation

        │

        ▼

Power BI Semantic Model

        │

        ▼

Interactive Reports
```

This repository complements my Medium article:

**Power BI at 11: Eleven Lessons That Changed Modern Analytics**

where Lessons 7 and 8 discuss Microsoft's transition from standalone reporting to a unified analytics platform powered by Microsoft Fabric.

---

## Repository Contents

```
end-to-end-finance-analytics-microsoft-fabric/

├── README.md
├── Transaction.csv
├── Chart of Accounts.csv
├── date_dim.csv
├── Account Name.png
├── Chart.png
├── Profit.png
└── List Tables.png
```

---

## Sample Dataset

Included datasets

- Transaction.csv
- Chart of Accounts.csv
- date_dim.csv

The datasets simulate financial transactions for learning Microsoft Fabric analytics.

---

## Analytics Workflow

1. Import CSV files into Microsoft Fabric.
2. Store data inside a Lakehouse.
3. Query data using Spark SQL.
4. Transform data with PySpark.
5. Prepare reporting datasets.
6. Build interactive Power BI reports.
7. Share insights through Microsoft Fabric.

---

## SQL Example

The project demonstrates Spark SQL queries including joins and aggregations.

Example:

```sql
SELECT
    a.AccountName,
    SUM(
        CASE
            WHEN t.Type='Revenue'
            THEN t.Amount
            ELSE -t.Amount
        END
    ) AS TotalProfit
FROM financedemoworkspace.transactions t
JOIN financedemoworkspace.accounts a
ON t.AccountID = a.AccountID
GROUP BY a.AccountName
ORDER BY TotalProfit DESC;
```

---

## Technologies

- Microsoft Fabric
- Lakehouse
- Spark SQL
- PySpark
- Power BI
- Power Query
- DAX

---

## What You'll Learn

This project demonstrates how to

- Build an end-to-end analytics solution
- Load finance datasets into Microsoft Fabric
- Work with Lakehouse architecture
- Query data using Spark SQL
- Transform data using PySpark
- Prepare reporting datasets
- Build Power BI reports
- Understand how Power BI integrates with Microsoft Fabric

---

## Repository Screenshots

Included screenshots

- List Tables.png
- Account Name.png
- Chart.png
- Profit.png

These screenshots illustrate

- Lakehouse tables
- Spark SQL queries
- PySpark analysis
- Financial reporting

---

## Related Article

Power BI at 11: Eleven Lessons That Changed Modern Analytics

This repository provides a practical implementation of the Microsoft Fabric concepts discussed in Lessons 7 and 8, demonstrating how Power BI works as part of a unified analytics platform.

---

## Future Enhancements

Planned additions

- OneLake Shortcuts
- Direct Lake Semantic Model
- Fabric Data Factory Pipeline
- Dataflows Gen2
- Real-Time Intelligence
- Copilot integration
- CI/CD deployment

---

## Author

Olufemi Olamoyegun

Microsoft Fabric Super User

Business Intelligence & Analytics Professional

GitHub

https://github.com/olufemi-builds

Portfolio

https://olufemiolamoyegun.github.io

---

## License

MIT License
## License

This project is licensed under the [MIT License](LICENSE).

