# how_do_you_feel_my_dear
NLP project for Text Mining and Sentiment Analysis.

Recently, **emotion detection** in text has received attention in the literature on **sentiment analysis**. Detecting emotions is important for studying **human communication in different domains**, including fictional scripts for TV series and movies. The project aims at studying fictional scripts of several movies and TV series under the emotional profile. In particular, the task of the project is threefold:

1. Create a model to predict emotions in text using available datasets as WASSA-2017 in which emotions are represented as categorical classes;
2. Exploit the model to study an emotional profile of the main characters in one of the movies included in the Cornell Movie--Dialogs Corpus;
3. Study how this emotional profile changes in time along the evolution of the movie story and how it is affected by the various relations among the different characters.

## First model attempts
In the notebook named [**text_mining_starting_point.ipynb**](/text_mining_starting_point.ipynb) you can fetch the data from the WASSA-2017 website, make some initial preprocessing cleaning up the textual documents and make some attempts in models architectures. Data are then saved into the folder named **emotions**.

## Model Selection with few parameters
In the notebook named [**text_mining_model_selection.ipynb**](/text_mining_model_selection.ipynb) you can make a model selection tuning few hyper-parameters, then cross-validating the accuracy of the model.

## Full Model Selection on colab
In the notebook named [**text_mining_model_selection-colab.ipynb**](/text_mining_model_selection-colab.ipynb) you can make a full model selection tuning more hyper-parameters, then cross-validating the accuracy of the model. Then the model architecture and weights learnt are saved into the folder **final_model**. If you want to execute in a 5x times faster press the colab button below and select the **GPU** in the colab runtime.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16TOIflO9CPvh8WMYQRDCKT6dZ43PHoPM?usp=sharing)

## Tokenizer fitted on sequences saved
In the folder named [**tokenizer**](/tokenizer) you can find 2 notebooks in which it has been saved and tested the **Keras Tokenizer**. Since The tokenizer instance needs to be fitted on texts, It has been saved the one fitted on the texts used for the model training. If you use the same tokenizer fitted on different texts it could be risky, reaching different results. Its has been then tested on test data with the model saved and It works well.
Now it is all ready for the application of the model in the **movie characters emotion detection**.

## Preprocess the movie utterances
From the Cornell Movie-Dialogs Corpus data (https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html) it has been selected the movie: **The Godfather** (_1972 - Mario Puzo, Francis Ford Coppola_). You can find the preprocessing and utterances extraction from the conversations of the movie selected in the notebook renamed [**text_mining_preprocess_movie_data.ipynb**](/text_mining_preprocess_movie_data.ipynb), and also find the final dataset saved with the texts and the characters associated. A further selection has been done on the **main chacarters**: _Don Corleone, Tom Hagen, Michael Corleone, Peter Clemenza and Sonny Corleone_.

## Predictions done on the _Godfather_ Characters
Once taken the **tokenizer** and the **model already trained**, can be done the **predictions** of the **emotions** from dialogues of the film choosen and the characters selected. See the notebook renamed [**text_mining_godfather_emotions_predictions.ipynb**](/text_mining_godfather_emotions_predictions.ipynb). Then the dataset with the predictions done is saved in another _.csv_ file named: **godfather_emotions.csv**.

## Analysis of the emotional profile of _Godfather_ main characters
In the notebook named [**text_mining_godfather_emotions_analysis.ipynb**](/text_mining_godfather_emotions_analysis.ipynb) it is studied how this emotional profile changes in time along the evolution of the movie story and how it is affected by the various relations among the different characters. In particular it is created a dataframe with couple of speaker and respondent dialogues, and they are analysed the **sentiments of the speakers conditional on the respondents**.
