# Sentiment Analysis on Moroccan Arabic Dialect

## Project Overview

This project focuses on sentiment analysis for the Moroccan Arabic dialect using deep learning techniques. The model architecture includes fine-tuned Word2Vec embeddings, trained alongside the model, and a Bidirectional LSTM layer. The model aims to predict sentiment in Arabic text, distinguishing between positive and negative sentiments.

## Model Architecture

The architecture of the sentiment analysis model involves the following key components:

1. **Word Embeddings:**
   - Utilizes Word2Vec embeddings with a vector size of 100.
   - The embeddings are fine-tuned during training on the sentiment analysis dataset.

2. **Bidirectional LSTM:**
   - Employs a Bidirectional Long Short-Term Memory (LSTM) layer with 200 units.
   - Enhances the model's ability to capture contextual information from both past and future time steps.

3. **Flatten, Dense, and Dropout Layers:**
   - Includes a Flatten layer to transform the LSTM output into a 1D array.
   - Adds a Dense layer with 200 units and ReLU activation function.
   - Incorporates a Dropout layer with a dropout rate of 0.5 to prevent overfitting.

4. **Output Layer:**
   - Utilizes a Dense layer with a single unit and a sigmoid activation function for binary classification.

## Model Training Results

The model was trained for 5 epochs with a batch size of 64. The training results are as follows:

- **Training Accuracy:** 98.18%
- **Validation Loss:** 1.4093
- **Validation Accuracy:** 79.17%

## Sample Predictions

The model was tested on several sample sentences with the following sentiment predictions:

1. **لقد كان يومًا رائعًا : [1.]** (Positive)
2. **أنا حزين جدًا : [1.]** (Positive)
3. **لقد فزت بالمباراة : [1.]** (Positive)
4. **لقد خسرت وظيفتي : [1.]** (Positive)
5. **لقد تخرجت من الجامعة : [1.]** (Positive)
6. **لقد تزوجت : [1.]** (Positive)
7. **لقد أنجبت طفلًا : [1.]** (Positive)
8. **لقد مات والدي : [0.]** (Negative)
9. **لقد انتقلت إلى منزل جديد : [1.]** (Positive)

The model seems to perform well on these sample sentences, correctly identifying positive sentiments in most cases. However, it may encounter challenges with nuanced expressions, and continuous refinement could further enhance its accuracy.

## Dependencies

Ensure you have the required Python libraries installed:

```bash
pip install numpy gensim scikit-learn keras pandas nltk
```

Feel free to explore and modify the notebook based on your specific needs and dataset characteristics.
