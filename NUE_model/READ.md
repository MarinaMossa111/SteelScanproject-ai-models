# NUE Model Component

This directory houses the **NUE Model** architecture, a specialized neural network framework integrated into the pipeline to run parallel evaluations and comparative benchmarks alongside the YOLO architectures for industrial steel surface defect detection.

## 📁 Workflow & Directory Structure

To maintain a clean and modular codebase, the datasets and execution configurations for this model are separated into distinct pipelines:

1. **Structured Data Segregation:**
   * Contains localized data splits optimized for the specific tensor shapes and input dimensions required by this model framework.
   * Annotated paths are kept fully isolated from the YOLO components to prevent any cross-contamination during model benchmarking.

2. **Core Training & Validation Scripts:**
   * Built as independent, separated files to manage the complete deep learning lifecycle of the network.
   * Handles feature map extraction, localized loss functions, validation metric calculations, and weight checkpointing.

---

## 🔬 Purpose and Integration

The primary objective of this standalone component is to provide high-fidelity structural defect analysis. By deploying this parallel model structure, the system achieves:
* **Comparative Benchmarking:** Evaluates precision, recall, and processing latency directly against the YOLOv8/v11 models.
* **Architecture Validation:** Cross-verifies bounding box predictions on intricate material anomalies, focusing on multi-scale surface defect localization.
* **Optimized Feature Representation:** Leverages specific architectural backbones tailored to high-resolution structural texture classification.

---

## 🛠️ Getting Started

### 1. Environment Setup
Ensure your deep learning environment has the necessary framework libraries installed (adjust based on your specific implementation backend, e.g., PyTorch or TensorFlow):
```bash
pip install torch torchvision numpy scikit-learn
