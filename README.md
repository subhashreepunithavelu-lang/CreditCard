# Credit Card Default Prediction (UCI Dataset)

## About
This project analyses the **Default of Credit Card Clients** dataset using Python in a Jupyter Notebook. The goal is to understand which customer details and payment behaviours are linked to a customer failing to pay their credit card bill next month (default), and to build a model that predicts it.

## Dataset
- **File:** `default_of_credit_card_clients.xls`
- **Source:** UCI Machine Learning Repository (Default of Credit Card Clients)
- **Records:** 30,000 customers
- **Features:** 23 input columns plus 1 target column
- **Period:** Credit card data from Taiwan, April to September 2005
- **Missing values:** None
- **Class balance:** about 78% non-default and 22% default (imbalanced)

### Columns
| Column | Description |
|---|---|
| `ID` | Customer ID |
| `LIMIT_BAL` | Credit limit given (NT dollars), including family credit |
| `SEX` | 1 = male, 2 = female |
| `EDUCATION` | 1 = graduate school, 2 = university, 3 = high school, 4 = others |
| `MARRIAGE` | 1 = married, 2 = single, 3 = others |
| `AGE` | Age in years (21 to 79) |
| `PAY_0`, `PAY_2` to `PAY_6` | Repayment status from September (`PAY_0`) back to April (`PAY_6`). -1 = paid on time, 1 = payment delayed 1 month, 2 = delayed 2 months, and so on up to 9 |
| `BILL_AMT1` to `BILL_AMT6` | Bill statement amount from September back to April (NT dollars) |
| `PAY_AMT1` to `PAY_AMT6` | Amount paid in September back to April (NT dollars) |
| `default payment next month` | **Target:** 1 = default, 0 = no default |

### Data notes
- The Excel file has a header row (`X1`, `X2`, ...) above the real column names, so load it with `header=1`.
- `EDUCATION` contains values 0, 5 and 6 and `MARRIAGE` contains 0, which are not in the official description. Group them into "others" during cleaning.
- `PAY_0` is the September status and there is no `PAY_1` column.
- The target is imbalanced, so use accuracy together with precision, recall, F1 and ROC-AUC.

## Notebook
- **File:** `CreditCard.ipynb` (replace with your notebook's name)
- **What it does:**
  - Loads the Excel file and cleans the data
  - Explores default rate by age, education, marriage and credit limit
  - Studies the effect of repayment history on default
  - Trains and evaluates classification models to predict default

## How to Run
1. Download or clone this repository
   ```
   git clone https://github.com/subhashreepunithavelu-lang/<your-repo-name>.git
   ```
2. Install the required libraries
   ```
   pip install pandas numpy matplotlib seaborn scikit-learn xlrd jupyter
   ```
3. Open the notebook in Jupyter Notebook or Google Colab
4. Load the data using:
   ```python
   import pandas as pd
   df = pd.read_excel("default_of_credit_card_clients.xls", header=1)
   ```
5. Run all cells

## Tools Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

## Author
**Subhashree**
MOP Vaishnav College

## Acknowledgement
Dataset: I-Cheng Yeh and Che-hui Lien, *Default of Credit Card Clients*, UCI Machine Learning Repository.
