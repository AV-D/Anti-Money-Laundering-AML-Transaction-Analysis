## Overview  
This notebook is designed to explore financial transaction data by extracting and merging CSV files from zipped archives. It loads two transaction datasets, performs initial data cleansing, and creates an integrated DataFrame for further analysis. The notebook provides a foundation for tasks such as anomaly detection, risk assessment, and potential money laundering identification.  

## Features  
- **Zip Extraction**: Reads CSV files from given zip archives using Python’s `zipfile` module.  
- **Data Loading**: Utilizes Pandas to load the extracted data into DataFrames.  
- **Data Merging**: Concatenates multiple datasets into one unified DataFrame for comprehensive analysis.  
- **Exploratory Setup**: Provides an initial code framework for further visualization and modeling using `Seaborn`, `Matplotlib`, `scikit-learn`, and `NetworkX`.  
- **Machine Learning Preparation**: Sets up modules for data preprocessing and modeling (including **SMOTE** for imbalanced datasets) to facilitate classification tasks later in the workflow.  

## Dependencies  
Before running the notebook, ensure you have the following Python libraries installed:  

- Python 3.x  
- Pandas  
- Seaborn  
- Matplotlib  
- NetworkX  
- scikit-learn  
- imbalanced-learn  

### Install Required Packages  
Use the following command to install the dependencies:  

```bash
pip install pandas seaborn matplotlib networkx scikit-learn imbalanced-learn
```

## Files and Data  
- `exploration.ipynb` - The main Jupyter Notebook for data extraction, processing, and exploratory analysis.  
- `HI-Small_Trans.csv.zip` - A zip archive containing the **HI** transaction data CSV file.  
- `LI-Small_Trans.csv.zip` - A zip archive containing the **LI** transaction data CSV file.  

Ensure the zip files are available in the same directory as the notebook or provide the appropriate file paths.  

## Usage  
1. **Open the Notebook**  
   - Launch Jupyter Notebook or JupyterLab and open `exploration.ipynb`.  

2. **Run Cells Sequentially**  
   - Import necessary libraries.  
   - Extract and read CSV files from the provided zip archives.  
   - Merge the datasets into a single DataFrame for analysis.  

3. **Explore & Enhance**  
   - Use the resulting DataFrame to perform further data exploration, visualization, and predictive modeling as needed.  

## Next Steps  
This notebook is a starting point for your data exploration workflow. You may extend it by:  

- Cleaning and transforming the data further as part of preprocessing steps.  
- Visualizing transaction trends, anomalies, and network relationships.  
- Applying machine learning techniques (e.g., `RandomForestClassifier` or other models) to detect suspicious transactions.  
- Experimenting with **SMOTE** or other techniques for handling imbalanced datasets in classification tasks.  

## Example Dataset Preview  
The dataset contains columns such as:  

- **Timestamp**: Date and time of the transaction.  
- **From_Bank / To_Bank**: Bank IDs involved in the transaction.  
- **Account / Account.1**: Account IDs of sender and receiver.  
- **Amount_Received / Amount_Paid**: Transaction amounts in respective currencies.  
- **Payment_Format**: Mode of payment (e.g., Cheque, Reinvestment).  
- **Is_Laundering**: Binary flag indicating whether a transaction is suspected of money laundering (`0 = No, 1 = Yes`).  

### Sample Data:  

| Timestamp          | From_Bank | Account     | To_Bank | Account.1  | Amount_Received | Receiving_Currency | Amount_Paid | Payment_Currency | Payment_Format | Is_Laundering |
|--------------------|----------|------------|---------|------------|-----------------|---------------------|-------------|-----------------|---------------|--------------|
| 2022/09/01 00:20  | 10       | 8000EBD30  | 10      | 8000EBD30  | 3697.34         | US Dollar          | 3697.34     | US Dollar       | Reinvestment  | 0            |
| 2022/09/01 00:20  | 3208     | 8000F4580  | 1       | 8000F5340  | 0.01            | US Dollar          | 0.01        | US Dollar       | Cheque        | 0            |

## License  
This project is provided **"as is"** without any warranties. You are free to use and modify the contents of this notebook for educational and research purposes.  

