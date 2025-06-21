### 📝 Week 1 Progress Report – Garbage Classification using EfficientNetV2B2

#### ✅ Dataset Preparation
- Created a dataset directory with six class folders:
  - `cardboard`, `glass`, `metal`, `paper`, `plastic`, `trash`
- Used TensorFlow’s `image_dataset_from_directory()` to load and split the dataset into training and validation sets (80/20).

#### ✅ Model Building
- Implemented **EfficientNetV2B2** as the base model using transfer learning (pretrained on ImageNet).
- Added a custom classification head with:
  - `GlobalAveragePooling2D`
  - `Dropout`
  - `Dense(6, activation='softmax')` for 6 classes.

#### ✅ Model Compilation and Training
- Compiled with `Adam` optimizer and `sparse_categorical_crossentropy` loss.
- Used callbacks: `EarlyStopping` and `ModelCheckpoint` to improve training efficiency.
- Training is currently in progress.

#### 🔍 Output Preview
```python
Classes: ['cardboard', 'glass', 'metal', 'paper', 'plastic', 'trash']

Epoch 1/15
64/64 ━━━━━━━━━━━━━━━━━━━━ 45s 488ms/step - accuracy: 0.2166 - loss: 1.7693 - val_accuracy: 0.2455 - val_loss: 1.7236
Epoch 2/15
64/64 ━━━━━━━━━━━━━━━━━━━━ 24s 378ms/step - accuracy: 0.2356 - loss: 1.7334 - val_accuracy: 0.2040 - val_loss: 1.7382
Epoch 3/15
64/64 ━━━━━━━━━━━━━━━━━━━━ 24s 378ms/step - accuracy: 0.2169 - loss: 1.7454 - val_accuracy: 0.2040 - val_loss: 1.7584
Epoch 4/15
64/64 ━━━━━━━━━━━━━━━━━━━━ 24s 376ms/step - accuracy: 0.2076 - loss: 1.7511 - val_accuracy: 0.2733 - val_loss: 1.7262