
# 🚀 Project Overview

Pneumonia is a life-threatening lung infection that must be detected early.
This project uses a **transfer learning approach with ResNet50** to classify chest X-rays into three categories:

* **NORMAL**
* **VIRAL PNEUMONIA**
* **BACTERIAL PNEUMONIA**

The model is trained using the **Chest X-Ray Dataset**, fine-tuned with **FastAI**, and deployed using a simple **Gradio web interface**.

---

# 🎥 Demo Video

Click the link below to watch the model prediction demo:

▶️ **[Pneumonia Detection Output Video](https://drive.google.com/file/d/1tFxbH3axuyvKr7kV4Y0cxzd6xQEUfRu0/view?usp=sharing)**

---

# 🧠 Model Details

### ✔ Algorithm

* **ResNet50** pretrained on ImageNet
* Fine-tuned using FastAI’s `vision_learner()`

### ✔ Learning Process

* Random **80/20 train-validation split**
* Image resizing to **128×128**
* Fine-tuned for **25 epochs**
* Achieved strong accuracy (verified using interpretation tools)

### ✔ Metrics

* **Accuracy**
* **Confusion Matrix** using `ClassificationInterpretation`

---

# 🛠 Technologies Used

* Python 3
* FastAI
* FastBook
* PyTorch
* ResNet50
* Gradio (for deployment UI)
* Pillow (PIL)

---

# 🌐 Gradio Web App

The project includes an interactive **Gradio** web interface.

To launch:

```python
iface.launch()
```

This gives an output like:

```
Running on local URL: http://127.0.0.1:7860
```

Upload an X-Ray image → the model returns the pneumonia type instantly.

---

# 🧾 Sample Predictions

Sample output from the model:

```
('BACTERIAL', tensor(0), tensor([9.9985e-01, 1.84e-07, 1.47e-04]))
```

```
('VIRAL', tensor(2), tensor([6.40e-04, 5.74e-05, 9.99e-01]))
```

These values represent:

* **Predicted class**
* **Class index**
* **Probabilities for each class**

---

