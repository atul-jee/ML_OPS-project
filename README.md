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
