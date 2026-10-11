# CNN Image Classification Using PyTorch

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** using PyTorch to classify images into 10 different categories using the CIFAR-10 dataset.

The model learns visual patterns and features from images through convolutional layers, ReLU activation functions, and max-pooling layers. It then uses fully connected layers to predict the image category.

The project also includes an interactive image-upload feature that allows users to upload an image and view the model's predicted class and confidence score.

## 🎯 Project Objectives

- Understand the fundamentals of Convolutional Neural Networks.
- Perform image preprocessing and normalization.
- Build a CNN architecture using PyTorch.
- Train the model using the CIFAR-10 dataset.
- Evaluate the model using test-set accuracy.
- Predict the class of a user-uploaded image.

## 📂 Dataset

This project uses the **CIFAR-10 dataset**, which contains 60,000 color images divided into 10 classes.

- Training images: 50,000
- Testing images: 10,000
- Image dimensions: 32 × 32 pixels
- Image channels: 3 (RGB)
- Number of classes: 10

### Classes

1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

The dataset is downloaded automatically using `torchvision.datasets.CIFAR10`.

## 🛠️ Technologies Used

- **Python** — Programming language
- **PyTorch** — Deep learning framework
- **Torchvision** — Dataset loading and image transformations
- **NumPy** — Numerical operations
- **Matplotlib** — Image visualization
- **Pillow (PIL)** — Image processing
- **ipywidgets** — Interactive image upload in Jupyter Notebook

## 🧠 CNN Architecture

The model contains three convolutional blocks followed by fully connected layers.

| Layer | Configuration |
|---|---|
| Convolution 1 | 3 input channels → 32 filters, 3 × 3 kernel |
| ReLU | Non-linear activation |
| Max Pooling | 2 × 2 |
| Convolution 2 | 32 → 64 filters, 3 × 3 kernel |
| ReLU | Non-linear activation |
| Max Pooling | 2 × 2 |
| Convolution 3 | 64 → 128 filters, 3 × 3 kernel |
| ReLU | Non-linear activation |
| Max Pooling | 2 × 2 |
| Flatten | Converts feature maps into a vector |
| Fully Connected 1 | 2,048 → 256 neurons |
| ReLU | Non-linear activation |
| Output Layer | 256 → 10 classes |

### Training Configuration

- Optimizer: Adam
- Loss function: Cross-Entropy Loss
- Batch size: 32
- Number of epochs: 10
- Image normalization: RGB channels normalized using mean 0.5 and standard deviation 0.5

## ⚙️ Project Workflow

1. Load the CIFAR-10 training and testing datasets.
2. Convert images into tensors and normalize pixel values.
3. Create DataLoaders for batch processing.
4. Define the CNN architecture.
5. Initialize the loss function and Adam optimizer.
6. Train the model using forward propagation and backpropagation.
7. Evaluate classification accuracy on the test dataset.
8. Upload a custom image through the notebook interface.
9. Display the predicted class and its confidence score.

## 📊 Model Evaluation

The model is evaluated on the CIFAR-10 test dataset using classification accuracy.

The notebook calculates accuracy by comparing predicted class labels with the actual labels.

**Evaluation metric:** Test Accuracy (%)

The final accuracy depends on the training run. Run the notebook to obtain the actual result before adding it to this README.

## 🖼️ Custom Image Prediction

The notebook provides an interactive image-upload feature.

Users can:
- Upload a JPG, JPEG, or PNG image.
- Preprocess the image to match the model's input format.
- View the image.
- Get the predicted CIFAR-10 class.
- View the model's confidence score.

**Note:** The model is trained on small 32 × 32 CIFAR-10 images. Predictions on real-world images may be unreliable, particularly when the image differs significantly from the training data.

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/CNN-CIFAR_Project.git
cd CNN-CIFAR_Project
```

Replace `YOUR-USERNAME` with your GitHub username and adjust the repository name if necessary.

### 2. Install dependencies

```bash
pip install torch torchvision numpy matplotlib pillow ipywidgets jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run the notebook

Open `CNN-CIFAR_Project.ipynb` and execute the cells in order.

The CIFAR-10 dataset will download automatically when the dataset-loading cell runs.

### 5. Predict a custom image

Run the image-upload cells, upload a supported image, and execute the prediction cell to view the result.

## 📁 Repository Structure

```text
CNN-CIFAR_Project/
│
├── CNN-CIFAR_Project.ipynb
├── README.md
└── datasets/
    └── CIFAR-10 dataset files (downloaded automatically)
```

The dataset folder may be generated locally when the notebook runs; it does not need to be uploaded to GitHub.

## 🔮 Future Improvements

- Plot training and validation loss across epochs.
- Add a confusion matrix and precision, recall, and F1-score.
- Improve generalization using data augmentation.
- Tune hyperparameters to improve classification accuracy.
- Save and load trained model weights.
- Build a web application for real-time image classification.

## 👨‍💻 Author

**Hemant Gulve**

Aspiring Data Analyst and Machine Learning / Deep Learning professional.

This project is part of my learning journey in deep learning, computer vision, and practical implementation using PyTorch.
