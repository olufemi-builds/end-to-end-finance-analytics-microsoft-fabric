Microsoft-Fabric-Finance-Analytics-Demo

This repository demonstrates an **end-to-end finance dashboard workflow** using Microsoft Fabric:

- Lakehouse data → Fabric Notebook → PySpark analysis → Visualizations
- Visuals include Revenue by Account, Profit Trend, and Expense Breakdown
- Fully reproducible, auditable, and ready for sharing

## Quick Start

1. Open `notebooks/QuickAnalysis.ipynb` in Fabric Notebook
2. Upload CSVs from the `data/` folder
3. Run the notebook cells to generate visuals
4. Check `images/` folder for example screenshots

## Datasets

- `transactions.csv` – sample transactions
- `accounts.csv` – chart of accounts
- `date_dim.csv` – calendar dimension

## License

This project is licensed under the [MIT License](LICENSE).

## Learn More

- [Microsoft Fabric Overview](https://learn.microsoft.com/en-us/fabric/fundamentals/microsoft-fabric-overview)
