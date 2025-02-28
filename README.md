# Mobile-Based Multi-Organ Segmentation Transformer for CT Medical Images

## Table of Contents

1. [Objective](#objective)
2. [Technology Stack](#technology-stack)
3. [Dataset Description](#dataset-description)
4. [Models Used](#models-used)
   - [UNETR](#unetr)
   - [UNET](#unet)
   - [DETR](#detr)
5. [Front-End Design](#front-end-design)
6. [Flask Framework](#flask-framework)
7. [Deployment](#deployment)
8. [GPU vs TPU Training](#gpu-vs-tpu-training)
9. [Project Screenshots](#project-screenshots)
10. [Summary](#summary)
11. [References](#references)

## Objective

- Develop a mobile application for multi-organ segmentation.
- Implement a transformer-based architecture for segmenting organs in abdomen CT images.
- Integrate the mobile application with the segmentation algorithm.
- Deploy the system on a cloud platform.

## Technology Stack

- **Frontend:** Flutter (Google Firebase for authentication)
- **Deep Learning Framework:** TensorFlow
- **Data Processing:** NumPy, OpenCV
- **Infrastructure:** GPUs and TPUs
- **Deployment:** Amazon Web Services (AWS)

## Dataset Description

- **Name:** Synapse Multi-Organ Segmentation Dataset
- **Source:** [Synapse Website](https://www.synapse.org/)
- **Total Data Used:** 4720 images and masks
- **Format:** CT Scans with segmentation masks

## Models Used

### UNETR

- Uses a Vision Transformer encoder with a CNN-based decoder.
- Achieves global context understanding with self-attention mechanisms.
- Produces high-resolution segmentation maps.

### UNET

- Traditional encoder-decoder architecture for semantic segmentation.
- Uses convolutional layers with skip connections.
- Outputs multi-class segmentations.

### DETR

- Detection Transformer model for object segmentation.
- Utilizes a ResNet-50 backbone for feature extraction.
- Employs Transformer attention mechanisms for segmentation.

## Front-End Design

- **Authentication:** Email and phone OTP verification via Firebase.
- **User Interface:** Upload CT images, segment using the model, and display results.
- **Model Selection:** Users can choose between UNET, UNETR, and DETR.

## Flask Framework

- **Backend Processing:** Handles image uploads, model inference, and results transmission.
- **Integration with Flutter:** Uses Base64 encoding for seamless communication.
- **API Endpoints:** REST API for image segmentation and processing.

## Deployment

- **AWS EC2 Instance:** Hosts Flask backend.
- **Command for Deployment:** `python org_flask.py`
- **Challenges:** Resource limitations on AWS SageMaker led to model training on Kaggle.

## GPU vs TPU Training

| Processor          | Time per Epoch | Total Training Time |
| ------------------ | -------------- | ------------------- |
| CPU                | 6 hours        | Extremely slow      |
| GPU (Google Colab) | ~200 sec      | 5.5 hours           |
| TPU                | ~100 sec      | 2.7 hours           |

## Project Screenshots

![image](https://github.com/user-attachments/assets/2f339761-70e7-4f5c-8638-3347ac5a2403)


## Summary

An end-to-end Android application for segmenting CT scan images into 10 organs has been designed and deployed. The system integrates deep learning models with a mobile interface, enabling real-time medical image segmentation.

## References

- [UNETR Paper](https://openaccess.thecvf.com/content/WACV2022/papers/Hatamizadeh_UNETR_Transformers_for_3D_Medical_Image_Segmentation_WACV_2022_paper.pdf)
- [UNET Explanation (YouTube)](https://youtu.be/ng_gAxQnXAY)
- [DETR Architecture (YouTube)](https://youtu.be/xuh37qziXnw)
- [Flutter-Firebase Documentation](https://firebase.google.com/docs/auth/flutter/start)
- [Flask Deployment on AWS](https://youtu.be/uhO2JvOvTWU)

Feel free to modify this `README.md` file to add more details or adjust links as needed!
