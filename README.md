# Customer Shopping Behavior Analysis

**Status:** Python data inspection, cleaning and EDA notebook prepared. SQL analysis and Power BI dashboard are planned, not yet completed.

## Project overview

An independent portfolio project exploring a publicly available customer-shopping dataset. The analysis examines customer demographics, product categories, recorded purchase amounts, subscription status, discounts, review ratings and reported purchase frequency.

### Dataset

- 3,900 records and 18 original columns.
- 37 missing values in `Review Rating`.
- 3,900 unique customer IDs in the supplied file.
- No transaction date field.
- The data is publicly available and intended for educational analysis; it is not a retailer's confidential internal data.

**Original dataset reference:** [Customer Shopping Trends Dataset on Kaggle](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset)

The raw CSV included here was supplied for this project. Please check the dataset page's current licence and attribution requirements before redistributing it publicly. If redistribution is not permitted, remove `data/raw/customer_shopping_behavior.csv` and provide instructions for downloading it from the source instead.

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## Repository structure

```text
customer-shopping-behavior-analysis/
├── data/
│   ├── raw/
│   │   └── customer_shopping_behavior.csv
│   └── cleaned/
│       └── customer_shopping_behavior_cleaned.csv
├── notebooks/
│   └── customer_shopping_behavior_eda.ipynb
├── sql/
├── powerbi/
│   └── screenshots/
├── README.md
└── requirements.txt
```

## Run the Python notebook

1. Clone or download this repository.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Start Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open `notebooks/customer_shopping_behavior_eda.ipynb` and run the cells from top to bottom.

The notebook reads the raw CSV from `data/raw/` and exports the cleaned dataset to `data/cleaned/`.

## Data handling notes

- Column names are standardized to lowercase `snake_case`.
- Leading/trailing spaces in text values are removed.
- Missing review ratings are retained as missing; no ratings are fabricated.
- The notebook checks whether `discount_applied` and `promo_code_used` contain identical values before treating them as separate signals.

## Important interpretation limits

- The file contains one row per customer ID in the supplied version. Do not describe it as a verified multi-order transaction history.
- There is no transaction date, so month-over-month or year-over-year analysis is not possible.
- The sum of `purchase_amount_usd` is the sum of recorded row amounts, not verified company revenue or customer lifetime value.
- Group differences are descriptive and do not establish causation.

## Project roadmap

- [x] Inspect raw dataset and identify missing values and duplicate rows
- [x] Standardize column names and text values
- [x] Prepare Python EDA notebook
- [ ] Complete and review Python EDA interpretations
- [ ] Write SQL business-analysis queries and validate their results
- [ ] Build Power BI dashboard
- [ ] Add genuine dashboard screenshots
- [ ] Finalize project findings and recommendations

## Author

**Vignani Erram**

This is an independent learning and portfolio project. 
