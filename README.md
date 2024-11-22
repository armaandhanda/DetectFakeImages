# Objective
The objective of this project is to detect fake images by leveraging multi-modal data (images and text captions). A multi-modal GAN-based approach was used to combine features from images and text for robust classification in a noisy, real-world dataset.


# Key Highlights
Multi-Modal GAN Architecture:

Integrated both image and text modalities to enhance detection capabilities.
Used EfficientNetB0 as the backbone for extracting image features.
Processed captions using a TextVectorization layer and embedding layers for text features.
Fine-Tuning:

Fine-tuned the last 5 layers of the EfficientNet backbone to optimize feature extraction for this task.
Added L2 regularization and dropout layers to reduce overfitting.
Binary Classification Pipeline:

Combined image features and caption embeddings into a single vector.
Added dense layers with activation functions to classify fake vs. real data.
Robust Dataset Handling:

Designed a custom mapping function to process datasets into the expected format for training.
Utilized map functions to seamlessly integrate paired datasets of images and captions.
Tools and Frameworks
Python: Programming language for building and training the model.
TensorFlow/Keras: Deep learning framework for model architecture and training.
Hugging Face Transformers: Used for embedding text features.
EfficientNetB0: Pre-trained backbone for image feature extraction.
How to Use
Setup Environment:

Ensure Python 3.x and TensorFlow 2.x are installed.
Install required libraries:
bash
Copy code
pip install tensorflow numpy
Prepare Dataset:

The dataset should include paired inputs:
Two images: Representing real and potentially fake content.
Captions: Associated text information.
Use a preprocessing pipeline to create `train_paired_dat


