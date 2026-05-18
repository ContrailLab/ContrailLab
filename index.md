# ContrailHub: An Open-Access Platform for Global Contrail Detection and Climate Impact

<p align="center">
  <a href="#datasets">📊 Datasets</a> • 
  <a href="#models">💻 AI Models</a> • 
  <a href="#platform">🌐 Online Monitor</a> • 
  <a href="#publications">📝 Publications</a>
</p>

---

## 🛰️ Overview

![ContrailHub Hero Banner](https://images.unsplash.com/photo-1436491865332-7a61a109cc05?auto=format&fit=crop&w=1200&q=80) 
*Image: Satellite-tracked persistent linear contrails and their radiative forcing context.*

**ContrailHub** is a state-of-the-art, open-access platform dedicated to the quantifying, detecting, and mitigating of aviation-induced contrails. Integrating multi-source satellite remote sensing (e.g., MODIS, GOES) with advanced deep learning frameworks, this platform provides high-resolution data products and real-time monitoring tools for researchers, policymakers, and the aviation industry to foster sustainable aviation.

---

## 📊 1. Contrail Detection Datasets (航迹检测数据集)

We provide comprehensive, manually annotated, and cross-validated contrail datasets derived from geostationary and polar-orbiting satellites to benchmarking AI segmentation models.

### 💾 Available Products
| Dataset Name | Satellite Source | Spatial/Temporal Resolution | Coverage | Download |
| :--- | :--- | :--- | :--- | :--- |
| **Contrail-GEO-v1.0** | GOES-16 / High-Res | 2 km / 15-min | North America (2020-2024) | [🔗 Link] |
| **Contrail-MODIS-Global**| MODIS (Aqua/Terra) | 1 km / Daily | Global Hotspots (2018-2025) | [🔗 Link] |

### 🔍 Data Preview
![Dataset Sample Visualization](./assets/images/dataset-preview.png)
*Figure 1: Sample of gridded contrail masks overlaid on false-color infrared satellite imagery.*

---

## 💻 2. Open-Source AI Models (模型代码公开)

Our repository hosts pipeline codes for state-of-the-art pixel-level contrail detection network architectures tailored for atmospheric remote sensing characteristics.

### 🛠️ Model Zoo
* **Contrail-U-Net++**: Optimized U-Net with Atrous Spatial Pyramid Pooling (ASPP) and Squeeze-and-Excitation (SE) modules for capturing long, thin linear features.
* **Spatio-Temporal Transformer**: A continuous-frame tracking network leveraging temporal consistency in geostationary satellite streams.

```bash
# Quick Start: Train our benchmark model on your local cluster
git clone [https://github.com/ContrailHub/contrail-models.git](https://github.com/ContrailHub/contrail-models.git)
cd contrail-models
pip install -r requirements.txt
python train.py --config configs/unet_aspp_modis.yaml
