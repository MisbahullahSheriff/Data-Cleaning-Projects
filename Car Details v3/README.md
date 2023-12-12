# Car Details v3 dataset: A Data Cleaning Project

<br>

## Table of Contents:
- [Project Overview](#project-overview)
- [Files](#files)
- [Tools Used](#tools-used)
- [Data Cleaning Steps](#data-cleaning-steps)
- [Results](#results)
- [References](#references)
- [Note](#note)
- [Let's Connect](#lets-connect)

<br>

## Project Overview:
- The main aim of this project is to clean the `Car Details v3` dataset and transform it to a form suitable for further exploratory data analysis for better interpretation or predictive modelling
- This project doesn't involve handling missing values or outliers, those steps are reserved to be done in the exploratory analysis step
- Rather, this project aims at identifying and correcting any invalid values and preparing the dataset for further exploratory analysis
- This project also aims to demonstrate my skills in Data Cleaning using Python and tools like Pandas and Numpy

<br>

## Files:
- `Car Details v3.csv`: contains the entire dataset used in the project
- `data_dictionary.txt`: provides a short description of the features present in the dataset
- `notebook.ipynb`: contains all the code written to implement the project
- `notebook.pdf`: the pdf version of `notebook.ipynb`

<br>

## Tools Used:
- Python
- Pandas
- Numpy
- Google Colab

<br>

## Data Cleaning Steps:
- Analyzed the meta-data about the dataset
- Identified and deleted the duplicate records
- Performed column-wise inspection; identified and treated any inaccuracies and inconsistencies within the data:
  - Converted data types of some features for `optimizing memory utilization`
  - Handled messy and inconsistent values in numeric features and renamed them for better readability
  - Dropped the irrelevant features from the dataset
  - Re-ordered the columns for better readability
- Implemented a function that takes in the raw dataset and returns the cleaned version
- All the data cleaning steps are implemented in `chained` fashion, for better readability and proof of skill

<br>

## Results:
- The cleaned dataset utilizes about 2.25 times less memory compared to the original dataset, thereby optimizing memory utilization
- Some features contain missing values; these could be:
  - dropped altogether; or
  - imputed using appropriate techniques
- Some categorical features contain very rare values (<1% of total observations):
- Overall, a lot of information could be extracted from this dataset and it should be analyzed and studied appropriately using statistics and graphical plots

<br>

## References:
- Converting `mileage` values:
  - 1 km/l = 2.35 mpg [link](https://www.mpgtolitres.com/kml-to-mpg)
  - 1 km/kg = 0.0016 mpg [link](https://math.stackexchange.com/questions/1141752/how-to-convert-kilometers-kilogram-km-kg-to-miles-gallon-mpg)
- Converting `torque` values:
  - 1 kg-m = 9.80665 N-m [link](https://www.convertunits.com/from/kg-m/to/N-m)
 
<br>

## Note:
- Thank you for going through my work 😀
- Hope you found it useful! 💫
- If you have some suggestions to improve this repository/project, please feel free to let me know 👍
- I'm always open to learning what I could've done better! 🚀

<br>

## Let's Connect:
- [LinkedIN](https://www.linkedin.com/in/mohammed-misbahullah-sheriff/)
