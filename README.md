# VisionPlus


### Explainable AI for Diabetic Retinopathy Screening

> **SIH 26038 — MedTech / BioTech / HealthTech**

VisionPlus is an explainable AI-based screening application designed to support diabetic retinopathy assessment from retinal fundus images.

The system combines image-quality assessment, deep-learning-based diabetic retinopathy grading, retinal vessel analysis, and Grad-CAM visualization to provide an interpretable screening result and referral support.

---

## 🎯 Problem Statement

Diabetic retinopathy is a major complication of diabetes that can lead to vision loss when not identified and managed appropriately.

In rural and resource-limited settings, access to specialized retinal screening and ophthalmic expertise can be limited.

VisionPlus aims to provide an AI-assisted screening workflow that can support preliminary assessment of retinal fundus images and help identify cases that may require further clinical evaluation.

---

## 💡 Proposed Solution

VisionPlus provides an end-to-end retinal image screening workflow:

**Fundus Image → Image Quality Assessment → Preprocessing → DR Grading → Explainability → Screening Report**

The application is designed for use with retinal fundus images obtained from compatible fundus-camera systems.

---

## 🔬 Key Features

### 1. Image Quality Assessment

Evaluates the uploaded retinal image for factors such as:

* Focus
* Illumination
* Field of view
* Overall image quality

Images can be categorized as:

* Good
* Borderline
* Ungradable

### 2. Diabetic Retinopathy Grading

A deep-learning model performs diabetic retinopathy classification using five grades:

| Grade | Description      |
| ----- | ---------------- |
| 0     | No DR            |
| 1     | Mild DR          |
| 2     | Moderate DR      |
| 3     | Severe DR        |
| 4     | Proliferative DR |

For the prototype screening workflow, grades 2–4 are treated as requiring referral consideration.

### 3. Explainable AI

VisionPlus uses **Grad-CAM** to generate a visual explanation of the model prediction.

The application displays:

* Original fundus image
* Grad-CAM visualization
* Predicted grade
* Confidence
* Screening interpretation

### 4. Retinal Vessel Analysis

A U-Net-based segmentation model is included for retinal vessel analysis and supporting image interpretation.

### 5. Screening Report

The application provides a structured screening result containing:

* Patient information
* Image-quality result
* DR grade
* Confidence
* Explainability visualization
* Referral indication
* Screening recommendation

---

## 🧠 AI / ML Components

### DR Classification

**ResNet18**

Used for five-class diabetic retinopathy grading.

### Vessel Segmentation

**U-Net**

Used for retinal vessel segmentation and supporting analysis.

### Explainability

**Grad-CAM**

Used to visualize image regions contributing to the model prediction.

---

## 🏗️ System Workflow

```text
              ┌─────────────────────┐
              │   Fundus Camera /   │
              │    Image Upload     │
              └──────────┬──────────┘
                         ↓
              ┌─────────────────────┐
              │  Image Quality      │
              │    Assessment       │
              └──────────┬──────────┘
                         ↓
              ┌─────────────────────┐
              │   Preprocessing     │
              └──────────┬──────────┘
                         ↓
              ┌─────────────────────┐
              │   DR Classification │
              │      ResNet18       │
              └──────────┬──────────┘
                         ↓
              ┌─────────────────────┐
              │   Grad-CAM          │
              │  Explainability     │
              └──────────┬──────────┘
                         ↓
              ┌─────────────────────┐
              │ Screening Result &  │
              │      Report         │
              └─────────────────────┘
```

---

## 🖥️ Application

VisionPlus is currently deployed as a **standalone Windows application** using MATLAB Runtime.

### Deployment

* Application: **VisionPlus**
* Version: **1.0.0**
* Platform: **Windows 64-bit**
* Deployment: **MATLAB Standalone Application**
* Runtime: **MATLAB Runtime**

The deployed application provides the complete VisionPlus user interface and screening workflow.

---

## 📊 Datasets

The development workflow uses publicly available retinal imaging datasets including:

* APTOS 2019
* IDRiD
* DRIVE
* Messidor-2

These datasets support different components of the image classification, segmentation, and evaluation workflow.

---

## 🌐 Intended Use

VisionPlus is intended as a **prototype screening-support system**.

It is designed to assist screening workflows, particularly where access to specialized retinal assessment may be limited.

It is **not intended to replace ophthalmologists, physicians, or professional medical diagnosis**.

All screening results should be reviewed by qualified healthcare professionals.

---

## 🌾 Rural Healthcare Vision

The proposed workflow is designed with resource-constrained screening environments in mind.

A potential deployment scenario is:

**Portable Fundus Camera → Laptop/Tablet → VisionPlus → AI Screening → Explainable Result → Referral Support**

This can help support preliminary screening workflows in rural and community healthcare settings.

---

## 🔐 Privacy

Patient information and application-generated local history are intended to remain on the user's system.

No real patient-identifying information should be uploaded to this public repository.

---

## 🚀 Future Enhancements

Planned improvements include:

* Direct fundus-camera integration
* Mobile/tablet support
* Additional lesion segmentation
* Improved model validation
* Multilingual clinical reporting
* Cloud-based deployment
* Secure healthcare data management
* Integration with clinical referral workflows

---

## 👥 VisionPulse Team

**Project:** VisionPlus
**Team:** VisionPulse Team
**SIH Problem Statement:** 26038
**Domain:** MedTech / BioTech / HealthTech

---

## ⚠️ Disclaimer

VisionPlus is a prototype research and screening-support application.

AI-generated results are not a medical diagnosis and should not be used as the sole basis for clinical decisions.

Clinical decisions must be made by qualified healthcare professionals.

---

## 📄 License

This repository is provided for academic and demonstration purposes.

