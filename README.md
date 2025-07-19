# 🌾 Crop Recommendation System

A machine learning-based crop recommendation system that suggests the most suitable crop to grow based on soil and weather conditions. This project uses a Support Vector Machine (SVM) classifier and provides an interactive interface using **Gradio**. It optionally integrates real-time weather data using the **OpenWeatherMap API**.

---

## 📌 Features

- Predicts optimal crops using:
  - Nitrogen (N), Phosphorus (P), Potassium (K)
  - Temperature, Humidity, Rainfall, pH
- Real-time weather data via city name input
- Two interactive Gradio interfaces:
  - Weather Info
  - Crop Recommender
- Lightweight and easy to deploy (no Django/Flask required)

---

## 🧠 Model Details

- **Algorithm**: Support Vector Classifier (SVC)
- **Library**: scikit-learn
- **Trained On**: `crop_data.csv`
- **Features Used**:
  - N, P, K
  - Temperature
  - Humidity
  - pH
  - Rainfall
- **Target Output**: Recommended Crop Name

---

## 📂 Project Structure

```
crop_recommendation/
├── crop_data.csv                # Dataset with soil and weather info
├── crop_recommendation.py      # Main ML and Gradio app
├── README.md                   # Project documentation
```

---

## 🔧 Installation

1. Clone the repository:
```bash
git clone https://github.com/Sharavanakumar-Ramalingam/crop_recommendation.git
cd crop_recommendation
```

2. Install the required dependencies:
```bash
pip install pandas numpy scikit-learn gradio requests
```

---

## ▶️ Usage

Run the app locally:

```bash
python crop_recommendation.py
```

Gradio will start a local server at `http://localhost:7860` — open it in your browser to access the UI.

---

## 🌐 OpenWeatherMap Integration

To fetch real-time weather details using the city name:
- Sign up at [OpenWeatherMap](https://openweathermap.org/api)
- Generate an API key
- Replace the `API_KEY` variable inside `crop_recommendation.py` with your key

```python
API_KEY = "your_api_key_here"
```

---

## 📊 Sample Output

```bash
Accuracy: 0.05
The best suited crop for the given conditions is: ['Carrot']
```

---


## 💡 Improvements to Consider

- Improve model accuracy with better preprocessing and tuning
- Add more samples and regional context to the dataset
- Enhance interface design with more user feedback
- Add support for location-based auto-fetch of weather

---

> “Empowering farmers with data-driven decisions for a better harvest.” 🌿
