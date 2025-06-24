# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a deep learning project for tree detection using YOLOv5 and PyTorch. The project is designed for beginners and targets Google Colab execution environment.

**Primary Goal**: Implement basic tree detection on aerial imagery using the NeonTreeEvaluation Benchmark dataset, without tree height/crown width estimation.

## Key Files

- `main.ipynb` - Main Jupyter notebook containing the complete workflow
- `best.pt` - Pre-trained model file for fine-tuning
- `要求.md` - Project requirements and specifications (in Chinese)

## Dataset Information

- **Source**: NeonTreeEvaluation Benchmark dataset
- **Download URL**: https://zenodo.org/records/5914554/files/evaluation.zip?download=1
- **Data Type**: Aerial orthoimagery with annotations
- **Format**: Requires conversion from NeonTree format to YOLO format

## Architecture & Workflow

The project follows a complete machine learning pipeline:

1. **Environment Setup**: Auto-detect GPU availability for Google Colab
2. **Data Pipeline**: Download → Extract → Format Conversion (NeonTree → YOLO)
3. **Model Training**: YOLOv5 with pre-trained model fine-tuning using `best.pt`
4. **Inference**: Detection on test images with visualization

## Development Environment

- **Target Platform**: Google Colab (with GPU auto-detection)
- **Framework**: PyTorch + YOLOv5
- **Format**: Jupyter Notebook cells for direct Colab execution
- **Language**: Bilingual comments (Chinese/English) for learning purposes

## Key Technical Requirements

- Data preprocessing must handle NeonTreeEvaluation annotation format
- Code should be simple and straightforward (student project level)
- Include detailed comments explaining parameters and processes
- Output visualized detection results
- Use provided `best.pt` as starting point for transfer learning

## Development Notes

- This is a beginner-level project focused on learning fundamentals
- Avoid complex fallback methods or advanced optimizations
- Prioritize code clarity and educational value over performance
- All code should be executable in Google Colab environment