# Stack Overflow Developer Survey dataset: A Data Cleaning Project

## Table of Contents:
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Files](#files)
- [Tools Used](#tools-used)
- [Project Workflow](#project-workflow)
- [Results](#results)
- [Note](#note)
- [Let's Connect](#lets-connect)

## Project Overview:
- The main aim of this project is to clean the `Stack Overflow Developer Survey` dataset and transform it to a form suitable for further exploratory data analysis for better interpretation or predictive modelling
- Data Cleaning is an essential crucial step in any Data Science and Analytics project which is usually carried out right after getting the dataset from an appropriate source
- To be able to derive meaningful insights from the data and to build reliable predictive models, we must inspect the data thoroughly and identify and handle any errors or inconsistencies present
- The purpose of this project is to demonstrate my skills in working on and cleaning large real-world datasets

## Dataset:
- [Data Source](https://insights.stackoverflow.com/survey)
- The data is compiled in 2 csv files:
  - `survey_results_public.csv`: the survey results dataset
  - `survey_results_schema.csv`: description about the columns
- This dataset comprises the results of the survey conducted by Stack Overflow in the year 2022
- The dataset consists of over 73,000 observations and 79 features
- The dataset contains several nested columns, missing values, inaccurate and inconsistent values that require thorough inspection for identification
- This dataset was particularly chosen for this project due to its complexity and to demonstrate my proficiency in cleaning real-world datasets

## Files:
- `data_cleaning_notebook.ipynb`: contains all the code written to inspect and clean the dataset

## Tools Used:
- Python
- Pandas
- Numpy
- Jupyter

## Project Workflow:
- Firstly, I gathered the dataset from `survey_results_public` and observed some meta-data to learn more about the dataset in hand
- Extracted the relevant info from `survey_results_schema` compiled a `Data Dictionary` dataframe, which states the column name and its description for all the columns
  - `survey_results_schema` was missing info for a few columns
- Inspected the dataset for any duplicate values and missing values
- Wrote some convenience functions to streamline the inspection and cleaning processes of the dataset:
  - `col_value_counts`: this function will return the count and percentage of occurance of each unique category of categorical columns in the dataset as a dataframe
  - `col_memory_usage`: this function will return the memory utilized by a given dataset in bytes
  - `col_strip_nested`: this function will return a dictionary of all the unique values along with its count in the nested columns
  - `col_description`: this function will return the description of the column based from the data dictionary dataframe `dictionary`
- Performed a column-wise inspection on all the 79 columns in the dataset
  - The convenience functions provided a lot of crucial info. and helped process and understand the dataset quickly
  - Many columns consisted of nested entries and inconsistent and erranous values
- Implemented a function `clean_data`, which takes in the raw data and returns the cleaned version
  - Some irrelevant columns were dropped
    - The columns `VCHostingPersonal use` and `VCHostingProfessional use` were dropped because they had 0 non-null values
  - All the column names were converted to lower case and renamed to appropriate titles for better readability
  - Most of the categorical features required:
    - Renaming the values to shorter and meaningful values
    - Cleaning up special characters and punctuation marks from the values
    - Converting data type to the Pandas `category` type for optimizing memory usage
  - The `clean_data` function contains all the cleaning steps in a `chain` manner
- Performed data validation to confirm there're no invalid entries in the dataset based on a few columns:
  - Checked if the values in `coding_pro_years` are not greater than those of `coding_years` as it would be incorrect
    - Implemented a function `validate_coding_years` to handle this check
  - Checked if the observations missing values in `country` also had missing values in `currency`
  - All the invalid observations were dropped from the dataset
- Finally the cleaned dataset,  `df_cleaned`, was obtained by passing the original dataset `df` through the functions `clean_data` and `validate_coding_years` sequentially
- Additionally, I also implemented a couple of convenience functions to aid in the feature engineering step, which could used in the modelling step of a predcitive modelling project
  - `get_top_categories`: this function returns the most common values within a nested column
  - `clean_nested_column`: this function performs 3 optional operations and returns the dataset with the new features
    - It can flatten the nested entries based on user-provided values
    - It can calculate the total no. of values within the nested entries
    - It can create binary indicator features based on the presence of most common values within the nested entries
    - A working example of this function is demonstrated at the end of the notebook
    - Read the function docstring for more info.
  - This step was done to extract meaningful features from the nested columns present in the dataset

## Results:
- The cleaned dataset utilizes about 2 times less memory compared to the original dataset, thereby optimizing memory utilization
- The cleaned dataset contains 76 columns (after dropping 3 irrelevant features)
- The cleaned dataset now contains columns with the following data types:
  - `float`: 5
  - `object`: 33
  - `category`: 38
- The working of the `clean_nested_column` function is demonstrated at the end for a taste of feature engineering

## Note:
- Thank you for going through my work 😀
- Hope you found it useful! 💫
- If you have some suggestions to improve this repository/project, please feel free to let me know 👍
- I'm always open to learning what I could've done better! 🚀

## Let's Connect:
- [LinkedIN](https://www.linkedin.com/in/mohammed-misbahullah-sheriff/)
