# Pranav Shinde — Computer Vision Engineer

**Detection · Segmentation · Tracking · Edge Deployment**

Pune, India · [shindepranav.site](https://shindepranav.site) · [shinde.a.pranav@gmail.com](mailto:shinde.a.pranav@gmail.com)

---

## What I work on

I build CV systems end-to-end — from raw data and annotation infrastructure through model training to production inference. Currently at a defence R&D firm working on object detection and tracking for real operational environments.

Things I've shipped in production:

- **500k+ image annotation pipeline** — bare-metal CVAT (PostgreSQL/Redis/Nginx), YOLO cascade for initial masks, custom SAM 2.1 boundary refiner, watchdog-driven export→process→re-upload loop. No manual triggering.
- **13-class instance segmentation** — mAP50 ~0.74, custom `WeightedDetectionLoss` for severe class imbalance, P2 feature pyramid heads for separating visually similar classes in cluttered scenes.
- **PyTorch → TensorRT INT8 migration** — 9.2 GB → 2 GB memory footprint (−78%), ~23 ms → ~3.7 ms latency. Profiled with Nvidia Nsight Systems/Compute across RTX 3060 and RTX 5080.
- **Dual-GPU training pipeline** — resolved CUDA context conflicts between training and validation processes, cut validation turnaround by 18%.

---

## Stack

| Area | Tools |
|---|---|
| Detection & Segmentation | YOLO v8/v11, SAM 2.1, OpenCV, custom loss functions |
| Tracking | ByteTrack, BoT-SORT, Kalman Filters, ReID |
| Optimization | ONNX, TensorRT, INT8/FP16 quantization, Nsight profiling |
| Training Infra | PyTorch, multi-GPU, CVAT REST API automation |
| MLOps & Cloud | Docker, Kubernetes, AWS (EC2/S3/Lambda/RDS), CI/CD |
| Backend | Python, Node.js, PostgreSQL, Redis |

---

## Open source

### [exportrace](https://github.com/Py528/exportrace)
Benchmark your YOLO model across every export format on your own hardware — PyTorch, ONNX, CoreML, TensorRT — and get real FPS, real latency, real accuracy delta. Because "ONNX is faster" depends entirely on your machine.
`python` `onnx` `tensorrt` `coreml` `benchmarking` · 🚧 active development · [join waitlist](https://exportrace.vercel.app)

---

## Background

- 🎓 B.E. in AI & Data Science — MMCOE, Pune University (2023–2026)
- 🏆 Top 10 National Finalist — Smart India Hackathon 2024 (50,000+ competing teams)
- ☁️ AWS Certified Developer Associate (2024)
- 🪟 Microsoft Azure Fundamentals AZ-900

---

> *Ship the model, not just train it.*
