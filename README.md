# MULTI-VIEW-TEXT-TO-IMAGE-GAN-FOR-CAR-MODEL-GENERATION-FROM-DESCRIPTIONS

## Overview
#### This project implements a Multi-view Text-to-Image Generative Adversarial Network (GAN) capable of generating top, front, and side views of cars from a single descriptive text input. The approach combines advanced rendering techniques, robust text embeddings, and state-of-the-art GAN architecture to bridge the gap between static single-view image generation and computationally expensive 3D modeling.

## Features
-  **Multi-view Image Generation:** Produces top, front, and side views from a single text description.
-  **Self-Attention Mechanisms:** Ensures feature alignment and consistency across generated perspectives.
-  **Semantic Understanding:** Utilizes BERT embeddings for accurate text-to-image mapping.
-  **Lightweight 2D Approximation:** Provides a scalable alternative to 3D modeling for visualization and prototyping.

## Repository Structure
Multi-view-Text-to-Image-GAN-for-Car-Model-Generation/

├── Model Training.ipynb        # Notebook for training the GAN

├── Text To Image Generation.ipynb  # Notebook for inference/generation of images

├── README.md                   # Project description and usage instructions


### Model Training (Model Training.ipynb)

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

### Image Generation (Text To Image Generation.ipynb)

#### Setup:

- Google Drive is mounted.
- Paths for annotations and rendered images are specified.
- Image transformations are defined.

### Text Embeddings:

- Pre-trained BERT tokenizer and model are initialized.
- Helper function to extract embeddings from text.

### Model Definition:

- Custom self-attention module for generators is implemented.
- Separate models for front, side, and top views are defined and initialized.

### Model Loading:

- Pre-trained generator models for each view are loaded from checkpoint files.

### Image Generation:

- Functions for generating front, side, and top view images from text descriptions using the respective generator models.


## Model Architecture
### The GAN consists of:

- **Generators:** Separate view-specific generators conditioned on text embeddings and noise vectors.
- **Discriminators:** Independent discriminators for each view with spectral normalization.
- **Self-Attention:** Incorporated in both generators and discriminators to capture global dependencies.

### Loss functions:

- Wasserstein Loss with Gradient Penalty (WGAN-GP): Stabilizes training.
- Alignment Loss: Ensures semantic coherence across views.

## Limitations
- Resolution: Currently limited to 128x128 pixels.
- Training Data: Performance depends on the diversity and size of the dataset.
- Computational Requirements: Training requires significant GPU resources.

## Authors
- Naga Venkata Vignesh Reddy Upputuri (nupputuri@uh.edu)
- Vasista Tummala (vtummala3@uh.edu)
#### University of Houston


