# Analyzing Sentiment of Product Reviews (v 1.0)


User reviews surely play an important role for making decisions for customers whether to buy the product or not which impacts the overall sale of the platform. Owners of those platforms can analyze this review to improve their products. Here I proposed an approach which will help to do sentiment analysis of amazon product reviews. I used TF-ID features extraction technique to get the features from the text data. For classification I used Naıve bayes, KNN, Linear SVC and XGBoost. To reduce the computation time and memory I used the chi-square feature selection  technique which helped to reduce the computation time significantly.


![social](https://img.shields.io/github/followers/trevortomesh?style=social)![twitter](https://img.shields.io/twitter/follow/trevortomesh?style=social)![languages](https://img.shields.io/github/languages/count/craftsbyshuvro/research-methods-class)


## Table of Contents

1. [Manifest](#manifest)
2. [Project Architectural Overview](#project-architectural-overview)
3. [Installation Instruction](#installation-instruction)
4. [Roadmap](#roadmap)
5. [Project Status](#project-status)
6. [How to contribute](#how-to-contribute)
7. [License](#license)
8. [Contact](#contact)
8. [Acknowledgements](#acknowledgements)


## Manifest

- Here are list of top files from this project

```
- /src/01.Preporcessing.ipynb --> This file is responsible for preprocessing the dataset
- /src/02.Classification.ipynb --> This file
- /src/data --> Here you can keep the dataset after downloading (Follow Installation Instruction)
- img ----------> Images folder for the readme
```

## Project Architectural Overview
<img src="img/SentimentAnalysisModelArchitecture.JPG" alt="drawing" width="450"/>

## Installation Instruction
To run the program follow below instructions.

- Download the dataset and place into src directory. [Download Dataset Here](https://www.kaggle.com/datafiniti/consumer-reviews-of-amazon-products/download)
- Set path to the following variables in this file [01.Preporcessing.ipynb](src/01.Preporcessing.ipynb)
You will find those files after downloading the whole dataset


   ```py
data1_path = '/consumer-reviews-of-amazon-products/1429_1.csv'
data2_path = "/consumer-reviews-of-amazon-products/Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv"
data3_path = "/consumer-reviews-of-amazon-products/Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products.csv"
```
- Run all the cells of this file [01.Preporcessing.ipynb](src/01.Preporcessing.ipynb)
This will export a file named `preprocessed-dataset.csv`  after doing necessary preprocessing. Preprocessing steps includes
    - Data Cleaning
    -Removing Link
    -Remove Tags
    -Removing Stop Word
    -Stemming

- Then run all the cell of this file [02.Classification.ipynb](src/02.Classification.ipynb)
This will use the preprocessed data from `preprocessed-dataset.csv` for further processing
    - It will vectorize the data using TF-IDF
    - It will oversample the dataset to balance the dataset
    - Split the whole dataset in 80:20 ratio which will be used for Training and Testing
    - It will use GridSearch with 5-Fold Cross validation to finetune the hyperparameters of the classifiers
    - At last it will evaluate the model with Test dataset and output the Training Time, Accuray, Precision, Recall & F1-Score


## Roadmap
There are few things i would like to address in future.
- I shall perform cross domain testing on this trained model
- I shall train model with large number of review data from various categories of product
- I have desire to do the Sentiment Analysis using Deep Learning technique (e.g. CNN, LSTM)
If you have other cool ideas regarding this, let me know also.


## Project Status
I am still working on this to improve the model. I am following the **Road-map** mentioned above

## How to contribute
 Any kind of feedback on this is greatly appritiated. I shall be more than happy to have any pull request from smart people like you.
 

## License
Distributed under the MIT License. See [LICENSE](LICENSE.md) file for more information.

## Contact
- For any kind of help or support. Feel free to knock me.
- Contact: <a href = "mailto: mali23@lakeheadu.ca">Send Email</a>


## Acknowledgements
Till now i am the only person who contributed in this project. If you are interested to join me. Fell free to knock me. <a href = "mailto: mali23@lakeheadu.ca">Email</a>

Here are few references from where i got inspired to make such project.
