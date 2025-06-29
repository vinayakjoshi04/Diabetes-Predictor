# 🩺 Diabetes Predictor using Logistic Regression & Flask

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A web-based diabetes prediction application that uses **Machine Learning** to assess diabetes risk based on medical parameters. Built with **Logistic Regression** and deployed using **Flask** web framework.

![image](https://github.com/user-attachments/assets/cd41e6db-b5f5-4e1c-91c9-94f25aa0e157)

## 🎯 Overview

This project implements a diabetes risk assessment tool using the famous **Pima Indians Diabetes Dataset**. The application provides a user-friendly web interface where users can input their medical parameters and receive an instant prediction about their diabetes risk.

## ✨ Features

- 🤖 **Machine Learning Model**: Logistic Regression trained with scikit-learn
- 📊 **Data Preprocessing**: Input scaling using StandardScaler for optimal performance
- 🌐 **Web Interface**: Clean and intuitive Flask-based web application
- 📱 **Responsive Design**: Mobile-friendly user interface
- ⚡ **Real-time Predictions**: Instant results with "Diabetic" or "Not Diabetic" classification
- 🎨 **Professional UI**: Modern, medical-themed design with smooth animations

## 🧠 Model Performance

| Metric | Score |
|--------|-------|
| **Algorithm** | Logistic Regression |
| **Accuracy** | ~81% |
| **Dataset** | Pima Indians Diabetes Dataset |
| **Features** | 8 medical parameters |
| **Preprocessing** | StandardScaler normalization |

### 📈 Model Evaluation Metrics
- **Accuracy Score**: Model performance on test data
- **Confusion Matrix**: Classification accuracy breakdown
- **Precision & Recall**: Detailed performance metrics
- **Feature Importance**: Analysis of key risk factors

## 📁 Project Structure

```
DIABETES-PREDICTOR/
├── 📊 Diabetes_Predictor.ipynb    # Jupyter notebook with model training
├── 📈 diabetes.csv                # Pima Indians Diabetes dataset
├── 🤖 model.pkl                   # Trained Logistic Regression model
├── ⚖️ scaler.pkl                   # Fitted StandardScaler object
├── 🐍 app.py                      # Flask backend application
├── 📁 templates/
│   └── 🌐 index.html             # Web UI template
├── 📋 requirements.txt            # Python dependencies
├── 📖 README.md                   # Project documentation
└── 📄 LICENSE                     # MIT License
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/diabetes-predictor.git
   cd diabetes-predictor
   ```

2. **Create virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Open in browser**
   ```
   http://127.0.0.1:5000
   ```

### Manual Installation
If you don't have a requirements.txt file:
```bash
pip install flask numpy scikit-learn pandas matplotlib seaborn
```

## 📊 Input Parameters

The model requires 8 medical parameters for prediction:

| Parameter | Description | Normal Range | Unit |
|-----------|-------------|--------------|------|
| **Pregnancies** | Number of pregnancies | 0-20 | count |
| **Glucose** | Plasma glucose concentration | 70-100 (fasting) | mg/dL |
| **Blood Pressure** | Diastolic blood pressure | 60-80 | mmHg |
| **Skin Thickness** | Triceps skinfold thickness | 12-25 | mm |
| **Insulin** | 2-hour serum insulin | 16-166 | μU/mL |
| **BMI** | Body Mass Index | 18.5-24.9 | kg/m² |
| **Diabetes Pedigree** | Genetic predisposition score | 0.078-2.42 | function |
| **Age** | Age in years | 1-120 | years |

## 🎯 Usage Example

1. **Navigate to the web interface**
2. **Fill in your medical parameters**:
   - Pregnancies: `2`
   - Glucose: `120 mg/dL`
   - Blood Pressure: `80 mmHg`
   - Skin Thickness: `20 mm`
   - Insulin: `100 μU/mL`
   - BMI: `25.5`
   - Diabetes Pedigree: `0.5`
   - Age: `35 years`
3. **Click "Analyze Risk"**
4. **View your prediction result**

## 🔬 Model Training Process

The machine learning pipeline includes:

1. **Data Loading**: Load Pima Indians Diabetes dataset
2. **Exploratory Data Analysis**: Statistical analysis and visualization
3. **Data Preprocessing**: Handle missing values and feature scaling
4. **Model Training**: Train Logistic Regression classifier
5. **Model Evaluation**: Assess performance using multiple metrics
6. **Model Serialization**: Save trained model and scaler using pickle

## 📈 Dataset Information

**Pima Indians Diabetes Dataset**
- **Source**: UCI Machine Learning Repository
- **Samples**: 768 instances
- **Features**: 8 medical predictor variables
- **Target**: Binary classification (0: Non-diabetic, 1: Diabetic)
- **Missing Values**: Handled during preprocessing

## 🛠️ Technical Stack

- **Backend**: Flask (Python)
- **Machine Learning**: scikit-learn
- **Data Processing**: pandas, NumPy
- **Visualization**: matplotlib, seaborn
- **Frontend**: HTML5, CSS3, JavaScript
- **Model Persistence**: pickle

## 🚀 Deployment Options

### Local Development
```bash
python app.py
```

### Cloud Deployment
- **Heroku**: Platform-as-a-Service deployment
- **Render**: Modern cloud platform
- **Streamlit Cloud**: ML-focused deployment
- **AWS/GCP/Azure**: Enterprise cloud solutions

### Docker Deployment
```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python", "app.py"]
```

## 🔮 Future Enhancements

- [ ] **Enhanced UI/UX**: Bootstrap or Tailwind CSS integration
- [ ] **Model Improvements**: Ensemble methods (Random Forest, Gradient Boosting)
- [ ] **User Authentication**: Login/signup functionality
- [ ] **Prediction History**: Save and track user predictions
- [ ] **Data Visualization**: Interactive charts and risk factor analysis
- [ ] **API Endpoints**: RESTful API for mobile app integration
- [ ] **Real-time Monitoring**: Model performance tracking
- [ ] **Multi-language Support**: Internationalization
- [ ] **Medical Validation**: Healthcare professional review system

## 📊 Performance Metrics

```python
# Model Performance Summary
Accuracy: 81.2%
Precision: 0.78
Recall: 0.74
F1-Score: 0.76
AUC-ROC: 0.85
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Medical Disclaimer

**Important**: This application is for educational and research purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with a qualified healthcare provider for medical concerns.

## 🙏 Acknowledgments

- **Dataset**: Pima Indians Diabetes Dataset from UCI ML Repository
- **Libraries**: scikit-learn, Flask, pandas, NumPy community
- **Inspiration**: Healthcare AI and preventive medicine research
- **Contributors**: Thanks to all contributors who help improve this project

## 📞 Contact

- **GitHub**: [@vinayakjoshi04](https://github.com/vinayakjoshi04)
- **Email**: vinayakjoshi2004@gmail.com
- **LinkedIn**: [Your Profile](https://www.linkedin.com/in/vinayak-joshi-99521528b/)

---

⭐ **Star this repository if you found it helpful!** ⭐

<div align="center">
  <img src="https://forthebadge.com/images/badges/made-with-python.svg" alt="Made with Python">
  <img src="https://forthebadge.com/images/badges/built-with-love.svg" alt="Built with Love">
</div>
