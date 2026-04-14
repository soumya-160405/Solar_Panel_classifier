# Solar Panel Condition Classification using Deep Learning

## Project Overview
This project implements a Deep Learning solution to automate the inspection of solar panels. By classifying images into various categories of degradation or cleanliness, the system helps in maintaining optimal energy production efficiency and reducing manual inspection costs.

## Problem Statement
Accumulations such as dust, snow, and bird droppings, along with physical or electrical damage, significantly hinder the performance of solar modules. Manual monitoring is inefficient; hence, an automated image classification system is essential for timely maintenance.

## Dataset
The project utilizes the **Solar Panel Images Dataset** (sourced from Kaggle). The dataset contains images categorized into six distinct classes:
- **Clean**: Panels in optimal condition.
- **Dusty**: Panels covered in dust/soiling.
- **Bird-drop**: Panels affected by avian waste.
- **Electrical-damage**: Visible signs of electrical failure or hotspots.
- **Physical-Damage**: Cracks or structural issues.
- **Snow-Covered**: Panels blocked by snow accumulation.

## Technical Implementation
- **Architecture**: MobileNetV2 (Transfer Learning)
- **Framework**: TensorFlow/Keras
- **Preprocessing**: 
  - Image resizing and normalization.
  - Data augmentation to improve model robustness.
- **Training**: The model was fine-tuned on the solar panel dataset, leveraging pre-trained weights from ImageNet for feature extraction.

## Performance & Results
- **Overall Accuracy**: ~74% on the validation set.
- **Key Metrics**:
  - High performance observed in detecting **Bird-drop** (F1-score: 0.84) and **Snow-Covered** (F1-score: 0.84) panels.
  - The model provides a balanced approach between computational efficiency (due to MobileNetV2) and classification accuracy.

## Installation & Usage
1. **Prerequisites**:
   - Python 3.x
   - TensorFlow
   - NumPy, Pandas, Matplotlib
2. **Execution**:
   - Open the `dl-ia2-solar-panel-images.ipynb` notebook in Jupyter or Google Colab.
   - Ensure the dataset path is correctly configured.
   - Run all cells to train the model and visualize results.

## Future Improvements
- Incorporating more diverse training data to improve the detection of 'Physical-Damage'.
- Implementing real-time detection via edge devices for on-site monitoring.
- Experimenting with heavier architectures like EfficientNet for potentially higher accuracy.
