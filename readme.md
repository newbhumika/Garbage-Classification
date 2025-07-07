# 🗑️ Garbage Classification using EfficientNetV2B2

This project aims to classify garbage images into **6 distinct categories** — `cardboard`, `glass`, `metal`, `paper`, `plastic`, and `trash` — using **transfer learning** with the **EfficientNetV2B2** architecture.

---

## 🔹 Week 1 Progress:
- ✅ Dataset organized and preprocessed using `image_dataset_from_directory`
- ✅ Applied image resizing and batching (image size: 124×124, batch size: 32)
- ✅ Built model using **EfficientNetV2B2** with ImageNet weights
- ✅ Set up training pipeline with early stopping and model checkpointing

> 📦 Dataset uploaded as `dataset.zip`. Unzip before running the notebook.

---

## 🔹 Week 2 Progress:
- ✅ Model trained for 15 epochs using EarlyStopping
- ✅ Visualized **training and validation accuracy/loss** using Matplotlib
- ✅ Detected class imbalance and signs of overfitting (val accuracy saturation)

---

## 🔹 Week 3 (Final) Progress:
- ✅ Fine-tuned model with improved data pipeline and regularization
- ✅ Achieved **~69% validation accuracy**
- ✅ Evaluated with `classification_report` and **confusion matrix**
- ✅ Created a **Gradio interface** for real-time prediction
- ✅ Saved trained model as `.keras` and `.h5`

### 🔍 Evaluation Summary:
| Metric       | Value    |
|--------------|----------|
| Accuracy     | ~69%     |
| Best Recall  | Paper (91%) |
| Best Precision | Plastic (89%) |

### 📊 Confusion Matrix:
Included in the `notebook` and `pptx` file showing high recall for `paper` and `metal`.

### 🌐 Gradio Web App:
A user-friendly Gradio app allows drag-and-drop image prediction:
```python
gr.Interface(...)



✅ Final Note:

TThis project demonstrates the practical use of transfer learning for environmental AI. While results are promising, future improvements can focus on balancing classes, fine-tuning the model, and optimizing performance for real-world deployment.


