# MULTI-VIEW-TEXT-TO-IMAGE-GAN-FOR-CAR-MODEL-GENERATION-FROM-DESCRIPTIONS

## Overview
#### This project implements a Multi-view Text-to-Image Generative Adversarial Network (GAN) capable of generating top, front, and side views of cars from a single descriptive text input. The approach combines advanced rendering techniques, robust text embeddings, and state-of-the-art GAN architecture to bridge the gap between static single-view image generation and computationally expensive 3D modeling.

## Features
-  **Multi-view Image Generation:** Produces top, front, and side views from a single text description.
-  **Self-Attention Mechanisms:** Ensures feature alignment and consistency across generated perspectives.
-  **Semantic Understanding:** Utilizes BERT embeddings for accurate text-to-image mapping.
-  **Lightweight 2D Approximation:** Provides a scalable alternative to 3D modeling for visualization and prototyping.

## Structure
### 📁 main/ 
### Model Training.ipynb

#### Setup:
- Google Drive is mounted.
- Paths for annotations and rendered images are specified.
- Image transformations are defined.

#### **Text Embeddings:**
- Pre-trained BERT tokenizer and model are initialized.
- Helper function to extract embeddings from text.

#### **Model Definition:**

- Custom self-attention module for generators is implemented.
- Separate models for front, side, and top views are defined and initialized.

#### **Model Loading:**

- Pre-trained generator models for each view are loaded from checkpoint files.

#### **Image Generation:**

- Functions for generating front, side, and top view images from text descriptions using the respective generator models.

### Text To Image Generation.ipynb
###