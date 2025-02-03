
# Named Entity Recognition (NER) for Text Classification

## Business Problem

The primary goal of this project is to apply Named Entity Recognition (NER) to identify and extract important entities from unstructured text. NER can be used across various industries to automate the extraction of meaningful information such as names, dates, locations, organizations, and more. 

In healthcare, for example, NER can help extract patient names, diagnoses, medical conditions, and treatments from medical records or doctors' notes, ultimately improving operational efficiency and decision-making. In the financial sector, NER can be used to identify company names, transaction details, and other key financial entities from reports, invoices, and documents. 

By automating this process, businesses can unlock insights from large volumes of text data without manual intervention, saving time and reducing human error.

## Project Overview

In this project, a deep learning model has been built to perform Named Entity Recognition (NER) using the Keras framework with TensorFlow backend. The model is based on a Bidirectional Long Short-Term Memory (Bi-LSTM) architecture with a TimeDistributed Dense layer to predict entity tags for each token in a sentence. The model is trained on padded sentence data and a target set of entity tags.

### Why This Project?

This project was created to:
1. **Automate Data Extraction**: Automatically extract relevant entities from text data, reducing the need for manual annotation.
2. **Improve Efficiency**: By leveraging machine learning, businesses can process large amounts of unstructured data more efficiently.
3. **Generalize to Various Applications**: The trained model can be applied to various domains such as healthcare, finance, and legal, where extracting entities from text is crucial for decision-making.

### Key Features:
- **Deep Learning Model**: Utilizes a Bidirectional LSTM network to learn dependencies in the text both forward and backward, making it ideal for sequential data.
- **TimeDistributed Layer**: Allows the model to make predictions for each token in a sentence.
- **Data Preprocessing**: Text data is tokenized and padded to ensure uniform input size for the model.
- **Model Evaluation**: The model's performance is evaluated using accuracy on a validation set, ensuring its effectiveness in real-world applications.

## Model Architecture

The model consists of:
1. **Embedding Layer**: Embeds input tokens into a 32-dimensional vector space.
2. **Bidirectional LSTM Layer**: A Bi-LSTM layer with 128 units, which processes the sequence data from both directions.
3. **TimeDistributed Dense Layer**: A dense layer applied to each token in the sequence, producing one of the 17 possible tags.
4. **Softmax Activation**: Applied at the output to predict the class (tag) of each token in the sequence.

### Training and Evaluation
- The model is trained using the categorical cross-entropy loss function and the Adam optimizer.
- Early stopping is implemented to prevent overfitting, with the best model being saved during training.
- The model is evaluated on a test set to predict entity tags for unseen sentences.

## Data and Preprocessing

- **Input Data**: Padded and encoded sentences.
- **Target Data**: One-hot encoded labels for each token in the sentence.
- **Validation and Test Sets**: The dataset is split into training, validation, and test sets to ensure that the model generalizes well.

## Use Cases and Applications

This NER model can be applied in a wide range of scenarios:
- **Healthcare**: Extract medical terms, patient names, diagnoses, and treatments from unstructured clinical text or patient records.
- **Finance**: Identify transaction details, company names, financial terms, and other entities from financial documents and reports.
- **Legal**: Extract case names, legal terms, and other relevant entities from legal documents, contracts, or case reports.
- **Customer Support**: Automatically identify key pieces of information from customer queries, such as product names, issues, and dates, to streamline customer support workflows.

## How to Run the Project

1. **Clone the repository**:
   ```bash
   git clone <repository_url>
   cd <repository_directory>

