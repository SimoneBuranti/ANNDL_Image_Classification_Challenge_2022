# 🌱 Plant Image Classification – ANNDL Challenge 2

This project was developed as part of the **Artificial Neural Networks and Deep Learning (ANNDL) Challenge 1**.  
The goal was to build a **Convolutional Neural Network (CNN)** capable of classifying **plant images into 8 classes**.  

Through a **bottom-up approach**, we started with simple models and progressively increased complexity, experimenting with **data augmentation, transfer learning, fine-tuning, and regularization** techniques.  
The final model achieved **91.1% accuracy on the test set**, and the project received a **6/7** evaluation score.  

---

## 📂 Dataset  
- Images were distributed across **8 plant classes**.  
- Dataset split: **85% training / 15% validation** (stratified sampling).  
- No explicit test set was used; evaluation relied on the **Codalab platform**.  

---

## 🚀 Approach  

### 1. **Baseline CNN**  
- Implemented a CNN from scratch as a baseline.  
- Added **data augmentation** (rotations, flips, normalization) to improve generalization.  

### 2. **Transfer Learning & Fine-Tuning**  
We experimented with several pre-trained models:  
- **VGG16** – First attempt, limited performance but interpretable.  
- **DenseNet201** – Better results; also tested with **10-fold cross-validation**.  
- **ConvNeXt Base** – Showed the best performance among tested models.  

### 3. **Regularization & Refinements**  
- **CutMix** data augmentation for improved robustness.  
- Added **GaussianNoise** layer after input.  
- Introduced **Dense + Dropout layers** at the classification head.  
- Tuned **EarlyStopping** patience to handle validation spikes.  

---

## ⚙️ Technologies & Frameworks  
- **Python 3**  
- **TensorFlow / Keras**  
- **Google Colab** (for training and experimentation)  
- **Codalab** (for evaluation)  

---

## 📊 Results  
- Final model: **ConvNeXt Base + CutMix + GaussianNoise + Dropout**.  
- Achieved **91.1% test accuracy** on Codalab.  
- Final evaluation: **6/7 score**.  

---

## 👥 Authors  
- Riccardo Luigi Aielli  
- Salvatore Buono  
- Simone Buranti  

