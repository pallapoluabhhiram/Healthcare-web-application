
## 🧠 Project Title: **AI-Powered Healthcare Web App for Disease Detection**

### 🧬 Project Description:

This project is a **Flask-based web application** that leverages **deep learning models** to detect **Skin Cancer** and **Diabetic Retinopathy (DR)** from medical images. The application provides an accessible, user-friendly interface for early disease diagnosis, helping users and healthcare providers take timely actions.

---
## Here is the drive link

## 🧩 Technologies Used:

* **Frontend:** HTML, CSS (templates: `index.html`, `skin.html`, `dr.html`)
* **Backend:** Python, Flask
* **Deep Learning:** TensorFlow / Keras (`skin1.h5`, `DR.h5` models)
* **Image Processing:** PIL (Pillow), NumPy
* **Machine Learning Frameworks:** Scikit-learn, TensorFlow

---

## 🧪 Features:

### 🔬 Skin Cancer Detection:

* Accepts skin lesion images from users via a file upload.
* Preprocesses images (resize, normalize).
* Uses a pre-trained deep learning model (`skin1.h5`) to predict whether the image indicates **Skin Cancer**.
* Displays results with actionable advice:
  ✅ *“Skin Cancer is NOT DETECTED. You are safe...”*
  ❌ *“Skin Cancer is DETECTED. Please consult a Doctor!!!”*

### 👁️ Diabetic Retinopathy Detection:

* Accepts retinal (eye fundus) images from users.
* Preprocesses images similarly.
* Uses another deep learning model (`DR.h5`) for classification.
* Displays similar results with relevant messages.

---

## 🛠️ Key Functional Components (Code Breakdown):

### 1. **Routes & Navigation:**

* `/` and `/home`: Homepage (`index.html`)
* `/skin`: Skin Cancer input page (`skin.html`)
* `/dr`: Diabetic Retinopathy input page (`dr.html`)

### 2. **Image Preprocessing Functions:**

* `skin_image(image)`: Resizes skin lesion image to 128x128, normalizes pixel values.
* `dr_image(image)`: Similar logic for diabetic retinopathy.

### 3. **Prediction Functions:**

* `classify_image()`: Loads and classifies uploaded skin image using `skin1.h5`.
* `dr_result()`: Processes retinal image using `DR.h5`.

### 4. **Model Outputs:**

Each route uses a threshold (0.5) to determine disease presence and return a message on the HTML page.

---

## 🏥 Use Case:

This application helps in **early screening** of **skin cancer** and **diabetic retinopathy** using **AI-driven automation**, reducing dependency on immediate clinical diagnosis and providing users a way to understand their condition from home.

---

## 🚀 How to Run the App:

### 🔧 Prerequisites:

* Python 3.x
* Flask
* TensorFlow
* Pillow
* NumPy
* Your `.h5` models (`skin1.h5` and `DR.h5`)
* HTML templates in a `/templates/` folder

### 🔌 Steps:

```bash
pip install flask tensorflow pillow numpy
python app.py
```

Then go to `http://127.0.0.1:5000/` in your browser.

---

## 🧠 Future Improvements:

* Add more disease classifiers (e.g., Pneumonia, COVID, etc.)
* Store results in a database for patient records.
* Improve UI/UX using Bootstrap or React.
* Add confidence scores or heatmaps using Grad-CAM for model transparency.

---

Let me know if you'd like a full `README.md` or documentation file for this project too — I’ll generate it for you!
