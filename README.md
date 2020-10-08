# Sarcasm-Detection

Sarcasm detection from News Headlines websites, this dataset has about 27,000 records. The training will be on the 20,000 records and the rest 7,000 will be used on the testing set.  
The data is loaded from this URL:  https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection. An array of sentences  and an array of labels is created, loading each headline as a sentence and the is sarcastic as the label. The corpus is splited into training and testing set. 

Processing of the dataset:

1. The training sequences is tokenized with hyperparameters the vocaculary size and the out of vocabulary token.
2. The training sequences are padded to the desired length.
3. The same processing is being followed for the tasting sequences.

Architecture of the model:

1. An Embedding Layer embedds the tokenized vocabulary  into the embedding dimension with input length as the max length.
2. A GlobalAveragePooling1D Layer that flattens the output of the embedding layer.
3. A Dense Layer with 24-units and Relu activation function.
4. A Dense Layer with 1-unit and Sigmoid activation .

The model is compiled with binary cross entropy as loss function and adam as optimizer.
The model is trained for 30 epoches for the padded data and labels.
