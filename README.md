# Tree Detection using YOLOv5

A deep learning project for tree detection in aerial imagery using YOLOv5 and PyTorch.

## Overview

This project implements automatic tree detection from aerial orthoimagery using the YOLOv5 object detection framework. The system processes the NeonTreeEvaluation Benchmark dataset and trains a custom model to identify individual trees in high-resolution aerial images.

## Dataset

- **Source**: NeonTreeEvaluation Benchmark
- **Format**: RGB aerial imagery with XML annotations
- **Annotations**: PASCAL VOC format converted to YOLO format
- **Classes**: Single class (tree)

## Technical Stack

- **Framework**: PyTorch + YOLOv5
- **Data Processing**: OpenCV, PIL, pandas
- **Environment**: Google Colab (GPU recommended)
- **Languages**: Python 3.7+

## Project Structure

```
├── main.ipynb              # Main Jupyter notebook
├── data/
│   ├── raw/                # Raw dataset files
│   └── processed/          # YOLO format dataset
├── runs/                   # Training outputs
└── yolov5/                 # YOLOv5 repository
```

## Usage

1. **Environment Setup**
   - Open `main.ipynb` in Google Colab
   - Ensure GPU runtime is enabled
   - Run cells sequentially

2. **Data Preparation**
   - Downloads NeonTreeEvaluation dataset automatically
   - Converts XML annotations to YOLO format
   - Splits data into train/validation/test sets

3. **Model Training**
   - Configures YOLOv5 parameters based on available GPU memory
   - Trains from official pretrained weights
   - Saves best model weights

4. **Inference Testing**
   - Runs inference on test images
   - Generates detection statistics
   - Visualizes confidence distribution

## Key Features

- Automatic GPU detection and configuration
- Bilingual comments (Chinese/English)
- Memory management for Colab stability
- Professional training pipeline
- Comprehensive result analysis

## Training Parameters

The system automatically adjusts training parameters based on GPU memory:

- **High-end GPU (≥15GB)**: YOLOv5m, batch=20, epochs=150
- **Mid-range GPU (≥8GB)**: YOLOv5s, batch=16, epochs=120
- **Low-end GPU (<8GB)**: YOLOv5s, batch=8, epochs=100

## Model Performance

The trained YOLOv5 model demonstrates excellent tree detection capabilities:

### Detection Statistics
- **Total Detections**: 3,408 trees detected across test images
- **Average Confidence**: 0.689 (68.9%)
- **Confidence Range**: 0.254 - 0.945
- **Standard Deviation**: 0.184

### Confidence Distribution
- **High Confidence (>0.7)**: 2,044 detections (60.0%)
- **Medium Confidence (0.4-0.7)**: 956 detections (28.1%)
- **Low Confidence (<0.4)**: 408 detections (11.9%)
<img width="901" alt="1334C6A6D5D4337B84624ACF60AE0C68" src="https://github.com/user-attachments/assets/b6286f9d-5a62-47b4-813c-dc02c720515f" />

<img width="911" alt="D231EAFCF5E29384C620941973580088" src="https://github.com/user-attachments/assets/4e1755c1-489f-4d46-95f2-765dd0860ace" />


### Processing Efficiency
- **Test Images Processed**: 20 aerial images
- **Average Detections per Image**: 170.4 trees
- **Maximum Detections in Single Image**: 960 trees
- **Detection Threshold**: 0.25 confidence minimum

### Key Performance Metrics
- **Precision**: High accuracy with 60% of detections above 0.7 confidence
- **Recall**: Effective detection of trees across varying scales and densities
- **Speed**: Real-time inference capability on GPU hardware
- **Robustness**: Consistent performance across different aerial imagery conditions

The model successfully identifies individual trees in complex aerial scenes with high reliability, making it suitable for forestry applications, environmental monitoring, and ecological research.

## Requirements

- Python 3.7+
- PyTorch
- OpenCV
- matplotlib
- pandas
- PyYAML
- tqdm

## License

This project is for educational purposes. Dataset licensing follows NeonTreeEvaluation Benchmark terms.
