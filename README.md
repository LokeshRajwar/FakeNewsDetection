# Fake News Detection
The latest hot topic in the news is fake news and many are wondering what data scientists can do to detect it and stymie its viral spread. This dataset is only a first step in understanding and tackling this problem.

__Original Dataset__  
The data source used for this project is dataset which contains 3 files with .tsv format for test, train and validation. Below is some description about the data files used for this project.

- Column 1: the ID of the statement ([ID].json).  
- Column 2: the label. (Label class contains: True, Mostly-true, Half-true, Barely-true, FALSE, Pants-fire)  
- Column 3: the statement.  
- Column 4: the subject(s).  
- Column 5: the speaker.  
- Column 6: the speaker's job title.  
- Column 7: the state info.  
- Column 8: the party affiliation.  
- Column 9-13: the total credit history count, including the current statement.  
- Column 9: barely true counts.  
- Column 10: false counts.  
- 11: half true counts.  
- 12: mostly true counts.  
- 13: pants on fire counts.  
- Column 14: the context (venue / location of the speech or statement).

__Prerequisites__    
- Python3.6  
- Sklearn  
- Numpy  
- Pandas  
- Scipy  
- NLTK  
- Matplotlib  

__Moulded Dataset__ 
The given Data Contains some useless columns. Following are the coloumns that are Useless for our Problem statement and are droppped from the dataframe.
1. Drop Useless Columns,  
        i. Sno  
        ii. barely_true_count  
        iii. false_counts  
        iv. half_true_counts  
        v. mostly_true_counts  
        vi. pants_on_fire_counts    
2. You will see that newly created dataset has only 2 classes as compared to 6 from original classes. Below is method used for reducing the number of classes.

       Previous-Label    :    Converted-Label  
         True           --        True  
         Mostly-true    --        True  
         Half-true      --        True  
         Barely-true    --        False  
         False          --        False  
         Pants-fire     --        False
- The Dataset Folder contains the Original data and the train_data.csv, test_data.csv, valid_data.csv are the cleaned and dropped datasets.
         
__Screenshot of CountPlot__  
Following Screenshots contains the Count plot of labels of the Following Data set available  in the repo. 

1. Training Data set  


![image](https://user-images.githubusercontent.com/34310411/51328366-3d2a1f80-1a99-11e9-876a-4a574b016b93.png)

2. Testing Data set  

![image](https://user-images.githubusercontent.com/34310411/51328400-4fa45900-1a99-11e9-86ca-5da36a19711c.png)


3. Validation Data set  


![image](https://user-images.githubusercontent.com/34310411/51328441-65b21980-1a99-11e9-975c-7411b7771b6f.png)


### Model Used : LSTM  
LSTM is a recurrent neural network (RNN) architecture that REMEMBERS values over arbitrary intervals. LSTM is well-suited to classify, process and predict time series given time lags of unknown duration. Relative insensitivity to gap length gives an advantage to LSTM over alternative RNNs, hidden Markov models and other sequence learning methods.

### *Architecture*

![model_lstm](https://user-images.githubusercontent.com/34310411/53307310-0d9edc00-38bd-11e9-9bef-dc773093a991.png)


### Model Summary

![image](https://user-images.githubusercontent.com/34310411/53307405-2d82cf80-38be-11e9-8cb8-1fa7a738fa4b.png)

- __Statistics while First Epoch__

![image](https://user-images.githubusercontent.com/34310411/53307450-cb769a00-38be-11e9-98b4-beee9a1df7f2.png)

- __Statistics while Last Epoch__

![image](https://user-images.githubusercontent.com/34310411/53307455-e0532d80-38be-11e9-9677-ca0fe51c4ff3.png)





### Results

![image](https://user-images.githubusercontent.com/34310411/53307486-17294380-38bf-11e9-8223-47711aee114f.png)


### Project by : Lokesh Singh Rajwar  
### Mentor : Sushant Chamoli (Faculty)
