# Face Authentication for Web Application

**Course:** Introduction to Information Security  
**University:** Ton Duc Thang University  
**Instructor:** Dr. Huynh Ngoc Tu  

---

## Team Members

| Student Name       | Student ID | Role                    |
|-------------------|-----------|-------------------------|
| **Phan Tri Hieu** | 523H0133  | Backend / AI Model      |
| **Le Nhat Huy**   | 523H0138  | Fullstack / Integration |
| **Tran Van Qui**  | 523H0174  | Frontend / UI           |

---

## Project Overview

This project focuses on building a **face authentication system for web applications** using biometric recognition and deep learning techniques. The goal is to replace traditional password-based authentication with a more secure and user-friendly solution.

The system integrates computer vision and machine learning models to perform real-time face detection, feature extraction, and identity verification.

Key components include:
- Face detection and alignment
- Deep feature embedding
- Similarity-based verification
- Liveness detection to prevent spoofing attacks

---

## Repository Structure

* `frontend/`: Web interface (HTML, CSS, JavaScript)
* `backend/`: FastAPI server and processing logic
* `models/`: Pretrained models (FaceNet, MTCNN, dlib)
* `database/`: Stored embeddings and user data
* `README.md`: Project documentation

---

## Tech Stack & Technologies

The system is implemented using the following technologies:

### Backend
* **FastAPI:** High-performance API framework
* **PyTorch:** Deep learning framework
* **MTCNN:** Face detection and alignment
* **FaceNet (InceptionResnetV1):** Feature extraction

### Frontend
* **HTML, CSS, JavaScript**
* **WebRTC:** Webcam access

### Security
* **JWT (JSON Web Token):** Authentication and session management
* **HTTPS:** Secure communication

---

## Key System Workflow

1. Capture real-time image from webcam  
2. Detect and align face using MTCNN  
3. Extract facial embedding using FaceNet  
4. Perform liveness detection:
   - Blink detection  
   - Movement analysis  
5. Compare embeddings using cosine similarity  
6. Return authentication result  

---

## Model Requirement

This project requires the dlib facial landmark model:

Download from:  
http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2  

After downloading:
- Extract the file  
- Place it in the `models/` directory  

---

## How to Run

1. Clone this repository:
```bash
git clone https://github.com/LeNhatHuy219/Face-Authentication-for-Web-Application.git
cd Face-Authentication-for-Web-Application
```
2. Install depencies:
```bash
pip install -r requirements.txt
```
3. Run :
```bash
uvicorn main:app --reload
```
4. Run fronted:
```bash
	•	Open index.html in browser
	•	Or use Live Server
```
---
## Key Features

- **Real-time Face Authentication:**  
  Capture and verify user identity instantly using webcam input.

- **Deep Learning-based Recognition:**  
  Utilize MTCNN for face detection and FaceNet for feature extraction.

- **Liveness Detection (Anti-spoofing):**  
  Prevent fake attacks using blink detection and movement analysis.

- **Cosine Similarity Matching:**  
  Compare facial embeddings to determine identity with high accuracy.

- **Secure Authentication:**  
  Use JWT (JSON Web Token) to manage user sessions securely.

- **Fast and Lightweight System:**  
  Optimized backend using FastAPI for real-time performance.

- **User-friendly Web Interface:**  
  Simple frontend built with HTML, CSS, and JavaScript.


