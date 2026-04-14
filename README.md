# Lab-3.4-CNN-Applications-Classification-Detection-Segmentation
Here’s a clean and professional **README.md** for your Lab 3.4 project 👇

---


## 📌 Overview

This lab demonstrates three important applications of **Convolutional Neural Networks (CNNs)** using pretrained models from `torchvision`:

1. **Image Classification** using ResNet
2. **Object Detection** using Faster R-CNN
3. **Semantic Segmentation** using DeepLabV3

All models are pretrained on the **ImageNet** dataset and used for inference on a sample image.

---

## 🛠️ Requirements

Install the required libraries before running the code:

```bash
pip install torch torchvision matplotlib pillow
```

---

## 📂 Project Structure

```
Lab3.4/
│── Sample.jpg
│── main.py
│── README.md
```

---

## 🧠 1. Image Classification (ResNet18)

* Uses a pretrained **ResNet18** model
* Classifies an input image into one of 1000 ImageNet classes

### 🔹 Steps:

* Load image
* Apply preprocessing (resize, normalize)
* Run inference
* Output predicted class index

### ✅ Output:

```
Predicted class: 243
```

---

## 🎯 2. Object Detection (Faster R-CNN)

* Uses pretrained **Faster R-CNN with ResNet50 backbone**
* Detects objects and returns:

  * Bounding boxes
  * Labels
  * Confidence scores

### 🔹 Output Example:

```python
{
  'boxes': Tensor[N, 4],
  'labels': Tensor[N],
  'scores': Tensor[N]
}
```

---

## 🧩 3. Semantic Segmentation (DeepLabV3)

* Uses pretrained **DeepLabV3 (ResNet50 backbone)**
* Performs pixel-wise classification

### 🔹 Output:

* Segmentation mask
* Each pixel assigned a class label

### 🖼️ Visualization:

* Displayed using `matplotlib`
* Color map: `nipy_spectral`

---

## ⚙️ Key Concepts

* **Transfer Learning**: Using pretrained models
* **Tensor Processing**: Image → Tensor → Model
* **Inference Mode**: `torch.no_grad()` for efficiency
* **Evaluation Mode**: `model.eval()` disables training layers

---

## ⚠️ Important Notes

* Ensure `Sample.jpg` exists in the working directory
* Input image must be preprocessed correctly
* GPU is optional but speeds up inference
* Outputs are class indices (not human-readable labels by default)

---

## 🚀 Future Improvements

* Convert class indices to labels (ImageNet classes)
* Draw bounding boxes on detected objects
* Overlay segmentation mask on original image
* Build a simple UI for visualization

---

## 👨‍💻 Author

**Muhammad Suffiyan Rafi**
Computer Scientist | AI/ML Enthusiast

---

If you want, I can also:
✅ Convert this into a **GitHub-ready styled README (with badges & images)**
✅ Add **output screenshots section**
✅ Turn this into a **lab report (PDF/Word)**
