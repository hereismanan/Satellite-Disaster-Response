# 🛰️ Satellite Disaster Response

## 📘 Overview
This project leverages deep learning and satellite imagery to assess disaster damage automatically.
By analyzing pre- and post-disaster satellite images, the model classifies affected areas into multiple
damage levels, enabling faster and more accurate disaster response and recovery operations.

---

## ⚙️ Problem Statement
During large-scale disasters such as earthquakes, floods, or hurricanes, rapid assessment of infrastructure
damage is crucial. Manual inspection is time-consuming and inconsistent.
This project automates the process using computer vision models trained on satellite imagery.

---

## 🎯 Motivation & Impact
- ⚡ Accelerate post-disaster analysis and response time.
- 🛰️ Utilize open satellite data for real-world humanitarian applications.
- 🤖 Reduce human dependency and subjective bias in damage assessment.
- 🌍 Support rescue planning and prioritization using AI predictions.
- 💡 Demonstrate how machine learning can contribute to social good.

---

## 🧩 Project Workflow
1. **Data Preprocessing**
   - Dataset used: `xView2` Disaster Dataset.
   - Pre- and Post-disaster images were resized, normalized, and augmented.
   - Data split into training, validation, and testing sets.

2. **Model Training**
   - Baseline: `ResNet18` (transfer learning from ImageNet).
   - Transformer-based models:
     - `Vision Transformer (ViT)`
     - `Swin Transformer`
   - Loss function: CrossEntropyLoss
   - Optimizer: Adam / AdamW
   - Learning Rate Scheduling used for optimization stability.

3. **Evaluation**
   - Accuracy and F1-score used as performance metrics.
   - Confusion matrix and per-class performance visualized.
   - Validation accuracy reached ~78.7% (best model).

4. **Visualization**
   - Sample predictions visualized using `matplotlib`.
   - Grad-CAM visualizations for understanding damaged regions.

---

## 🧠 Model Architectures
- **ResNet18**: Convolutional backbone for strong baseline performance.
- **Vision Transformer (ViT)**: Captures global context using self-attention.
- **Swin Transformer**: Hierarchical representation learning for fine-grained spatial understanding.

---

## 📊 Results
| Model | Validation Accuracy | Notes |
|--------|--------------------|-------|
| ResNet18 | 78.76% | Strong baseline CNN |

---

## 🧪 Tools & Libraries
```python
torch          # Deep learning framework
torchvision    # Pretrained models and transforms
matplotlib     # Visualization
numpy          # Numerical processing
PIL            # Image processing
scikit-learn   # Metrics and evaluation
```

---

## How to Run

# 1️⃣ Clone the repository
git clone https://github.com/<your-username>/Satellite-Disaster-Response.git
cd Satellite-Disaster-Response

# 2️⃣ Install dependencies
pip install -r requirements.txt

# 3️⃣ Run the notebook
jupyter notebook Satellite_Disater.ipynb

# 4️⃣ (Optional) Visualize results
python visualize_predictions.py
