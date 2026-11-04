# 🏙️ CivicAI – Intelligent Civic Issue Detection & Reporting System

**An AI-powered web application for detecting civic issues, assessing their severity, and generating structured complaints to support better urban maintenance.**

## 📌 Project Overview

CivicAI is an AI-based civic issue detection and reporting system designed to help identify common public infrastructure problems using images.

Users can upload an image of a civic issue, and the trained deep learning model predicts the issue category. The system also provides severity assessment, suggests the responsible department, and generates a structured complaint report.

The main goal of CivicAI is to make civic issue identification and complaint preparation easier, faster, and more organized.

## 🎯 Objectives

- Detect common civic issues using Artificial Intelligence.
- Classify uploaded images into different civic issue categories.
- Assess the severity of detected issues.
- Identify the relevant municipal department.
- Generate structured complaint reports.
- Maintain a local history of submitted complaint records.

## 🚧 Civic Issues Supported

The system supports five categories:

| Category | Description |
|---|---|
| 🕳️ Pothole | Detects potholes on roads |
| 🛣️ Road Damage | Identifies damaged road surfaces |
| 🗑️ Garbage | Detects garbage and waste accumulation |
| 💡 Broken Streetlight | Identifies damaged streetlights |
| 🚰 Drainage Problem | Detects drainage-related issues |

## 🤖 AI Model

CivicAI uses **MobileNetV2**, a convolutional neural network (CNN) architecture with ImageNet-pretrained weights.

### Model Details

- Base Model: MobileNetV2
- Pre-trained Weights: ImageNet
- Input Image Size: 224 × 224
- Number of Output Classes: 5
- Fine-tuning: Selected backbone layers and classifier head
- Optimizer: AdamW
- Loss Function: CrossEntropyLoss with class weights
- Model Checkpoint: `models/civic_model_improved.pth`

## ✨ Key Features

- **Image Upload:** Upload civic issue images for AI-based analysis.
- **Issue Classification:** Predicts one of five civic issue categories.
- **Confidence Score:** Displays the model's prediction confidence.
- **Severity Assessment:** Estimates the seriousness of the detected issue.
- **Department Assignment:** Suggests the relevant department based on the issue.
- **Complaint Generation:** Generates structured complaint text and PDF reports.
- **Complaint History:** Maintains locally stored complaint records.
- **Evidence Storage:** Stores uploaded evidence images.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| PyTorch | Deep learning framework |
| MobileNetV2 | Image classification model |
| Flask | Backend web framework |
| HTML | Web page structure |
| CSS | User interface styling |
| JavaScript | Frontend interactions |
| Streamlit / Other tools | Only include if used in the final implementation |
| Pillow | Image processing |

## 📂 Project Structure

```text
CivicAI/
│
├── dataset/
│   ├── pothole/
│   └── garbage_final/
│
├── models/
│   └── civic_model_improved.pth
│
├── notebooks/
│
├── app/
│   ├── templates/
│   └── static/
│
├── outputs/
│   ├── complaint_records.json
│   └── evidence_photos/
│
├── requirements.txt
├── README.md
└── app.py
```

*Note: Update this structure to match the exact files in your final GitHub repository.*

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/sachin007123/CivicAI.git
```

### 2. Open the Project Folder

```bash
cd CivicAI
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Environment

**Windows:**

```bash
venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Run the Application

If your Flask entry-point file is `app.py`:

```bash
python app.py
```

Open the local URL displayed in the terminal in your web browser.

## 🔄 System Workflow

1. User opens the CivicAI web application.
2. User uploads an image of a civic issue.
3. The uploaded image is preprocessed.
4. MobileNetV2 analyses the image.
5. The system predicts the civic issue category.
6. Severity is assessed.
7. The responsible department is suggested.
8. A structured complaint report is generated.
9. Complaint details and evidence are stored locally.

## 📊 Expected Output

The application provides:

- Predicted civic issue category.
- Prediction confidence.
- Estimated severity level.
- Suggested responsible department.
- Generated complaint details.
- Downloadable complaint PDF.
- Locally maintained complaint history.

## 🔐 Privacy and Limitations

- Uploaded images and complaint records are stored locally.
- The system is intended as a civic issue identification and reporting prototype.
- AI predictions may not always be accurate.
- Severity assessments should be verified by responsible authorities.
- The application prepares complaint reports but does not automatically submit complaints to official government portals.

## 🚀 Future Enhancements

- GPS-based civic issue location tracking.
- Live municipal complaint submission integration.
- Admin dashboard for complaint management.
- Real-time complaint status tracking.
- Mobile application development.
- Larger and more diverse training datasets.
- Improved model accuracy and performance.
- Integration with smart city platforms.

## 🎓 Academic Project Details

**Project Name:** CivicAI – Intelligent Civic Issue Detection and Reporting System

**Course:** B.Sc. Artificial Intelligence and Machine Learning

**University:** AMET University

**Project Type:** Final Year Capstone Project

**Developed By:** Sachin I.

## 👨‍💻 Author

**Sachin I.**

- GitHub: [@sachin007123](https://github.com/sachin007123)

---

⭐ **If you find this project interesting, consider giving the repository a star!**

*Building smarter communities through Artificial Intelligence.*
