# Sentiment Classification with BERT and Tokenization

This model performs sentiment classification using the BERT model and tokenization techniques. It can be used to classify multi-class feelings, in this case, it was trained with only two, where 0 represented the inexistence of feelings and 1 the existence of feelings

## Step 1: Importing the libraries

The code starts by importing the necessary libraries, including numpy, re, pandas, BeautifulSoup, seaborn, matplotlib, Google Colab, TensorFlow, and BERT.

## Step 2: Pre-processing

### Database loading

- Performs Google Drive assembly to access the dataset.
- Loads the dataset, performs manipulations and preprocessing, including removing unnecessary columns.

### Additional preprocessing

- Uses the BeautifulSoup library to remove HTML markup from texts.
- Cleans tweets, removing mentions, URLs and unwanted characters.
- Converts sentiment labels to a suitable format.

### Tokenization

- Uses the BERT library to tokenize texts.
- Creates a database with standardized lengths.

## Step 3: Model Construction

Defines a Deep Convolutional Neural Network (DCNN) model with embedding, convolution, max pooling, dense, and dropout layers.

## Step 4: Training

- Compiles and trains the model using the training set.
- Saves checkpoints during training.

## Step 5: Assessment

- Evaluate the model using the test set.
- Displays graphs showing loss and accuracy progression during training.

### Comments

- The DCNN model architecture is configured with specific parameters, such as vocabulary size, embedding dimension, units in dense layers, etc.

- Training is carried out over several seasons, and checkpoints are saved to allow training to be resumed.

- **Important:** The results presented were obtained in training with only 100 batches per epoch due to the extensive data set, which contains approximately 1.3 million tweets. The complete training would take approximately 4 hours or more. It was trained during this period and achieved 89% accuracy.

- There is an observation about potential overfitting, as training with 100 batches showed an accuracy of 95.53%, indicating the need to consider adjustments or techniques to mitigate overfitting.

- If desired, it is possible to use the complete dataset for training, but this will require more processing time.
