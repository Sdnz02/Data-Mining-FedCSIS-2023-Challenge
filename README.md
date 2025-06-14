# FedCSIS 2023 Challenge: Cybersecurity Threat Detection in the Behavior of IoT Devices

This project was developed for the **FedCSIS 2023 Data Mining Challenge**. The objective is to detect and classify cyberattack events based on system activity logs of IoT devices using machine learning models.

---

## Problem Description

The challenge focuses on analyzing system-level logs of IoT devices to determine whether certain events indicate a cyberattack. Each row in the dataset represents an event and is labeled as either part of an attack (`1`) or benign activity (`0`).

---

## Dataset Structure

The dataset includes **multiple CSV files**. Each file represents system activity logs with features such as:

- `SYSCALL_timestamp`, `SYSCALL_syscall`, `SYSCALL_success`, `SYSCALL_exit`
- `PROCESS_comm`, `PROCESS_exe`, `PROCESS_PATH`
- `CUSTOM_openFiles`, `CUSTOM_libs`, `CUSTOM_openSockets`
- `USER_ACTION_op`, `USER_ACTION_src`, `USER_ACTION_res`
- `attack` (target label)

---

## Preprocessing Steps

1. **Extract CSV files** from archive  
2. **Initial exploration**: file count and sample rows  
3. **Drop single-valued columns**  
4. **Label attack-containing files**  
5. **Label Encoding** for categorical features  
6. **Missing value handling**:
   - Categorical: fill with `'missing'`
   - Numerical: fill with median or `-1`
7. **Merge all CSVs into a single dataset**
8. **Normalization** (min-max scaling [0, 1])
9. **Drop remaining columns with NaNs**

---

## Models Used

After preprocessing, the data was split into `X` and `y`, then into train-test sets with a 20% test split.

Four machine learning models were trained and evaluated:

| Model              | Accuracy | F1 Score | Precision | ROC AUC | Recall  |
|--------------------|----------|----------|-----------|---------|---------|
| **Decision Tree**  | 99.79%   | 98.10%   | 99.05%    | 98.55%  | 97.15%  |
| **Random Forest**  | 99.70%   | 97.31%   | 98.45%    | 98.05%  | 96.19%  |
| **XGBoost**        | 99.52%   | 95.65%   | 98.83%    | 96.30%  | 92.67%  |
| **Logistic Regr.** | 95.96%   | 49.19%   | 85.08%    | 67.11%  | 34.59%  |

---

## Evaluation Summary

- **Decision Tree** and **Random Forest** outperformed other models across all metrics.
- **XGBoost** also performed competitively with high precision and recall.
- **Logistic Regression** lagged behind due to the dataset's non-linear nature.

---

## File Structure

├── Report FedCSIS 2023 Challenge.docx # Detailed report

├── Cybersecurity_Threat_Detection.pptx # Slide presentation

├── Data_Mining_FedCSIS_2023_Challenge.ipynb # Jupyter notebook Python (code)


---

## Team Members

- **Suat Deniz** - 2006102002  
- **Berkay Caplık** - 2206102900  
- **Abdulkadir Dağlar** - 2006102033  

---

## License

This project is licensed under the **MIT License**.


---

## Future Work

- Hyperparameter tuning (e.g., GridSearchCV, Optuna)
- Advanced ensemble methods (Stacking, Voting)
- Feature engineering with domain knowledge
- Cross-domain validation

