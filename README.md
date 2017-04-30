# FakeNewsClassifier
Neural net classifier for fake news.

## Data Collection and Cleaning
News_data2.csv contains title, article text, political orientation, veracity, news portal, link, classification, and a lemmatized version of the text. This data was originally used by researchers at Bauhaus-Universität Weimar who were performing stylometric analysis of fake news (https://arxiv.org/pdf/1702.05638.pdf). The data cleaning and csv formatting uses article_data.py.

## Model Training
The multilayer perceptron model is defined in model.py. The training script uses data from news_data2.csv, encodes articles into vocabulary vectors using a simple Bag of Words model. 

## Model Evaluation
Accuracy: 0.79
Precision: 0.06
Recall: 0.13

As you can see by precision and recall scores, the model fails to effectively classify fake news.

## Next Steps
Semantic meaning of the text can be captured using Word2Vec, making it possible to implement a CNN for more accurate classification. Realistically, classifying fake news using the current model doesn't make much sense as much fake news is not defined by word frequencies. Other approaches include cross-checking with independent fact-checking sites and finding inconsistencies within the article itself.


