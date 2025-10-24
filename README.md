# 🚴 Tour de France Data Analysis & Dashboard

A comprehensive Business Intelligence project analyzing historical Tour de France data from 1903-2020, featuring interactive dashboards, anomaly detection, and predictive modeling.

## 📊 Project Overview

This project transforms over a century of Tour de France historical data into actionable insights through:
- **Interactive Power BI Dashboard**
- **Machine Learning Models** (Anomaly Detection & Victory Prediction)
- **Data Warehouse Design**
- **Comprehensive ETL Pipeline**

## 🎯 Business Objectives

- Identify performance factors over time (distance, duration, speed)
- Analyze winner distribution by country
- Study participation trends (number of finishers)
- Track evolution of total distance and average time
- Create a historical dashboard for sports analysts and media

## 📁 Project Structure
France_tour/
├── Documents/
│ └── Project Presentation.pdf
├── EDA/
│ └── Exploratory Data Analysis notebooks
├── ML algorithms/
│ ├── anomaly_detection.py
│ └── victory_prediction.py
├── PowerBI Dashboard and webservice/
│ └── Tour_de_France_Dashboard.pbix
└── .gitattributes

## 🛠️ Technologies Used

- **Data Analysis**: Python (Pandas, NumPy)
- **Machine Learning**: Scikit-learn (Isolation Forest, Random Forest)
- **Data Visualization**: Power BI
- **Data Processing**: ETL with Python
- **Version Control**: Git/GitHub

## 📈 Key Features

### 📊 Dashboard KPIs
- **Overall Metrics**: Editions count, participants, winner speed/time, nations diversity
- **Country Analysis**: Wins, riders, stage victories, finishers
- **Rider Analysis**: Performance metrics, podium rates, competitiveness
- **Team Analysis**: Victory rates, stage wins, team performance
- **Stage Analysis**: Distance by type, stage composition, winner dominance

### 🤖 Machine Learning Models

#### 1. Anomaly Detection
- **Algorithm**: Isolation Forest
- **Purpose**: Identify unusual Tour editions
- **Features**: Distance, stages count, starters, finishers
- **Results**: Detected 5 anomalous editions (1903-1905, 1919, 2020)

#### 2. Victory Prediction
- **Algorithm**: Random Forest
- **Purpose**: Predict stage winners
- **Performance**: AUC 0.85, Precision 82%
- **Key Insight**: Distance is the most important factor

## 🗃️ Data Warehouse Schema

### Dimensions:
- `Dim Stage` (stage details, type, locations)
- `Dim Winner` (rider statistics, performance metrics)
- `Dim Tour` (edition overview, dates, participants)
- `Dim Finisher` (rider rankings, country, team)

## 🔧 Data Processing

### Datasets Cleaned:
- `df_finishers` (9,895 rows) - Time normalization, missing value handling
- `df_stages` (2,341 rows) - Location separation, distance normalization
- `df_tours` (109 rows) - Date separation, distance processing
- `df_winners` (102 rows) - Time correction, unit standardization

### ETL Challenges Solved:
- Complex time format conversion (`94h 33' 14"` → seconds)
- Geographical data separation
- Missing value imputation
- Unit standardization

## 🌐 Web Accessibility

- **Published Dashboard**: Power BI Online Service
- **Features**: Interactive visualizations, dynamic filters, multi-page navigation
- **Access**: Secure web link for authorized users

## 👥 Target Users

- **Race Organizers (ASO)**: Event evolution visualization
- **Sports Journalists**: Enriched analytical content
- **Sponsors**: Country-specific visibility analysis
- **Cycling Fans**: Historical trend exploration

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Power BI Desktop
- Required Python packages: pandas, scikit-learn, numpy

### Installation
```bash
git clone https://github.com/Hajer5503/France_tour.git
cd France_tour
pip install -r requirements.txt


