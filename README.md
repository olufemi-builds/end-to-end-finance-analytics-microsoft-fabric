# End-to-End Finance Analytics with Microsoft Fabric

An end-to-end analytics project demonstrating how Microsoft Fabric transforms finance data into business insights using Lakehouse, Spark SQL, PySpark, and Power BI.

Rather than building a standalone dashboard, this project illustrates how Power BI fits into a complete analytics workflow within Microsoft Fabric.

---

## Overview

This repository demonstrates a modern Microsoft Fabric analytics architecture.

```text
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

The article explores how Power BI has evolved from a self-service reporting tool into an essential component of Microsoft's unified analytics platform. This repository provides a practical implementation of the Microsoft Fabric concepts discussed in Lessons 7 and 8.

---

## Repository Contents

```text
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

This repository includes sample finance datasets for learning Microsoft Fabric analytics.

- Transaction.csv
- Chart of Accounts.csv
- date_dim.csv

The datasets simulate a finance reporting environment suitable for analytics, reporting, and demonstration purposes.

---

## Analytics Workflow

1. Import finance datasets into Microsoft Fabric.
2. Store data inside a Lakehouse.
3. Explore how finance datasets can be processed using Spark SQL and PySpark within Microsoft Fabric.
4. Prepare reporting-ready datasets.
5. Build interactive Power BI reports.
6. Publish and share insights through Microsoft Fabric.

---

## Example Spark SQL Query

The project demonstrates the type of Spark SQL queries commonly used for financial analysis.

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

This project demonstrates how to:

- Build an end-to-end analytics solution
- Organize finance data within Microsoft Fabric
- Understand Lakehouse architecture
- Explore Spark SQL for analytics
- Understand PySpark data transformations
- Prepare reporting-ready datasets
- Build Power BI reports
- Understand how Power BI integrates with Microsoft Fabric

---

## Repository Screenshots

The repository includes example screenshots showing:

- Account Name.png
- Chart.png
- Profit.png
- List Tables.png

These screenshots illustrate:

- Lakehouse tables
- Financial reporting visuals
- Data exploration
- Analytics outputs

---

## Why This Project

Power BI has evolved beyond standalone reporting. Today it serves as the analytics layer within Microsoft Fabric, connecting data ingestion, engineering, semantic modeling, and business intelligence.

This repository demonstrates that end-to-end approach using a finance analytics scenario and complements the concepts discussed in the accompanying Medium article.

---

## Related Article

This repository accompanies my Medium article celebrating Power BI's 11th anniversary.

**Power BI at 11: Eleven Lessons That Changed Modern Analytics**

Read the article:

https://medium.com/@olamoyegun07/power-bi-at-11-eleven-lessons-that-changed-modern-analytics-30fcd4581428

The article reflects on eleven years of Power BI's evolution, while this repository demonstrates the Microsoft Fabric architecture discussed in Lessons 7 and 8.

---

## Future Enhancements

Planned additions include:

- OneLake Shortcuts
- Direct Lake Semantic Models
- Fabric Data Factory Pipelines
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

https://olufemi-builds.github.io/olufemiolamoyegun.github.io/

---

## Connect

- Portfolio: https://olufemi-builds.github.io/olufemiolamoyegun.github.io/
- GitHub: https://github.com/olufemi-builds
- Medium: https://medium.com/@olamoyegun07
- LinkedIn: https://www.linkedin.com/in/olufemi-olamoyegun/

## License

This project is licensed under the [MIT License](LICENSE).
