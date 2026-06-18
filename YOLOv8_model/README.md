# YOLOv8 Steel Defect Detection Workflow

This component of the repository focuses on utilizing the **YOLOv8** architecture for real-time object detection and classification of surface defects on steel sheets. 

## 📁 Pipeline & Directory Structure

The files in this folder are split into two separate, dedicated components to keep the workflow modular:

1. **`NEU_DET_YOLO_Permanent/` (The Dataset Partition):**
   * This directory houses the dataset images and structural layout.
   * **Note on Format:** The original raw data was explicitly converted and re-structured into **XML annotation format** (bounding box coordinates, labels, and image metadata) to ensure compatibility with localized preprocessing and evaluation pipelines.

2. **`yoloModel1.py` (The Training Pipeline):**
   * This is a standalone, separated script dedicated entirely to handling the model lifecycle. 
   * It handles loading the core YOLOv8 network weights, parsing the data splits via configuration paths, executing the training epochs, and saving the optimized model checkpoints.

---

## 🎯 Target Defect Classes
The architecture is trained to detect, localize, and classify the following six structural surface anomalies:
* **Cr** (Crazing)
* **In** (Inclusion)
* **Pa** (Patches)
* **Ps** (Pitted Surface)
* **Rs** (Rolled-in Scale)
* **Sc** (Scratches)

---

## 🚀 Getting Started

### 1. Prerequisites
Install the required computer vision and deep learning packages in your environment:
```bash
pip install ultralytics opencv-python matplotlib
