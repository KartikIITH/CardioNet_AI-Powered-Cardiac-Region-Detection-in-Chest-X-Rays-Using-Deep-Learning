# 🚀CardioNet_AI-Powered-Cardiac-Region-Detection-in-Chest-X-Rays-Using-Deep-Learning

🚀 **CardioNet:** AI-Powered Cardiac Region Detection in Chest X-Rays Using Deep Learning
🧠 **Overview**
This project demonstrates the application of advanced artificial intelligence and deep learning for medical image analysis. The core objective is to detect and localize the cardiac region in chest X-ray images by predicting bounding boxes around the heart. Built using a custom-labeled dataset and a modified ResNet18 architecture, this work integrates robust data engineering, augmentation, and modern convolutional neural networks for a real-world healthcare problem.

📊 **Data**
Dataset Source: Derived from the RSNA Pneumonia Detection Challenge ([Kaggle link]), using 496 X-ray images annotated with custom heart bounding boxes.

**Labels:** X-ray images are paired with bounding box coordinates (xmin, xmax, ymin, ymax), enabling supervised regression training for object localization.

💡 **Medical Background**
Cardiac detection in X-rays is instrumental for evaluating heart size and position, aiding in the identification of conditions like cardiomyopathy and possible cardiac displacement due to pneumothorax or atelectasis.

Early and automated localization supports faster diagnosis, reducing risks of severe courses and long-term complications.

🎯 **Task**
Build an AI system to predict the bounding box surrounding the heart in each chest X-ray image.

🛠️ **Methodology** 

🏗️ **Data Preprocessing & Augmentation**
Resize images from 1024x1024 to 224x224 pixels (labels are scaled accordingly).

Standardize pixel values to the [0][1] range and normalize using dataset mean and standard deviation.

Split dataset into 400 training and 96 validation images based on subject IDs.

Data Augmentation applied identically to both images and bounding boxes:

🔸 Gamma contrast adjustments (0.7, 1.7)

🔸 Scaling (0.8, 1.2)

🔸 Rotation (-10°, +10°)

🔸 Translation (±10 px)

**Z-normalization is applied for better convergence.**


🔬 **Model Architecture & Training**
**Architecture:**  ResNet18, adapted to:

🖤 Take single-channel (grayscale) X-ray images as input.

🖼️ Output four values corresponding to the bounding box (xmin, xmax, ymin, ymax)

**Loss Function:** Mean Squared Error (MSE) for regression of bounding box coordinates.

**Optimizer:** Adam (lr=1e-4)

**Training:** 50 epochs with robust augmentation pipeline and PyTorch-based training loop.

🏆 **Results**
Demonstrates high-accuracy localization capability for the heart in chest X-ray images.

Model design and data engineering pipeline show readiness for integration into clinical workflows or as a core module in medical AI products.

📦 **Usage Instructions**
Prepare Data: Gather and annotate X-ray images with heart bounding boxes as per RSNA Challenge.

**Run Preprocessing:** Use included scripts/notebooks to preprocess, augment, and split data.

**Train Model:** Train the ResNet18-based regressor using the provided training scripts.

**Evaluate Output:** Validate predicted bounding boxes against ground truth using MSE or IoU metrics.

🛡️ **Key Skills Highlighted**

🤖 **Deep Learning** (PyTorch: ResNet18 customization, loss design, optimizer tuning)

🩺 **Medical Image Processing** (using image augmentation and normalization)

🛤️ **End-to-End AI Workflow** (data cleaning, annotation, custom dataset pipelines, regression on bounding boxes)

🌐 **Practical Application** (project bridges academia and healthcare domain for scalable deployability)

🔭 **Future Work**
Scale up to larger datasets and diverse X-ray modalities.

Adapt for multi-class detection or integration into broader CADx systems.

Further improvement with ensemble techniques and advanced loss functions.
