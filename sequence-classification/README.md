### IMDB Movie Review Sentiment Analysis

This project focuses on building a sentiment analysis model to classify movie reviews from the **IMDB Dataset** as either **positive** or **negative**. The dataset consists of 50,000 movie reviews, evenly split between positive and negative sentiments. The model has achieved **97% accuracy** on the test dataset, demonstrating its effectiveness in understanding the sentiment of movie reviews.

### Key Features:
- **Dataset**: IMDB Movie Reviews (50,000 labeled reviews)
- **Model Architecture**: 
  - Embedding layer for text representation
  - Stacked LSTM layers to capture sequential information in the reviews
  - Fully connected layers with sigmoid activation for binary classification
- **Preprocessing**:
  - Lowercasing of text
  - HTML tag removal using BeautifulSoup
  - Removal of non-alphabetic characters
  - Tokenization using NLTK
  - Lemmatization and stopword removal
- **Accuracy**: 97% on the test set

### Model Pipeline:
1. **Data Preprocessing**:
   - Reviews are preprocessed by converting text to lowercase, stripping HTML tags, and removing unwanted characters.
   - Tokenization and lemmatization are applied, and stopwords are removed to focus on meaningful words.
   - A vocabulary is created from the training data, and words are mapped to indices for embedding.

2. **Model**:
   - A **LSTM-based neural network** is used to process sequences of word embeddings.
   - The LSTM layers capture contextual relationships between words in a review.
   - A fully connected layer outputs a probability score, which is passed through a sigmoid function to classify reviews as either **positive** or **negative**.

3. **Training**:
   - The model is trained using **binary cross-entropy loss** and the **Adam optimizer**.
   - Dropout is applied between layers to prevent overfitting.
   - The model is evaluated on the test set, achieving 97% accuracy.


### Results:
- The model achieves **97% accuracy** on the test dataset, showcasing its effectiveness in movie review sentiment analysis.

### Downloading the Trained Model
The trained model parameters are available for download:
- **Download Link**: [Trained Model](https://drive.google.com/file/d/1aJmbvp-ORqBvQEkkJLqQrrovKlc3k6B0/view?usp=sharing)

### Future Improvements:
- Experimenting with **pre-trained word embeddings** like GloVe or BERT for better text representation.
- Implementing **Bi-LSTM** to capture context from both directions in the text.
- Fine-tuning hyperparameters like learning rate, dropout, and LSTM hidden sizes.

This model can be further optimized or adapted for other text classification tasks by altering the architecture or the dataset.
