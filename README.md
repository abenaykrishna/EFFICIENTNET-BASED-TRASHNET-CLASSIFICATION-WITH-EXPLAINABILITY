# EfficientNet-Based TrashNet Classification with Explainability

## Project Overview
This project implements a trash classification system utilizing EfficientNet variants on the TrashNet dataset. The primary goal is to enhance waste sorting and recycling practices by classifying images into six distinct waste categories. Additionally, the project incorporates explainability methods, specifically Grad-CAM and Guided Grad-CAM, to visualize the model's decision-making process.

## Dataset
The **TrashNet dataset** consists of a total of **2,527 images** categorized into six classes:

- **Glass:** 501 images
- **Paper:** 594 images
- **Cardboard:** 403 images
- **Plastic:** 482 images
- **Metal:** 410 images
- **Trash:** 137 images

### Data Split
The dataset is divided as follows:

- **Training Data:** 1,617 images
- **Validation Data:** 402 images
- **Test Data:** 2,019 images

## Models
This project employs several EfficientNet variants (B0, B1, B2, B3) for the classification task:

- Each model variant is initialized with pre-trained weights from ImageNet.
- A global average pooling layer and a dense layer are added to adapt the models for the six-class classification task.

### Model Architecture
The architecture for each EfficientNet variant includes:

1. **Input Layer:** Accepts images resized to the required dimensions.
2. **EfficientNet Backbone:** Utilizes the compound scaling method to optimize depth, width, and resolution.
3. **Global Average Pooling Layer:** Reduces the spatial dimensions of the feature maps.
4. **Dense Layer:** Outputs predictions for the six waste categories.

## Explainability Methods
To enhance understanding of model predictions, this project integrates:

- **Grad-CAM (Gradient-weighted Class Activation Mapping):** Provides visual explanations of where the model focuses when making predictions.
- **Guided Grad-CAM:** Combines Grad-CAM with guided backpropagation to produce sharper visualizations.

## Conclusion
This project aims to leverage advanced deep learning techniques for efficient waste classification while promoting transparency in model predictions through explainability methods. The findings can contribute significantly to improving waste management practices and fostering a sustainable environment.

## Installation Instructions
To set up this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/efficientnet-trashnet-classification.git
   cd efficientnet-trashnet-classification
