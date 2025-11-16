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

**Export formats:** `.fbx` / `.obj` / `.glb`  
**Texture resolution:** **4K–16K** depending on hardware capability

---

### 4️⃣ Mesh Cleanup & Optimization (Blender)
| Operation | Purpose |
|----------|---------|
| Decimation / Retopology | Reduce polygon count |
| UV Unwrap | Maintain texture accuracy |
| Normal / AO Map Baking | Preserve details after poly reduction |
| Scaling & Origin Reset | Correct coordinates |
| Artifact Removal | Remove floating vertices & holes |

🎯 **Goal:** Significant poly reduction with minimal loss in visual quality  
(60–90% reduction targeted)

---

### 5️⃣ Import into Unreal Engine 5
- Enable **Nanite** for high-resolution static meshes
- Import textures & create material shaders
- Generate **LODs** for real-time performance
- Add collisions for walkable environments
- Configure **Lumen lighting & post-processing**
- Arrange environment layout for navigation

---

### 6️⃣ Deployment & Showcase Options
| Output | Use Case |
|--------|---------|
| Windows .exe build | Demonstrations / Hackathons |
| VR build | Immersive campus walkthrough |
| WebGL | Browser-based showcase |
| Video render | Portfolio & exhibitions |

---

## ⚙ Performance Optimization Checklist
- Enable **Nanite** for static environment models
- **LODs** for every mesh
- Occlusion culling for large scenes
- Texture streaming enabled
- Target FPS: **60+**

---

## 🧠 Learnings & Key Takeaways
- Image quality affects accuracy more than image quantity
- Photogrammetry is cost-effective for creating digital twins
- Optimization is essential for real-time rendering in engines like UE5

---

## 🌟 Project Context
This workflow was used to create a **3D virtual college campus** as part of the  
**HackWars Hackathon — Chandigarh University**, under the theme of **Immersive and Spatial Computing**.

---

## 📌 Tools Used
- **RealityCapture** – Photogrammetry reconstruction
- **Blender** – Mesh cleanup & optimization
- **Unreal Engine 5** – Lighting, rendering & deployment

---

## 📧 Contact
For collaboration or research involving photogrammetry or virtual campus simulation, feel free to connect.

