# Harvestify: Smart Agriculture Assistant

Harvestify is an intelligent web application designed to assist farmers and agricultural stakeholders with critical decisions in crop selection, fertilizer usage, and plant disease diagnosis using AI models.

---

## 📄 Features

### 🌿 Crop Recommendation

Predicts the most suitable crop to grow based on:

* Soil nutrients (N, P, K)
* pH level
* Rainfall
* Real-time temperature and humidity (fetched from OpenWeather API)

### 🌾 Fertilizer Recommendation

Suggests the best fertilizer adjustment based on:

* Crop name
* Current N, P, K levels in the soil

### 🌺 Plant Disease Detection

Identifies plant diseases from uploaded leaf images using a deep learning model (ResNet9).

---

## 🚀 How It Works

### Models Used

* **Plant Disease Classifier**: Trained with ResNet9 on a dataset of leaf images.
* **Crop Recommender**: Trained RandomForest classifier based on agricultural conditions.

### Input-Output Flow

1. **Crop Prediction**: User inputs soil values and selects city; API fetches weather data and predicts suitable crops.
2. **Fertilizer Suggestion**: User provides current nutrient values and crop; system identifies deficiency/excess and recommends accordingly.
3. **Disease Detection**: User uploads a leaf image; model predicts the disease class and displays actionable information.

---



---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/harvestify.git
cd harvestify
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Add Your Weather API Key

Create a file named `config.py` and add:

```python
weather_api_key = "YOUR_API_KEY_HERE"
```

### 4. Run the Application

```bash
python app.py
```

Visit `http://127.0.0.1:5000` in your browser.

---

## 🌍 Live Demo (Optional)

If deployed (e.g., on Render/Heroku), add your app link here.

---

## 📊 Example Input & Output

**Crop Recommendation:**

* Input: N=90, P=42, K=43, pH=6.5, Rainfall=200, City=Delhi
* Output: Recommended Crop: `rice`

**Fertilizer Suggestion:**

* Input: Crop: Wheat, N=60, P=30, K=20
* Output: Suggestion: Add more nitrogen-based fertilizer

**Disease Detection:**

* Input: Upload image of infected tomato leaf
* Output: Detected: `Tomato___Leaf_Mold`

---

## 🚨 Notes

* Ensure stable internet for fetching weather data.
* Model performance may vary based on input quality.

---

## 🚀 Future Improvements

* Add support for multilingual interfaces.
* Enable real-time drone image analysis.
* Support satellite-based soil/water data.

---

## 🌟 Credits

* Dataset: PlantVillage, OpenWeatherMap, and various agriculture datasets
* Deep Learning Model: PyTorch
* Backend: Flask

---

## ✅ License

This project is open-source and available under the MIT License.

---
