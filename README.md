# Traffic IQ

An advanced machine learning pipeline optimized for maximum accuracy in multi-class classification tasks, featuring automated preprocessing, parallel processing, and ensemble modeling.

## 🚀 Features

- Advanced preprocessing with automated handling of missing values
- Parallel feature engineering with outlier detection
- Automated feature selection and polynomial feature creation
- Cross-validated model training with RandomForest
- Ensemble creation with voting classifier
- Progress tracking and checkpointing
- Memory-efficient processing of large datasets
- Comprehensive visualization and evaluation metrics

## 📋 Requirements

```bash
numpy>=1.21.0
pandas>=1.3.0
scikit-learn>=1.0.0
seaborn>=0.11.0
matplotlib>=3.4.0
joblib>=1.1.0
tqdm>=4.62.0
psutil>=5.8.0
```

## Project Description

A high-performance machine learning pipeline designed for multi-class classification tasks with an emphasis on maximum accuracy. This project implements an advanced, automated pipeline that handles the complete ML workflow from data preprocessing to model evaluation, utilizing parallel processing and ensemble methods.

## Key Features
- **Automated Preprocessing:** Handles missing values, categorical features, and outliers
- **Advanced Feature Engineering:** Creates polynomial features and statistical aggregations using parallel processing
- **Intelligent Model Selection:** Uses cross-validation and hyperparameter tuning
- **Memory-Efficient Processing:** Optimized for large datasets with checkpoint saving
- **Ensemble Learning:** Combines multiple models for improved accuracy
- **Progress Tracking:** Real-time monitoring with detailed logging and visualizations

## Technical Details
- **Language:** Python 3.x
- **Core Libraries:** scikit-learn, pandas, numpy
- **Processing:** Parallel computation support with joblib
- **Scalability:** Tested with 148K+ samples and 493 features
- **Model Type:** Ensemble (Random Forest + HistGradientBoosting)

## Use Case
Ideal for data scientists and ML engineers working on:
- Large-scale classification problems
- Multi-class prediction tasks
- Projects requiring high accuracy
- Automated ML pipelines
- Production-ready model development

This pipeline emphasizes both accuracy and efficiency, making it suitable for both research and production environments.

## Dataset

The dataset (`combined_data.zip`) is provided in the `data` directory. See `data/README.md` for detailed information.

- Total samples: 148,088
- Features: 24
- Classes: 14
- After preprocessing: 89,014 unique samples

## 💻 Installation

```bash
# Clone the repository
git clone https://github.com/Navya12341/Traffic-IQ

# Install required packages
pip install -r requirements.txt
```

## 🔧 Usage

```python
from model_training2 import MaxAccuracyPipeline

# Initialize and run pipeline
pipeline = MaxAccuracyPipeline("your_data.csv")
model, accuracy = pipeline.run_max_accuracy_pipeline()
```

For running with sleep prevention on Mac:
```bash
caffeinate -i python model_training2.py > training_log.txt 2>&1
```

## 📊 Pipeline Stages

1. **Preprocessing**
   - Automatic detection and handling of categorical/numerical features
   - Missing value imputation using KNN
   - Duplicate removal
   - Label encoding

2. **Feature Engineering**
   - Parallel processing for feature calculations
   - Outlier detection and handling
   - Polynomial feature creation
   - Statistical feature generation

3. **Model Training**
   - Stratified cross-validation
   - Hyperparameter optimization
   - Model fine-tuning
   - Ensemble creation

4. **Evaluation**
   - Confusion matrix visualization
   - Feature importance analysis
   - Comprehensive performance metrics

## 📈 Performance

- Handles large datasets (tested with 148K+ samples)
- Utilizes parallel processing for speed
- Implements memory-efficient operations
- Achieves improved accuracy through ensemble methods

## 🔍 Model Parameters

The pipeline automatically selects optimal parameters from:
- n_estimators: [200, 500]
- max_depth: [15, None]
- min_samples_split: [5]
- min_samples_leaf: [2]
- class_weight: ['balanced']

## 📝 License

MIT License

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## ✨ Acknowledgments

- Inspired by scikit-learn best practices
- Optimized for multi-class classification tasks
- Designed for maximum accuracy with reasonable computation time

