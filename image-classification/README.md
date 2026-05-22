# Image Classification Project

A complete beginner-friendly image classification system using Python, TensorFlow, and Keras. This project trains a Convolutional Neural Network (CNN) to classify images and provides prediction functionality.

## 📋 Project Overview

This project demonstrates:
- Building a CNN model with TensorFlow/Keras
- Training on image datasets
- Saving and loading trained models
- Making predictions on new images
- Visualizing accuracy and loss graphs
- Professional Python project structure

## 📁 Folder Structure

```
image-classification/
│
├── data/                    # Image dataset folder
│   ├── train/              # Training images organized by class
│   ├── test/               # Testing images organized by class
│   └── sample_images/      # Sample images for prediction
│
├── models/                 # Saved trained models
│   └── image_classifier_model.h5
│
├── images/                 # Output graphs and results
│   ├── accuracy_loss_graph.png
│   └── predictions_results.png
│
├── main.py                 # Main entry point
├── train.py                # Training script
├── predict.py              # Prediction script
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
├── .gitignore             # Git ignore file
└── venv/                  # Virtual environment (not uploaded to GitHub)
```

## 🚀 Quick Start Guide

### 1. Create Virtual Environment

```bash
# Navigate to project directory
cd image-classification

# Create virtual environment (Windows)
python -m venv venv

# Create virtual environment (macOS/Linux)
python3 -m venv venv

# Activate virtual environment (Windows)
venv\Scripts\activate

# Activate virtual environment (macOS/Linux)
source venv/bin/activate
```

### 2. Install Dependencies

```bash
# Upgrade pip
pip install --upgrade pip

# Install required packages
pip install -r requirements.txt
```

### 3. Prepare Dataset

Create sample dataset folders:

```bash
# Create data structure
mkdir -p data/train/class1 data/train/class2
mkdir -p data/test/class1 data/test/class2
mkdir -p models images
```

Add images to the data folders (minimum 10 images per class for training).

### 4. Train the Model

```bash
python train.py
```

This will:
- Load images from `data/train/`
- Build CNN model
- Train for 10 epochs
- Save model to `models/image_classifier_model.h5`
- Generate accuracy/loss graph

### 5. Make Predictions

```bash
python predict.py
```

This will:
- Load the trained model
- Make predictions on images in `data/sample_images/`
- Display results with confidence scores

### 6. Run Complete Pipeline

```bash
python main.py
```

This runs the entire workflow from training to prediction.

## 📦 Requirements

- Python 3.7+
- TensorFlow 2.x
- Keras (included with TensorFlow)
- NumPy
- Matplotlib
- scikit-learn
- Pillow

See `requirements.txt` for specific versions.

## 📊 Model Architecture

The CNN model includes:
- Input layer: 224x224 RGB images
- 3 Convolutional blocks with MaxPooling
- Dropout for regularization (0.5)
- Flatten layer
- Dense layers (128 units)
- Output layer (Softmax for multi-class classification)

## 📈 Performance Metrics

After training, the project generates:
- **Accuracy & Loss Graph**: Visual representation of model performance
- **Prediction Results**: Confidence scores for test images
- **Training Logs**: Detailed metrics for each epoch

## 🔧 Customization

### Change Image Size
In `train.py` and `predict.py`, modify:
```python
IMG_SIZE = (224, 224)  # Change to desired size
```

### Change Number of Epochs
In `train.py`, modify:
```python
EPOCHS = 10  # Change to desired number
```

### Change Batch Size
In `train.py`, modify:
```python
BATCH_SIZE = 32  # Change to desired size
```

## 🐛 Troubleshooting

**Issue**: Module not found error
- **Solution**: Ensure virtual environment is activated and all packages are installed

**Issue**: No images found in data folder
- **Solution**: Check folder structure and add images to `data/train/` subdirectories

**Issue**: Out of memory error
- **Solution**: Reduce batch size or image resolution

**Issue**: Model not found during prediction
- **Solution**: Train the model first using `train.py`

## 📱 Dataset Requirements

- **Minimum**: 10 images per class
- **Recommended**: 50-100 images per class
- **Supported formats**: JPG, PNG, BMP
- **Image size**: Will be resized to 224x224 (configurable)
- **Classes**: Organize in subdirectories by class name

## 💾 Saving Results

The project automatically saves:
- Trained model: `models/image_classifier_model.h5`
- Accuracy/Loss graph: `images/accuracy_loss_graph.png`
- Predictions: Console output and optional CSV

## 🔐 Security & Best Practices

- Use virtual environment to isolate dependencies
- Add sensitive data to `.gitignore`
- Commit code but not large model files
- Use meaningful variable names
- Add comments for complex logic
- Validate all inputs

## 📚 Learning Resources

- [TensorFlow Documentation](https://www.tensorflow.org/learn)
- [Keras API Reference](https://keras.io/api/)
- [CNN Basics](https://www.tensorflow.org/tutorials/images/cnn)
- [Image Classification Guide](https://www.tensorflow.org/tutorials/images/classification)

## 🎓 University Submission

### ZIP File Preparation

```bash
# Create ZIP file (Windows)
Compress-Archive -Path image-classification -DestinationPath image-classification.zip

# Create ZIP file (macOS/Linux)
zip -r image-classification.zip image-classification -x "image-classification/venv/*" "image-classification/.git/*" "image-classification/.DS_Store"
```

### Files to Include

✅ Include:
- All `.py` files
- `requirements.txt`
- `README.md`
- `.gitignore`
- `data/` folder structure
- `models/` folder (if model is generated)
- `images/` folder (output graphs)

❌ Exclude:
- `venv/` folder (recreate with pip install)
- `.git/` folder
- `__pycache__/` directories
- `.pyc` files

## 📝 License

This project is created for educational purposes.

## ❓ FAQ

**Q: Can I use different image formats?**
A: Yes, the project supports JPG, PNG, and BMP formats.

**Q: How long does training take?**
A: Depends on dataset size and system. Typically 2-5 minutes for 100 images per class.

**Q: Can I use GPU acceleration?**
A: Yes, TensorFlow automatically uses GPU if available.

**Q: How do I improve model accuracy?**
A: Use more training data, adjust hyperparameters, or use data augmentation.

---

**Created for University Assignment**
**Last Updated**: 2024
