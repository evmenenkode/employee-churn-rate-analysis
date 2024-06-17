# Employee Churn Prediction Project

This project aims to predict whether employees under a pilot program will leave the company or not, based on historical employee data. The project utilizes Google Cloud Platform (GCP) services, including BigQuery as a data warehouse, Google Colab for data processing and model building, and Looker Studio for data visualization.

## Data Sources

The project uses two data sources:

1. tbl_hr_data: Contains historical data about employees.
2. tbl_new_employees: Contains data about employees currently working at the company and under the pilot program.
   
## Project Workflow

- Data Ingestion: The data from tbl_hr_data and tbl_new_employees is uploaded to BigQuery as a data warehouse.
- Data Preparation: A view is created by joining the two tables to get a full table view for all employees. Google Colab is connected to BigQuery, and data cleaning and transformation are performed.
- Model Building: A machine learning model is built using the historical employee data (tbl_hr_data) to predict whether employees under the pilot program will leave the company or not. Different models are tested using the PyCaret library, and the Random Forest model is chosen for training.
- Model Training and Prediction: The Random Forest model is trained on the historical data, and predictions are made for the employees under the pilot program (tbl_new_employees).
- Data Loading: The prediction results are loaded back into BigQuery.
- Data Visualization: The prediction data is connected to Looker Studio, and visualizations are created to analyze the results.

## Repository Structure

- colab_notebook.ipynb: Google Colab notebook containing the code for data processing, model building, and prediction.
- README.md: This file, providing an overview of the project.

## Dependencies
- Google Cloud Platform (GCP) account
- BigQuery
- Google Colab
- PyCaret
- Looker Studio

## Usage

1. Set up a GCP account and enable the required services (BigQuery, Colab, Looker Studio).
2. Upload the data files (tbl_hr_data and tbl_new_employees) to BigQuery.
3. Open the colab_notebook.ipynb file in Google Colab and run the code cells to perform data processing, model building, and prediction.
4. Connect the prediction data in BigQuery to Looker Studio and create visualizations to analyze the results.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
