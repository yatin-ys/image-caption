# Image Caption Generation
This repository contains a deep learning project to generating image captions using a combined Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) architecture. The aim is to automatically generate descriptive captions for images, enhancing the understanding of the visual content.

## Dataset
Flickr30k dataset, a diverse collection of images paired with human-generated captions. This dataset enables the training and evaluation of the image caption generator, facilitating the learning of meaningful relationships between images and their corresponding textual descriptions.

Link - https://www.kaggle.com/datasets/hsankesara/flickr-image-dataset

## Method

1. Image Feature Extraction - We use the VGG16 model to derive image features
2. Caption Preprocessing - involves converting to lowercase, removing non-alphabetic characters, adding start and end tokens, tokenizing for numerical conversion, determining vocabulary size and calculating max caption length
3. Model Implementation
   - CNN Encoder - CNN that takes in an input image and extracts high-level features from it. These features are then transformed into a fixed-length vector representation
   - RNN Decoder - It takes the fixed length vector representation from the CNN and generates a sequence of words one at a time to form a coherent caption. At each step, the RNN generates the next word based on its previous output and a hidden state that maintains context.
4. Generate Captions

## Result
BLEU Score:
- BLEU-1 - 0.623424
- BLEU-2 - 0.412801
