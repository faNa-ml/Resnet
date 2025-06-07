Here is a professional **`README.md`** in **English** tailored for your GitHub project using ResNet to classify images of dogs:

---

# 🐶 ResNet-Based Image Classifier for Dog Breeds

This repository implements a convolutional neural network using a **pre-trained ResNet-18 model** from PyTorch’s `torchvision` library to classify images of dogs. The training pipeline includes data loading, validation, augmentation, transfer learning, and performance visualization.

---

## 📁 Dataset

* Location: `archive_4dog` (update `DATA_PATH` if needed)
* Structure must follow the **ImageFolder format**:

  ```
  archive_4dog/
      ├── breed1/
      │   ├── img1.jpg
      │   ├── img2.jpg
      ├── breed2/
      │   ├── img3.jpg
      │   ├── ...
  ```

---

## 🔧 Features

* **Transfer Learning** with ResNet-18
* Automatic **image validation and cleaning**
* **Data augmentation** using `torchvision.transforms`
* Split into **80% training** / **20% validation**
* Saves trained model as `resnet_pet_classifier.pth`
* Visualization of **loss curves** and **accuracy trends**

---

## 🚀 Setup Instructions

1. **Install Dependencies**

   ```bash
   pip install torch torchvision matplotlib Pillow
   ```

2. **Ensure Directory Structure**
   Confirm the dataset is organized into subfolders by class names.

3. **Run Training Script**

   ```bash
   python resnet_train.py
   ```

---

## 🏋️‍♂️ Training Settings

| Setting       | Value        |
| ------------- | ------------ |
| Model         | ResNet-18    |
| Image Size    | 224×224      |
| Batch Size    | 32           |
| Epochs        | 15           |
| Optimizer     | Adam         |
| Learning Rate | 0.001        |
| Loss Function | CrossEntropy |

---

## 📊 Output

* **Model Checkpoint**: `resnet_pet_classifier.pth`
* **Training Graph**: `resnet_training_results.png`

Example output:

```
Epoch [1/15]
Train Loss: 0.6521 | Val Loss: 0.4783 | Accuracy: 81.25%
...
Training completed successfully!
```

---

## 📈 Visualizations

* **Loss Progression**
* **Validation Accuracy**

<img src="resnet_training_results.png" alt="Training plots" width="600">

---

## 📌 Notes

* Pre-trained weights are used and **base layers are frozen** to speed up training.
* Only the **fully connected head is trained**.
* Code includes a safeguard to **remove corrupted images**.

---


