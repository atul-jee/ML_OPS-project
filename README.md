# MLOps Spam Detection Project

This repository contains a machine learning project for detecting spam messages using MLOps best practices. The project leverages tools such as DVC for experiment tracking and reproducibility.

## Project Structure

```
mlops-spam/
├── data/                # Raw and processed data
├── dvclive/             # DVC Live metrics and plots
│   └── plots/
│       └── metrics/
│           └── precision.tsv
├── models/              # Saved models
├── src/                 # Source code for training and evaluation
├── .dvc/                # DVC configuration files
├── .gitignore
├── dvc.yaml             # DVC pipeline configuration
├── requirements.txt     # Python dependencies
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.7+
- [DVC](https://dvc.org/doc/install)
- [Git](https://git-scm.com/)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/atul-jee/ML_OPS-project
    cd mlops-spam
    ```

2. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

3. Pull data and models using DVC:
    ```sh
    dvc pull
    ```

### Running the Pipeline

To run the full pipeline and reproduce results:
```sh
dvc repro
```

### Tracking Metrics

Metrics such as precision are tracked using DVC Live and can be found in `dvclive/plots/metrics/`.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT
## Jupyter Notebook Overview

The `mynotebook.ipynb` notebook demonstrates a full machine learning workflow for spam detection using NLP techniques. The steps include:

- **Data Loading & Cleaning:** Loads the SMS spam dataset, removes unnecessary columns, renames columns, encodes target labels, and removes duplicates.
- **Feature Engineering:** Applies text preprocessing (lowercasing, tokenization, stopword removal, stemming) to prepare messages for modeling.
- **Vectorization:** Converts processed text into numerical features using TF-IDF vectorization.
- **Train-Test Split:** Splits the data into training and testing sets.
- **Model Training:** Trains multiple classifiers (SVM, KNN, Naive Bayes, Decision Tree, Logistic Regression, Random Forest, AdaBoost, Bagging, Extra Trees, Gradient Boosting, XGBoost).
- **Model Evaluation:** Evaluates each model’s accuracy and precision on the test set and prints the results for comparison.

This notebook provides a clear, reproducible pipeline for comparing various machine learning models on
