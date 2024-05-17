# **FedCSIS 2023 Challenge: Cybersecurity Threat Detection in IoT Device Logs**

## Overview

  This repository contains the solution for the FedCSIS 2023 Challenge on cybersecurity threat detection in IoT device logs. The challenge involves developing a model to predict if logs from an IoT system indicate a cyberattack. The solution is submitted as part of the competition and evaluated based on the ROC AUC measure.

## Data

  The repository includes the following data files:
  
  •	train_data.zip: Contains 15,027 log files in CSV format for training.
  
  •	test_data.zip: Contains 5,017 log files in CSV format for testing.
  
  •	train_files_containing_attacks.txt: Lists the subset of training files indicating cyberattacks.
  
  •	test_files_ordering_for_submissions.txt: Specifies the order of test files for submission.
  
  •	test_labels.csv: Contains true labels for the test data.

## Contents

  •	data_loading_and_diagnosis.ipynb: Jupyter Notebook providing the code for loading the data, performing basic diagnostics, and preparing the data for modeling.
  
  •	model_development.ipynb: Jupyter Notebook containing the code for developing and evaluating machine learning models for cybersecurity threat detection.
  
  •	submission_preparation.ipynb: Jupyter Notebook guiding the preparation of the final submission file according to the competition requirements.
  
  •	report.pdf: Detailed report describing the approach, methodology, results, and conclusions of the solution.

## Requirements

  •	Python 3.x
  
  •	Libraries: pandas, numpy, zipfile

## Usage

  1.	Clone the repository to your local machine.
     
  2.	Unzip the train_data.zip and test_data.zip files.
     
  3.	Open and run the Jupyter Notebooks in the provided order to analyze the data, develop models, and prepare the submission.
     
  4.	Submit the final prediction file and the report to the FedCSIS 2023 Challenge platform for evaluation.

## Contributors

  •	Suat Deniz
  
  •	Abdulkadir Dağlar
  
  •	Berkay Caplık

## License

  This project is licensed under the MIT License.
