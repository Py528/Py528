# 👋 Pranav Shinde

### Computer Vision Engineer | Detection, Tracking & Model Deployment

📍 Pune, Maharashtra, India
📧 shinde.a.pranav@gmail.com
📞 +91 7028625660
🌐 Portfolio: [shindepranav.site](https://shindepranav.site)

![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-ee4c2c?style=flat-square&logo=pytorch)
![YOLO](https://img.shields.io/badge/YOLO-Detection%20%26%20Tracking-blueviolet?style=flat-square)
![ONNX](https://img.shields.io/badge/ONNX-TensorRT-lightgrey?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-Vision-5C3EE8?style=flat-square&logo=opencv)
![AWS](https://img.shields.io/badge/AWS-Deployment-orange?style=flat-square&logo=amazonaws)
![Docker](https://img.shields.io/badge/Docker-Infra-2496ED?style=flat-square&logo=docker)

---

## Who I am

I'm a computer vision engineer working on **object detection, tracking, and edge deployment** — the full pipeline from raw data and annotation through training to production inference. I care most about systems that actually ship, not research demos that sit in a backlog.

I specialize in:
- 🎯 **Detection & segmentation** — YOLO-based instance segmentation, SAM-refined annotation pipelines, class-imbalance handling
- 🔁 **Tracking** — frame-to-track conversion, persistent object IDs across video
- ⚡ **Model optimization** — PyTorch → ONNX/TensorRT migration, INT8 quantization, latency/memory profiling
- 🏗️ **Infra for ML** — self-hosted annotation tooling, GPU pipeline orchestration, cloud deployment (AWS)

---

## Selected work

### 📦 Annotation pipeline for a 500K+ image dataset
Migrated a full CVAT deployment from Docker to bare-metal Linux (PostgreSQL, Redis, Django, OPA, NGINX) to remove container overhead, then built a semi-automated labeling pipeline: a cascade of YOLO models produces initial masks, a custom **SAM 2.1** refiner cleans up boundaries, and a polyshape-to-polytrack converter turns per-frame detections into persistent object tracks. Watchdog-based automation handles export → process → re-upload with no manual triggering.
→ Trained a 13-class instance segmentation model to **mAP50 ~0.74** on this pipeline.

### ⚡ Model deployment & quantization
Migrated inference from PyTorch to ONNX/TensorRT with INT8 quantization:
- Model memory footprint: **9.2GB → 2GB** (-78%)
- Inference latency: **~23ms → ~3.7ms**
- Benchmarked TensorRT engines across an RTX 3060 and RTX 5080, including batch-size sweeps and cold-start vs. warm-inference profiling with Nvidia Nsight Systems/Compute

### 🏷️ Class-imbalanced detection at scale
Built a custom `WeightedDetectionLoss` using inverse-frequency class weighting for a 12-class, 21,000+ image vehicle dataset, and implemented P2 feature-pyramid detection heads to improve separability between visually similar camouflaged object classes.

*(Full write-up and diagrams on my [portfolio](https://shindepranav.site).)*

---

## Also comfortable with

- **Infra/DevOps:** AWS (EC2, Lambda, RDS, S3, CloudWatch), Docker, CI/CD (GitHub Actions, ECR/ECS Fargate) — used to deploy and serve the ML systems above, not as a standalone focus
- **Full-stack:** Next.js, React, Firebase, PostgreSQL — from earlier internship work

---

## Education

🎓 **B.E. in AI & Data Science** — Marathwada Mitra Mandal College of Engineering, Pune (2023–2026)
🎓 **Diploma in Computer Technology** — BVJNIOT, Pune (2020–2023)

---

## Connect

[![Portfolio](https://img.shields.io/badge/Portfolio-shindepranav.site-black?style=flat-square&logo=vercel)](https://shindepranav.site)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Pranav%20Shinde-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com)

---

> Ship the model, not just train it.
