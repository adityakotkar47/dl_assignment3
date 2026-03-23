# 🎯 YOLO26 Object Detection Lab

> **Lab Assignment** — Deep Learning & Computer Vision | 2025–26

## 👥 Group Details

| Member | Roll No | PRN | GitHub | Email |
|--------|---------|-----|--------|-------|
| Rishi Waghmare (Leader) | 12 | 202301040014 | [@RishiWaghmare12](https://github.com/RishiWaghmare12) | rishi12waghmare@gmail.com |
| Jidnyesh Suryawanshi | 49 | 202301040053 | [@Jidnyesh12](https://github.com/Jidnyesh12) | jidnyesh0149@gmail.com |
| Shivam Hippalgave | 41 | 202301040046 | [@Kingshivamx](https://github.com/Kingshivamx) | shivamhippalgave@gmail.com |
| Aditya Kotkar | 7 | 202301040009 | [@adityakotkar47](https://github.com/adityakotkar47) | adityakotkar47@gmail.com |

## 👨‍🏫 Faculty Details

- **Faculty Name:** Dr. Diptee Chikmurge(Ghusse)
- **Designation:** Professor
- **Email:** dvchikmurge@comp.maepune.ac.in

## 🏫 Institute Details

- **Institute:** MIT Academy of Engineering, Alandi
- **Department:** Computer Engineering
- **Course Code:** 2311332L
- **Academic Year:** 2025-26, Semester VI
- **Lab Date:** 19/03/2026
- **Submission Date:** 22/03/2026

---

## 📋 About This Project

This project implements **object detection**, **instance segmentation**, and **image classification** using **YOLO26** (Ultralytics). We evaluate multi-task performance and explore real-world applications in traffic monitoring.

### Key Features
- ✅ Object Detection with YOLO26n
- ✅ Instance Segmentation with YOLO26n-seg
- ✅ Image Classification with YOLO26n-cls
- ✅ Multi-model benchmarking (n, s, m variants)
- ✅ Model export (ONNX, TorchScript)
- ✅ Real-world application: Traffic & Road Safety Monitoring

---

## 🔧 Setup

### Requirements
```bash
pip install ultralytics roboflow supervision matplotlib seaborn pandas numpy opencv-python-headless
```

### Dataset
- **Dataset:** COCO128 (subset of COCO with 128 images, 80 classes)
- **Source:** Built-in with Ultralytics (auto-downloads during training)

---

## 🚀 Run

1. Open `YOLO26_Object_Detection_Lab.ipynb` in Google Colab
2. Set Runtime → Change runtime type → GPU (T4 recommended)
3. Run all cells sequentially
4. Results will be saved in `/content/runs/` and `/content/predictions/`

---

## 📊 Results

### Detection Performance (YOLO26n on COCO128)

| Metric | Value |
|--------|-------|
| mAP@50 | 0.6676 (66.76%) |
| mAP@50-95 | 0.4994 (49.94%) |
| Precision | 0.7142 (71.42%) |
| Recall | 0.5845 (58.45%) |
| Training Time | 10 epochs in 0.020 hours |

### Model Comparison

| Task | Model | mAP@50 | mAP@50-95 | Top-1 Acc | Inf. Time (ms) |
|------|-------|--------|-----------|-----------|----------------|
| Detection | YOLO26n | 0.6676 | 0.4994 | N/A | 24.4 |
| Segmentation | YOLO26n-seg | N/A | N/A | N/A | 22.4 |
| Classification | YOLO26n-cls | N/A | N/A | 52.34% | N/A |

### Variant Benchmark

| Model | Parameters (M) | Inference Time (ms) |
|-------|----------------|---------------------|
| YOLO26n | 2.57 | 24.4 |
| YOLO26s | 10.01 | 57.5 |
| YOLO26m | 21.90 | 81.2 |

---

## 🌍 Real-World Application

**Domain:** Traffic & Road Safety Monitoring

**Problem Statement:** Real-time detection of vehicles, pedestrians, and traffic signs to improve road safety and enable autonomous driving systems.

**How YOLO26 Helps:** Provides real-time object detection with high accuracy, enabling fast inference needed for traffic monitoring. Multi-class detection identifies various road objects simultaneously.

**Key Challenges:**
- Varying lighting conditions
- Object occlusions
- Small object detection
- Real-time processing requirements

**Deployment:** Edge devices (Jetson Nano) / Cloud infrastructure

---

## 📁 Repository Structure

```
.
├── YOLO26_Object_Detection_Lab.ipynb   # Main notebook
├── README.md                            # This file
├── requirements.txt                     # Python dependencies
├── results/
│   ├── detection_output.png            # Detection visualization
│   ├── segmentation_output.png         # Segmentation visualization
│   ├── classification_top5.png         # Classification results
│   ├── training_curves.png             # Training metrics
│   ├── benchmark_comparison.png        # Model comparison
│   └── domain_application.png          # Traffic monitoring demo
└── exports/
    ├── best.pt                         # PyTorch weights
    ├── best.onnx                       # ONNX export
    └── best.torchscript                # TorchScript export
```

---

## 🎓 Learning Outcomes

1. ✅ Understood YOLO26 architecture and its variants
2. ✅ Configured YOLO26 pipeline on COCO128 dataset
3. ✅ Performed detection, segmentation, and classification
4. ✅ Evaluated models using mAP, Precision, Recall metrics
5. ✅ Optimized models through fine-tuning and augmentation
6. ✅ Exported models for deployment (ONNX, TorchScript)
7. ✅ Explored traffic monitoring as real-world application

---

## 📜 Undertaking

All code, analysis, results, and observations presented in this project are our own work and have not been copied from any other group or external source without proper attribution. We have followed academic integrity guidelines throughout this assignment.

---

## 📝 License

This project is submitted as part of academic coursework at MIT Academy of Engineering, Alandi.

---

## 🔗 References

- [Ultralytics YOLO Documentation](https://docs.ultralytics.com/)
- [COCO Dataset](https://cocodataset.org/)
- [YOLO26 on Hugging Face](https://huggingface.co/Ultralytics/YOLO26)

---

**Last Updated:** 22/03/2026
