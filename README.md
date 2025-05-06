# 🚀 Spacecraft Detection and Debris Classification using YOLOv8


## 1. 🛰️ Introduction

With the increasing number of space missions, Earth's orbital environment has become congested with satellites, defunct spacecraft, rocket bodies, and space debris. These high-velocity objects pose serious threats to operational missions, making real-time detection critical.

Traditional debris monitoring techniques (like radar and manual inspection) struggle with scale. With advances in high-resolution satellite imaging, deep learning-based automation is essential.

### 🔍 Why This Project?

We initiated this project to support global space safety and sustainability efforts through automated vision-based debris and spacecraft detection.

### 🎯 Key Objectives

- Apply computer vision to space operations.
- Build a scalable, real-time object detection system using YOLOv8.
- Enable potential integration with space traffic management systems.

### 🌍 Societal Impact

- **Safety**: Prevent space collisions.
- **Sustainability**: Enhance long-term orbital operations.
- **Efficiency**: Minimize manual monitoring.
- **Education**: Promote AI adoption in aerospace.

---

## 2. 🧠 Methodology

### ⚙️ Overview

We used **YOLOv8**—a high-speed, anchor-free object detection model—for accurate identification and classification of spacecraft and debris.

### 📊 Architecture Pipeline


### 🧪 Steps Followed

1. **Dataset Preparation**
   - Dataset: SPARK 2022 Stream-1 ([Access Dataset](https://cvi2.uni.lu/spark-2022-dataset/))
   - Label verification and augmentation
   - Split: 70% train, 15% validation, 15% test

2. **Model Training**
   - Fine-tuned YOLOv8 pretrained weights
   - Augmentations: rotation, brightness/contrast, Gaussian noise
   - Hyperparameter tuning: learning rate, batch size, epochs

3. **Evaluation Metrics**
   - mAP@0.5, precision, recall
   - Class-wise performance
   - Visual validation via bounding box overlays

4. **Deployment (Optional)**
   - OpenCV-based real-time object detection on satellite imagery

---

## 3. 📁 Dataset Description

- **Name**: SPARK 2022 Stream-1
- **Size**: ~110,000 RGB images
- **Classes**: 11 (10 spacecraft + 1 space debris)
- **Type**: Synthetic, photo-realistic simulation

### 🧩 Challenges Addressed

- Cluttered orbital environments
- Lighting variations and shadows
- Tiny and irregular objects
- Low signal-to-noise image conditions

📥 **Dataset Link**: [https://cvi2.uni.lu/spark-2022-dataset/](https://cvi2.uni.lu/spark-2022-dataset/)

---

## 4. 📈 Results & Ablation Study

### ✅ Overall Performance (YOLOv8)

| Metric          | Score    |
|-----------------|----------|
| mAP@0.5         | 95.3%    |
| Precision       | 93.7%    |
| Recall          | 90.1%    |
| Debris Precision| 99.5%    |

### 🔁 Comparison with YOLOv5

| Model   | mAP@0.5 | Precision | Recall  |
|---------|---------|-----------|---------|
| YOLOv5  | 83.2%   | 85.0%     | 82.5%   |
| YOLOv8  | 95.3%   | 93.7%     | 90.1%   |

### 🧵 Class-wise Performance

| Class                   | Precision | Recall | mAP@0.5 |
|------------------------|-----------|--------|---------|
| debris                 | 99.5%     | 95.8%  | 99.4%   |
| lisa_pathfinder        | 96.8%     | 98.2%  | 99.1%   |
| earth_observation_sat_1| 85.2%     | 79.8%  | 86.6%   |

### ⚡ Why YOLOv8 Performed Best

- Anchor-free architecture for faster detection
- Decoupled head improves classification and localization
- Batch normalization & augmentation for generalization
- High debris precision (99.5%) crucial for mission safety

---

## 5. ✅ Conclusion

This project demonstrates that **YOLOv8** is a robust and efficient solution for detecting spacecraft and classifying space debris in satellite images.

### 🚀 Contributions

- Improved orbital situational awareness
- Reduced risk of space collisions
- Scalable, real-time surveillance framework

### 🔭 Future Work

- Integrate temporal analysis for object tracking
- Test on real satellite video streams
- Explore deployment in onboard spacecraft modules


---

## 📚 Citation

If you use the dataset, cite the original paper:


---

## 💬 Contact

For collaboration or queries, feel free to reach out via GitHub Issues or email listed on the project website.

---



