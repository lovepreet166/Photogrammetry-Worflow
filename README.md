# Photogrammetry-Worflow
# 📌 Photogrammetry Workflow for 3D Modelling  
Using Drone Imagery, RealityCapture, Blender & Unreal Engine 5

This document explains the complete pipeline followed to reconstruct high-fidelity 3D environments from real-world structures using photogrammetry.

---

## 🔄 End-to-End Workflow

### 1️⃣ Dataset Collection — Drone Survey
- Plan flight altitude: **35–70 meters**
- Maintain **70% front overlap** and **60% side overlap**
- Capture in **RAW / high-resolution JPEG**
- Avoid harsh sunlight for uniform shadows
- Use **grid + circular** flight patterns around buildings

📌 **Output:** High-resolution image dataset (hundreds to thousands of photos)

---

### 2️⃣ Image Pre-processing
- Remove blurry and underexposed images
- Group images by building/area
- Optional: color correction / exposure match
- Keep **EXIF + GPS metadata** intact

---

### 3️⃣ Photogrammetry Reconstruction (RealityCapture)
Workflow inside software:
