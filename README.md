# AI-Exam-Anxiety-Prediction
AI-Based Anomaly Detection Platform

An AI-powered anomaly detection system that identifies unusual patterns in datasets and real-time system metrics using machine learning. The platform allows users to upload datasets or monitor system resources (CPU, Memory, Disk) to detect anomalies.

Built using Python, Streamlit, and Isolation Forest, this project demonstrates how AI can be applied for data monitoring, system health analysis, and anomaly detection.

Features

• Upload CSV or Excel datasets for anomaly detection • Automatically works with any numeric columns • Detects normal vs anomalous data points • Shows detected anomalies separately • Displays recent prediction logs • Real-time system metrics monitoring • Download prediction results as CSV • Interactive Streamlit web interface

Tech Stack

Python

Streamlit

Scikit-learn

Pandas

NumPy

Joblib

Psutil

Machine Learning Model

The project uses Isolation Forest, an unsupervised machine learning algorithm designed for anomaly detection.

Isolation Forest works by:

Randomly selecting features

Splitting data points

Isolating rare patterns faster than normal data

Anomalies are detected based on how easily they can be isolated from the dataset.

Project Structure

AI-Anomaly-Detection │ ├── api │ └── app.py # FastAPI server │ ├── data │ ├── collect_metrics.py # Script to collect system metrics │ └── system_metrics.csv # Dataset for training │ ├── model │ ├── train_model.py # Train anomaly detection model │ └── anomaly_model.pkl # Saved ML model │ ├── tester │ └── tester.py # Script to test API endpoints │ ├── logs │ └── prediction_log.json # Stores prediction logs │ ├── streamlit_app.py # Main Streamlit application │ ├── requirements.txt └── README.md

How It Works Dataset Anomaly Detection

User uploads a CSV or Excel file.

Numeric columns are automatically extracted.

Isolation Forest is trained on the uploaded data.

Each record is labeled as:

NORMAL ANOMALY

Results are displayed and can be downloaded.

Real-Time System Monitoring

The application collects:

CPU usage

Memory usage

Disk usage

These metrics are passed to the trained anomaly detection model to predict whether the system behavior is normal or anomalous.

Installation

Clone the repository:

git clone https://github.com/akshattt7/AI-Based-Anomaly-Detection-Platform.git cd AI-Based-Anomaly-Detection-Platform

Create virtual environment:

python -m venv .venv

Activate environment:

Windows

.venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt Running the Application

Start the Streamlit app:

streamlit run streamlit_app.py

The application will open at:

http://localhost:8501 Example Workflow

1️⃣ Upload a dataset 2️⃣ Click Predict Anomaly 3️⃣ View detected anomalies 4️⃣ Download prediction results

OR

Click Use Current CPU, Memory & Disk to analyze real-time system metrics.

Future Improvements

• Image/Screenshot anomaly detection • Time-series anomaly detection • Real-time monitoring dashboard • Cloud deployment • Alert system for anomalies

Author

Akshat Pandey

GitHub https://github.com/akshattt7
