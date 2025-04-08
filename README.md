# Human-Face-Shapes-Classification
Human Face Shapes Classification Just Using Custom CNN 

![human face](https://github.com/alirzx/Human-Face-Shapes-Classification/blob/main/photo_6030725518216774984_y.jpg)

# Project Overview
This project focuses on classifying human face shapes into five distinct categories using a custom Convolutional Neural Network (CNN). Accurately determining face shapes has practical applications in areas such as personalized recommendations for hairstyles, eyewear, and cosmetics.

# Problem Statement
Human faces can be categorized into specific shapes based on their geometric features. The primary face shape categories include:

### Heart: Characterized by a wider forehead and a narrow chin.

### Oblong: Longer than it is wide, with a balanced forehead, cheekbones, and jawline.

### Oval: Forehead is slightly wider than the chin, with a rounded jawline.

### Round: Equal width and height with soft, rounded edges.

### Square: Forehead, cheekbones, and jawline are approximately the same width with a strong jawline.

The objective is to develop a model that can automatically classify a given facial image into one of these five categories.

# Dataset
The dataset utilized for this project comprises images labeled according to the aforementioned face shape categories. Each category contains a balanced number of images to ensure unbiased learning. The images have been preprocessed to standardize dimensions and enhance feature extraction.

# Methodology
## Data Preprocessing
### Image Resizing: All images are resized to 224x224 pixels to maintain uniformity.

### Normalization: Pixel values are normalized to the range [0, 1] to facilitate faster convergence during training.

### Augmentation: Techniques such as rotation, flipping, and zooming are applied to increase dataset diversity and improve model generalization.

# Model Architecture
The custom CNN model is designed with the following architecture:

## Convolutional Layers: Extract spatial features from input images.

## Batch Normalization: Normalize activations to stabilize and accelerate training.

## ReLU Activation: Introduce non-linearity to the network.

## MaxPooling Layers: Downsample feature maps to reduce dimensionality.

## Fully Connected Layers: Integrate extracted features for final classification.

## Dropout Layers: Prevent overfitting by randomly setting a fraction of input units to zero during training.

The final layer utilizes a softmax activation function to output probabilities for each of the five face shape categories.

# Training Configuration
## Loss Function: Cross-Entropy Loss, suitable for multi-class classification tasks.

## Optimizer: AdamW, chosen for its adaptive learning rate and weight decay capabilities.

## Learning Rate Scheduler: ReduceLROnPlateau, which reduces the learning rate when the validation loss plateaus, enhancing model performance.

## Gradient Scaling: Implemented using GradScaler to manage mixed-precision training and prevent gradient underflow.

# Results
The model's performance is evaluated using accuracy and the F1-score. The confusion matrix indicates the model's proficiency in distinguishing between similar face shapes. Detailed performance metrics and visualizations are provided in the accompanying Jupyter notebooks.

### test set results :
![accuracy-loss](https://github.com/alirzx/Human-Face-Shapes-Classification/blob/main/Plots/photo_6030725518216774998_y.jpg)
![test confusion matrix ](https://github.com/alirzx/Human-Face-Shapes-Classification/blob/main/Plots/photo_6030725518216774999_x.jpg)

# Conclusion
This project demonstrates the feasibility of classifying human face shapes using a custom CNN. The approach can be extended to other applications requiring facial feature analysis. Future work may involve integrating more complex architectures or leveraging transfer learning to enhance accuracy further.
