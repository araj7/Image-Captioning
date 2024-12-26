# Image Captioning

## Overview
The **Image Captioning** program is designed to generate descriptive captions for input images. It uses an Encoder-Decoder architecture, combining computer vision and natural language processing techniques. By feeding image tensors and accompanying descriptions into the network during training, the program learns to predict captions for unseen images. 

This approach is a simplified yet effective method for building a vision-and-language model that encodes images and decodes their descriptions using recurrent neural networks (RNN).

---

## Dataset
The program uses the **Flickr8k** dataset, which can be accessed [here](https://www.kaggle.com/adityajn105/flickr8k/activity).

---

## Workflow
### **1. Data Preprocessing**
- **Description Cleaning**: Preprocess the `train_test_descriptions` by normalizing and cleaning the text data.
- **Image Transformation**:
  - Resize images.
  - Convert images to tensors.
  - Normalize pixel values for consistent input representation.
- **Vocabulary Creation**:
  - Build a vocabulary from image descriptions.
  - Use the `FreqDist` function to identify word frequencies.
  - Exclude words appearing fewer than 5 times.
  - Assign unique numbers to each vocabulary word.

### **2. Data Preparation**
- Determine the maximum description length in the dataset.
- Create a main vocabulary mapping (including special start and end tags).
- Load images from the specified directory into the variable `imgg`.
- Define a data loader class to handle images and captions.

### **3. Model Architecture**
#### **Encoder**:
- Uses a pre-trained **ResNet-18** model for feature extraction.

#### **Decoder**:
- Implements an RNN-based decoder to generate captions from image embeddings and input sequences.

### **4. Training**
- Initialize components:
  - Encoder.
  - Embedding size.
  - Hidden size.
  - Loss criterion.
  - Optimizer.
- Train the model over multiple epochs using a custom training function.

### **5. Testing**
- Use the trained model to generate captions for new images.

---

## Steps to Run the Program
> **Note**: Ensure to execute the code sequentially to avoid errors.

1. Preprocess the descriptions.
2. Transform images by resizing and normalizing them.
3. Build and refine the vocabulary.
4. Load images and descriptions into the data loader.
5. Define and initialize the encoder and decoder models.
6. Train the models using the provided training function.
7. Use the testing function to generate captions for input images.

---

## Key Features
- **Simplified Encoder-Decoder Pipeline**:
  - Combines ResNet for image encoding and RNN for caption generation.
- **Efficient Vocabulary Management**:
  - Filters out low-frequency words to improve model focus and reduce computational complexity.
- **Custom Training and Testing Functions**:
  - Fine-tune the model over epochs.
  - Generate human-like captions for test images.

---

## Tools & Libraries
- **Python**: Programming language for implementation.
- **PyTorch**: Deep learning framework for model building and training.
- **Pandas & NumPy**: For data manipulation and preprocessing.
- **Matplotlib**: For visualizing results.

---

## Future Enhancements
- Experiment with advanced architectures like Transformer-based models (e.g., Vision Transformers).
- Expand dataset usage for improved generalization.
- Implement Beam Search for more accurate caption generation.
- Enhance preprocessing by incorporating lemmatization and stemming.

---

## Author
This project was developed by **Amit Raj** to explore the intersection of computer vision and natural language processing through image captioning.

---
