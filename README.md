
# 🦷 Automated Dental PAI Scoring System

[![Powered by YOLOv8](https://img.shields.io/badge/Model-YOLOv8m--Seg-blue)](https://github.com/ultralytics/ultralytics)
[![Framework FastAPI](https://img.shields.io/badge/API-FastAPI-green)](https://fastapi.tiangolo.com/)
[![Status](https://img.shields.io/badge/Status-Clinically_Validated-orange)]()

An AI-powered diagnostic tool that automates the **Periapical Index (PAI)** scoring system for dental X-rays. Unlike traditional models that rely on raw pixel counts, this system uses a **Scale-Invariant Smart Ratio** to score lesions accurately regardless of image zoom or resolution.

## 🎯 Key Features
* **Precision Detection:** Uses `YOLOv8m-seg` with `retina_masks` for high-fidelity lesion segmentation.
* **Smart Scoring:** Calculates `Lesion / Tooth Structure` ratio to assign PAI scores (1-5).
* **False Positive Rejection:** Successfully ignores healthy trabecular bone patterns and root fillings (Gutta-percha).
* **Deployable API:** Full FastAPI backend ready for clinical integration.

## 🖼️ Clinical Results
| PAI 1 (Healthy) | PAI 3 (Moderate) | PAI 5 (Severe) |
| :---: | :---: | :---: |
| ![Healthy](path/to/healthy_screenshot.jpg) | ![PAI3](path/to/pai3_screenshot.jpg) | ![PAI5](path/to/pai5_screenshot.jpg) |
| *Model correctly ignores healthy bone* | *Accurate segmentation of apical loss* | *Detection of large-scale infection* |

## 🛠️ Tech Stack
* **Core Model:** YOLOv8 Medium (Segmentation)
* **Backend:** FastAPI + Uvicorn
* **Processing:** OpenCV (CLAHE, Thresholding)
* **Deployment:** Ngrok / Docker

## 🚀 Quick Start
### 1. Clone & Install
```bash
git clone [https://github.com/yourusername/dental-pai-scoring.git](https://github.com/yourusername/dental-pai-scoring.git)
cd dental-pai-scoring
pip install -r requirements.txt
