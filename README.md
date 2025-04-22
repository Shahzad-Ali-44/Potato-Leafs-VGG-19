# 🥔 Potato Leaf Disease Detection using VGG-19

This project uses a Convolutional Neural Network (CNN) based on the **VGG-19** architecture to automatically detect and classify diseases in potato leaves. The model identifies whether a leaf is:
- 🟡 Early Blight
- 🔴 Late Blight
- ✅ Healthy



## 🧠 What is VGG-19 and Why Use It?

**VGG-19** is a deep convolutional neural network developed by the Visual Geometry Group (VGG) at Oxford. It has 19 layers (16 convolutional + 3 fully connected) and is known for its simplicity and strong performance in image classification tasks.

### 🔧 How It Works

- **VGG-19 is used as a feature extractor.**  
- **The convolutional base is frozen** to retain learned features from ImageNet.  
- **Custom dense layers are added** to classify potato leaf diseases.  
- **This approach reduces training time** while maintaining high accuracy on a limited dataset.




## 📂 Dataset

- 🔗 **Source**: [Roboflow](https://universe.roboflow.com/ai-xwoe2/potato-eq4aq)
- 🧪 **Classes**: Early Blight, Late Blight, Healthy
- 🖼️ **Size**: 4998 training images(subset), 705 test images
- 🗂️ **Structure**:
  ```
  potato-1/
  ├── train/
  │   ├── Potato___Early_blight/
  │   ├── Potato___Late_blight/
  │   └── Potato___healthy/
  └── test/
      ├── ...
  ```



## ⚙️ Training Configuration

- 📐 Input Size: 224 x 224 x 3
- 📦 Batch Size: 32
- 🧠 Optimizer: Adam (lr=0.001)
- 🔁 Epochs: Up to 50 (with Early Stopping)
- 🎛️ Loss Function: Categorical Crossentropy
- 🎨 Augmentations: Rotation, Zoom, Shift, Flip, Shear



## 📈 Results

- ✅ **Test Accuracy**: ~87%
- 📊 **Confusion Matrix**, **Classification Report**, and sample predictions included
- 🔍 Precision, recall and F1-score available per class



## 🔮 Predictions

The model predicts the class of unseen test images with high confidence. Visualization of predictions is saved in `predictions_VGG-19.png`.


## 📦 Outputs

| File | Description |
|------|-------------|
| `vgg19_potato_model.keras` | Trained model |
| `vgg19_history.npy`        | Training history |
| `confusion_matrix.png`     | Evaluation graph |
| `predictions_VGG-19.png`   | Sample predictions |



## 🛠 Dependencies

Install the required Python libraries:
```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
```



## 📜 License

This project is licensed under the [MIT License](LICENSE).
