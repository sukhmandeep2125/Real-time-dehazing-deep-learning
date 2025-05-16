
# Real-Time Dehazing Using Deep Learning

This repository contains a complete pipeline for real-time image and video dehazing using deep learning. The project implements and compares multiple variants of a CNN-based DeepDehazeNet model with 4, 8, and 16 convolutional layers. The best-performing model is further used for real-time video dehazing and Raspberry Pi deployment.

---

## 📁 Folder Structure

```
.
├── 4_layer_model/          # 4-layer DeepDehazeNet model, training notebook, and results
├── 8_layer_model/          # 8-layer model, weights, and plots
├── 16_layer_model/         # 16-layer model and its outputs
├── comparison_model/       # Python script comparing all three models + results table
├── dataset/                # Hazy and clear images for training/testing
├── video_project/          # Video input/output and real-time dehazing script
├── raspberry_results/      # Outputs from Raspberry Pi deployment
├── gflop_analysis/         # Model complexity analysis (GFLOPs)
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
├── LICENSE                 # License file
└── .gitignore              # Files to ignore in version control
```

---

## 🚀 Features

- Train DeepDehazeNet with 4, 8, and 16 layers
- Compare models using PSNR, SSIM, visual results, and GFLOPs
- Select the best-performing model
- Perform real-time video dehazing with OpenCV
- Deploy dehazing on Raspberry Pi with HDMI display
- Save plots, tables, and videos for reproducible analysis

---

## 🧪 How to Run

### 1. Clone Repository
```bash
git clone https://github.com/sukhmandeep2125/real-time-dehazing-using-deep-learning.git
cd real-time-dehazing-using-deep-learning
```
### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3.Train Models (Jupyter Notebooks)
```bash
Open and run:

4_layer_model/4_model.ipynb

8_layer_model/8_model.ipynb

16_layer_model/16_model.ipynb

```
### 4. Compare Models
Run:
```bash
python comparison_model/final_comparison_models.py

```

### 5. Run Real-Time Video Dehazing
```bash
python video_project/video.py
```

---

## 📊 Results

All result plots (loss, PSNR, SSIM) and comparison tables are available in the `results_(layers)/` folders of each model. Final comparison is stored in `comparison_model/results/`.

---

## 💻 Raspberry Pi Deployment
For embedded hardware testing, the best-performing model was deployed on a Raspberry Pi with a 7-inch HDMI screen. Outputs are saved in `raspberry_results/`.

---

## ⚙️ GFLOP Analysis
The notebook `gflop_analysis/GFLOPs_analysis.ipynb` compares model complexities (GFLOPs) to guide optimal deployment decisions.

---

## 📦 Dataset

Images are stored in the `dataset/` folder:
- `dataset/hazy/` — Hazy input images
- `dataset/clear/` — Ground truth images

---


## 🎥 Demo Output

Below is an example output using the best DeepDehazeNet model:
![Demo](results/demo.gif)

---

## 📜 License

This project is licensed under the MIT License.

---

## ✍️ Authors

- Sukhmandeep singh (sukhmandeep2125@gmail.com)
