# 🍅 Tomato Leaf Disease Classification

A deep learning system to detect and classify tomato diseases from leaf spot images using a **Convolutional Neural Network (CNN)** model. The model achieves **93% accuracy** and is deployed via **FastAPI** and accessible through web and mobile apps.

---

## ✅ Key Features

- Classifies common tomato diseases via visible leaf spots.
- CNN trained on annotated tomato leaf image dataset.
- Supports both web and mobile interfaces (React / React Native).
- Fast inference using TensorFlow Lite.
- API hosted via FastAPI + Docker + ECS.
- Images are preprocessed and fed through a deployed model which returns prediction and confidence score.

---

## 🧠 Model Overview

| Architecture | Type     | Accuracy |
|--------------|----------|----------|
| CNN          | Custom   | 93%      |

- Input: Tomato leaf images.
- Output: Predicted disease class and confidence score.
- Optimized for lightweight deployment (TFLite).

---

## 🧰 Tech Stack

- **Backend**: FastAPI, TensorFlow, TensorFlow Lite
- **Frontend**: React, React Native
- **DevOps**: Docker, Amazon ECS, GCP Cloud Storage
- **Libraries**: NumPy, PIL, Uvicorn

---

## 🔍 API Endpoints

| Route       | Method | Description                         |
|-------------|--------|-------------------------------------|
| `/ping`     | GET    | Health check                        |
| `/predict`  | POST   | Upload an image and get prediction  |

### Request Example

**POST** `/predict`  
Body: multipart/form-data with an image file

### Response Example

```json
{
  "class": "Tomato___Late_blight",
  "confidence": 0.9321
}
```

---

## 🖼 Sample Classes

- Tomato___Early_blight  
- Tomato___Late_blight  
- Tomato___healthy

---

## 🚀 How to Run Locally

1. **Clone Repository**
   ```bash
   git clone https://github.com/SteveParadox/Agric_ai.git
   cd Agric_ai/Api
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run FastAPI App**
   ```bash
   uvicorn api:app --reload
   ```

4. **Access API**
   - Visit `http://localhost:8000/docs` to use Swagger UI

---

## 📱 Mobile/Web Integration

- **React Web App**: Upload tomato leaf images from browser.
- **React Native App**: Capture image via phone camera and send to API.
- Designed to support farmers with easy, quick disease identification.

---

## 🐳 Docker Support

```bash
docker build -t tomato-disease-api .
docker run -p 8000:8000 tomato-disease-api
```

---

## ☁️ Cloud Deployment

- **Model Hosting**: TensorFlow Serving on GCP
- **API Server**: Docker container on Amazon ECS

---

## 📁 Repo Structure

```
├── Api/
│   ├── api.py
│   ├── model_tf_serving.py
│   ├── requirements.txt
├── models/
│   ├── model.h5
│   └── model.tflite
├── Training/
│   └── Tomato_Disease_Prediction.ipynb
├── README.md
```

---

## 🧪 Future Improvements

- Add support for more crop types.
- Integrate pest detection.
- Add local language support for UI.
- SMS or WhatsApp bot support for farmers without smartphones.

---

## 📜 License

MIT License © SteveParadox
