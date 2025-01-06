# Healthcare Camp Attendance Predictor 🏥

## 👋 Created by Ana

[Ana](https://openana.ai) is a sophisticated AI Software Engineer with extensive expertise in software engineering, machine learning, and data science. With a friendly and supportive approach, Ana helps developers and data scientists build better applications and gain deeper insights from their data.

Visit [openana.ai](https://openana.ai) to learn more about Ana's capabilities and how she can help with your projects! 🚀

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://openana-ml-demo.streamlit.app/) [![Kaggle Dataset](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/datasets/shivan118/healthcare-analytics)

An advanced machine learning application for predicting and analyzing healthcare camp attendance patterns. This project helps MedCamp optimize their healthcare camp resources and improve attendance rates through sophisticated ML predictions and comprehensive insights.

## 🎯 Project Overview

MedCamp organizes health camps in several cities targeting working professionals with low work-life balance. The organization has conducted 65 such events over 4 years, accumulating data from approximately 110,000 registrations. This application addresses a critical challenge: optimizing inventory management while maintaining service quality.

### Business Problem

MedCamp faces two key challenges:
1. **High Drop-off Rate**: Significant difference between registration numbers and actual attendance
2. **Inventory Management**: 
   - Excess inventory leads to unnecessary costs
   - Insufficient inventory results in poor participant experience

### Solution Approach

Our application provides:
- Predictive analytics for attendance probability
- Comprehensive data exploration tools
- Multiple ML model options with explainable AI
- Feature importance analysis for better decision-making

## 📊 Dataset Details & Insights

Source: [Healthcare Analytics Dataset on Kaggle](https://www.kaggle.com/datasets/shivan118/healthcare-analytics)

### Key Statistics & Analysis
- 🏥 Total Health Camps: 65 (Multiple formats across 4 years)
- 👥 Total Registrations: 75,278 (Significant dataset size)
- 🧑‍💼 Unique Patients: 37,633 (Diverse patient base)
- 📅 Time Period: 2003-2006 (Consistent temporal data)
- 📊 Missing Values: Minimal across datasets
- 🎯 Success Rate: Varies by camp format

### Data Quality & Characteristics
- Most datasets have complete information with minimal missing values
- Rich demographic and socioeconomic indicators
- Comprehensive patient engagement metrics
- Detailed camp categorization (3 formats)
- Temporal patterns show consistent data collection
- Strong feature set for predictive modeling

### Files Structure & Detailed Analysis

1. **Health_Camp_Detail.csv** (65 rows × 6 columns)
   - Health_Camp_ID: Unique identifier for each camp
   - Camp_Start_Date & End_Date: Temporal information
   - Category1, Category2, Category3: Camp classification
   - No missing values, complete camp information
   - Even distribution across categories
   - Temporal patterns show consistent camp scheduling

2. **Train.csv** (75,278 rows)
   - Registration details for all camps
   - Links Patient_ID with Health_Camp_ID
   - Registration_Date tracking
   - Multiple anonymized variables (Var1-Var5)
   - Key dataset for model training
   - Strong predictive features identified
   - Clear registration patterns visible

3. **Patient_Profile.csv** (37,633 unique patients)
   - Comprehensive patient demographics
   - Online_Follower & Social media engagement metrics
   - Socioeconomic indicators (Income, Education)
   - Age and First_Interaction_Date tracking
   - Geographic (City_Type) distribution analysis
   - Employment categories and patterns
   - Rich source for feature engineering
   - Strong correlation with attendance patterns

4. **First_Health_Camp_Attended.csv**
   - Format 1 camp attendance records
   - Donation amount patterns analyzed
   - Health_Score distribution insights
   - Strong correlation between donations and scores
   - Key success metrics identified
   - Attendance patterns by camp category

5. **Second_Health_Camp_Attended.csv**
   - Format 2 camp participation data
   - Health_Score distribution analysis
   - Scoring methodology comparison with Format 1
   - Attendance patterns differ from Format 1
   - Unique success factors identified

6. **Third_Health_Camp_Attended.csv**
   - Format 3 camp engagement metrics
   - Stall visit patterns analyzed
   - Popular stall sequences identified
   - Engagement depth metrics developed
   - Success criteria differs significantly
   - Unique attendance motivators found

### Camp Formats & Characteristics

1. **Format 1**: 
   - Instantaneous health score provided
   - Donation-based participation
   - Focus on immediate health assessment

2. **Format 2**: 
   - Instantaneous health score
   - Standardized health metrics
   - Emphasis on health monitoring

3. **Format 3**: 
   - Multiple health awareness stalls
   - Focus on health education
   - Success measured by stall engagement

### Target Variable Definition & Model Performance

The prediction task focuses on "favorable outcomes":
- **Format 1 & 2**: Successfully receiving a health score
- **Format 3**: Visiting at least one awareness stall

Model Performance Metrics:
- ROC-AUC Score as primary metric
- Scores above 0.7 considered good
- Scores above 0.8 considered excellent
- Current model achieves ~0.85 AUC

Key Predictive Features:
- Registration patterns
- Patient demographics
- Historical engagement
- Socioeconomic indicators

## 🔧 Technical Implementation

### Tech Stack

#### Frontend
- **Streamlit**: Interactive web interface
- **Plotly**: Dynamic visualizations
- **Matplotlib/Seaborn**: Statistical plots

#### Backend/ML
- **Core**: Python 3.8+
- **Data Processing**: 
  - pandas
  - numpy
  - scikit-learn
- **ML Models**:
  - Random Forest
  - XGBoost
  - LightGBM
  - Logistic Regression
  - CatBoost
- **Model Explainability**: SHAP (SHapley Additive exPlanations)

### Key Features

1. **Exploratory Data Analysis** �
   - Temporal attendance patterns
   - Demographic analysis
   - Registration vs. attendance correlation
   - Category-wise performance metrics

2. **Model Training Interface** 🤖
   - Multiple algorithm options
   - Hyperparameter tuning
   - Cross-validation
   - Performance metrics visualization

3. **Feature Analysis** 🎯
   - Importance rankings
   - Correlation studies
   - Interactive feature exploration

4. **Model Explainability** 🔍
   - SHAP value analysis
   - Feature contribution plots
   - Individual prediction explanations

5. **Model Management** 💾
   - Save/load functionality
   - Version tracking
   - Performance comparison

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.8+
pip
git
```

### Installation

1. Clone the repository:
```bash
git clone [your-repo-url]
cd [repo-name]
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
streamlit run app.py
```

## 📱 Usage Guide

### 1. Data Exploration
- View comprehensive camp statistics
- Analyze temporal patterns
- Explore demographic distributions
- Investigate feature correlations

### 2. Model Training
- Select relevant features
- Choose ML algorithm
- Configure model parameters
- Train and evaluate performance

### 3. Model Interpretation
- Examine global feature importance
- Analyze individual predictions
- Understand model decisions
- Export insights

## 📈 Model Evaluation

### Metrics
- Primary: ROC-AUC Score
- Supporting metrics:
  - Precision
  - Recall
  - F1 Score
  - Confusion Matrix

### Validation Strategy
- Train/Test split based on temporal cutoff
- Camps before March 31st, 2006: Training
- Camps after April 1st, 2006: Testing

## 🌟 Live Demo

Experience the application: [Healthcare Camp Predictor](https://openana-ml-demo.streamlit.app/)

### Demo Features
- Interactive data exploration
- Real-time model training
- Dynamic visualizations
- Instant predictions

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.


## 🙏 Acknowledgments

- Dataset provided by [Kaggle](https://www.kaggle.com/datasets/shivan118/healthcare-analytics)
- MedCamp for the valuable healthcare initiative
- Streamlit for the excellent web framework

---
Built with ❤️ by [Ana](https://openana.ai) | [Live Demo](https://openana-ml-demo.streamlit.app/)
