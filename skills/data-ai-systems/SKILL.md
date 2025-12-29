---
name: data-ai-systems
description: Master data engineering, machine learning, and AI systems including Python data science, ML frameworks, analytics, and MLOps. Use when working with data pipelines, building ML models, or implementing AI solutions.
sasmp_version: "1.3.0"
bonded_agent: 01-frontend-ui-specialist
bond_type: PRIMARY_BOND
---

# Data & AI Systems

## Quick Start

Data science and ML require integrated knowledge across multiple domains:

```python
# Machine Learning Example with Scikit-learn
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, precision_score

# Load and prepare data
X_train, X_test, y_train, y_test = train_test_split(
    features, labels, test_size=0.2, random_state=42
)

# Train model
model = RandomForestClassifier(n_estimators=100, max_depth=10)
model.fit(X_train, y_train)

# Evaluate
predictions = model.predict(X_test)
accuracy = accuracy_score(y_test, predictions)
precision = precision_score(y_test, predictions)
```

## Python Data Science Stack

### Core Libraries

#### NumPy & Pandas
- **NumPy**: Numerical computing, arrays, linear algebra
- **Pandas**: Data manipulation, DataFrames, time series analysis
- **Data Cleaning**: Handling missing values, outliers, data normalization
- **Feature Engineering**: Creating meaningful features from raw data

#### Visualization
- **Matplotlib**: Low-level plotting library
- **Seaborn**: Statistical data visualization
- **Plotly**: Interactive, web-based visualizations
- **Tableau/Power BI**: BI tools for dashboards

### Machine Learning

#### Scikit-learn Framework
- **Supervised Learning**: Regression, classification, ensemble methods
- **Unsupervised Learning**: Clustering, dimensionality reduction
- **Model Selection**: Cross-validation, hyperparameter tuning
- **Pipeline**: Automated ML workflows

#### Deep Learning Frameworks
- **TensorFlow/Keras**: Neural networks, computer vision, NLP
- **PyTorch**: Dynamic computation graphs, research-friendly
- **Transfer Learning**: Pre-trained models (BERT, ResNet, GPT)
- **Fine-tuning**: Adapting models to specific tasks

### Data Engineering

#### ETL Pipelines
- **Extraction**: APIs, databases, files, real-time streams
- **Transformation**: Data cleaning, aggregation, feature engineering
- **Loading**: Data warehouses, data lakes, databases
- **Orchestration**: Airflow, Prefect, Dbt

#### Big Data Tools
- **Apache Spark**: Distributed data processing
- **Hadoop**: Distributed storage and computation
- **Kafka**: Real-time data streaming
- **Apache Hive**: Data warehouse queries

### Statistics & Analytics

#### Statistical Methods
- **Descriptive Statistics**: Mean, median, variance, distribution
- **Hypothesis Testing**: A/B testing, statistical significance
- **Regression Analysis**: Linear, logistic, polynomial regression
- **Time Series**: ARIMA, seasonal decomposition, forecasting

#### Analytics Metrics
- **Business Metrics**: KPIs, conversion rates, retention
- **Model Metrics**: Accuracy, precision, recall, F1, AUC-ROC
- **Causal Inference**: Understanding cause-effect relationships

## Machine Learning Workflow

### Problem Definition
1. **Understand Business Context**: Goals, constraints, success metrics
2. **Define ML Problem**: Classification, regression, clustering
3. **Data Requirements**: Volume, quality, collection strategy

### Data Preparation
1. **Exploratory Data Analysis (EDA)**
   - Distribution analysis
   - Correlation analysis
   - Outlier detection

2. **Preprocessing**
   - Missing value handling
   - Scaling and normalization
   - Encoding categorical variables

### Model Development
1. **Baseline Models**: Simple models for comparison
2. **Feature Engineering**: Creating relevant features
3. **Model Selection**: Trying different algorithms
4. **Hyperparameter Tuning**: Grid search, random search, Bayesian optimization

### Evaluation
1. **Train/Validation/Test Split**: Proper data separation
2. **Cross-validation**: k-fold, stratified cross-validation
3. **Performance Metrics**: Task-specific evaluation criteria
4. **Error Analysis**: Understanding failure modes

### Deployment & Monitoring
1. **Model Serving**: REST APIs, batch predictions
2. **Performance Monitoring**: Tracking metrics in production
3. **Data Drift Detection**: Detecting distribution changes
4. **Retraining**: Automated or scheduled model updates

## MLOps Best Practices

### Model Management
- **Versioning**: Tracking model versions, parameters, performance
- **Reproducibility**: Consistent results with same inputs
- **Documentation**: Model cards, performance reports

### Pipeline Automation
- **CI/CD for ML**: Automated testing, validation, deployment
- **Feature Stores**: Centralized feature management
- **Experiment Tracking**: MLflow, Weights & Biases

### Monitoring & Maintenance
- **Performance Tracking**: Model accuracy over time
- **Data Quality**: Input data validation
- **Alert Systems**: Detecting degradation

## NLP & Computer Vision

### Natural Language Processing
- **Text Preprocessing**: Tokenization, stemming, lemmatization
- **Word Embeddings**: Word2Vec, GloVe, FastText
- **Transformers**: BERT, GPT, attention mechanisms
- **Applications**: Sentiment analysis, NER, machine translation

### Computer Vision
- **Image Preprocessing**: Resizing, normalization, augmentation
- **Convolutional Networks**: CNNs for image classification
- **Object Detection**: YOLO, R-CNN, SSD
- **Segmentation**: Semantic and instance segmentation

## Learning Resources

- AI Engineer Roadmap: https://roadmap.sh/ai-engineer
- Scikit-learn: https://scikit-learn.org
- TensorFlow: https://www.tensorflow.org
- Fast.ai: https://www.fast.ai
- Kaggle Competitions: https://www.kaggle.com
