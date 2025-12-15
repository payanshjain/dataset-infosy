# 🧠🔍 DeepVision Crowd Monitor

### AI System for Real-Time Crowd Density Estimation, Overcrowding Detection & Visual Analytics

DeepVision Crowd Monitor is an **end-to-end AI platform** designed to estimate crowd density, detect overcrowded regions, and visualize density maps using **deep learning models and video analysis**.

Built for real-world **public safety and smart surveillance** applications such as:

- 🚉 Railway & Metro Stations  
- ✈️ Airports  
- 🕌 Religious Gatherings  
- 🎉 Festivals & Public Events  
- 🏟 Stadiums  
- 🏙 Smart City Surveillance  

The system combines **deep learning, computer vision, statistical analysis, and an interactive dashboard** to enable intelligent crowd monitoring.

---

## 🚀 Key Features

### 🔹 Real-Time Processing
- Crowd density estimation on image/video frames  
- Fast inference using **FastAPI backend**  
- Live visualization using **Streamlit dashboard**

---

### 🔹 Multiple ML/DL Models Supported

| Model Name       | Description |
|------------------|------------|
| **CSRNet**       | High-accuracy crowd counting using dilated CNN |
| **MobileCSRNet** | Lightweight and fast model optimized for real-time |
| **SimpleCNN**    | Baseline CNN model for demonstration |
| **Random Forest**| Classical ML baseline for comparison |

---

### 🔹 Interactive Dashboard (Streamlit)

Includes:
- 📊 **EDA Viewer**
- 🧪 **Model Evaluation Viewer**
- 🖼 **Prediction Samples**
- 🎛 **Live Demo Tab**
- 📚 **About Page**

---

### 🔹 Automated EDA (Exploratory Data Analysis)
- Distribution plots  
- Heatmaps  
- Correlation matrices  
- Summary statistics  
- Auto-generated CSV reports  

---

### 🔹 Model Evaluation Tools
- MAE, MSE, RMSE metrics  
- Training & validation curves  
- Per-model prediction samples  
- CSV-based evaluation reports  

---

🧱 Architecture Overview
┌────────────────────────┐
│   Streamlit Frontend   │
└─────────────┬──────────┘
              │
              ▼
     API Calls to FastAPI Backend
              │
┌─────────────▼─────────────┐
│       FastAPI Backend     │
│  - Preprocessing          │
│  - Model Inference        │
└─────────────┬─────────────┘
              │
              ▼
┌─────────────────────────────┐
│   Machine Learning Models   │
│ CSRNet, MobileCSRNet, etc.  │
└─────────────────────────────┘
              │
              ▼
┌───────────────────────────────────────────────┐
│ Density Maps • Metrics • EDA • Visual Results │
└───────────────────────────────────────────────┘

📁 Project Structure
deepVision_crowd_monitor/
│
├── backend/               # FastAPI backend for inference
├── frontend/              # Streamlit dashboard (app.py)
├── EDA/                   # Automated EDA scripts & outputs
├── models/                # ML/DL model architectures
├── preprocessing/         # Frame extraction & preprocessing
├── results/               # Evaluation metrics & CSV reports
├── src/                   # Shared utilities
│
├── requirements.txt
└── README.md

⚙️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/springboardmentor0509-source/deepVision_crowd_monitor.git
cd deepVision_crowd_monitor

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

🖥️ Running the Application
🔹 Start FastAPI Backend
cd backend
uvicorn main:app --reload


Backend runs at:
👉 http://localhost:8000

Swagger UI:
👉 http://localhost:8000/docs

🔹 Start Streamlit Dashboard
cd frontend
streamlit run app.py


Dashboard opens at:
👉 http://localhost:8501

📊 EDA & Model Evaluation
✔ EDA Outputs

Located in:

EDA/plots/
EDA/summary/


Includes histograms, heatmaps, correlation plots, and summary statistics.

✔ Model Evaluation Outputs

Located in:

results/


Contains metrics, prediction CSVs, and training curves.

🎯 Use Cases

Smart city surveillance

Public safety monitoring

Stadium & event crowd control

Metro & railway station monitoring

Emergency response systems

🔮 Future Enhancements

Multi-camera fusion

Edge deployment (Jetson Nano)

ONNX / TensorRT optimization

Predictive crowd analytics

Automated SMS / Email alerting

🤝 Contributing

Pull requests and suggestions are welcome!

📜 License

This project is licensed under the MIT License.

