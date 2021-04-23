# wikipiifed - Automated dataset creation and Federted learning


This repo represent the automated dataset creation from [wikipedia biography pages](https://en.wikipedia.org/wiki/Category:Living_people) and utilizing the dataset for Federated learning of BERT based Named entity recognizer.


## Running scraper and creating the dataset

[wikipii_dataset.ipynb](https://github.com/ratmcu/wikipiifed/blob/master/wikipii_dataset.ipynb) is a walk through of the dataset creation. 

Sequence of dataset creation is:

1. gathering all the links of living people from Wikipedia
2. scoring the pages based on the presense of named entities hence filtering
3. starting parallel workers to scrape and create csv and text files with infobox data and scraped text 
4. splitting the dataset to test/train/validation sets based on the entity presense score

## Running federated training

[remote_bert.ipynb](https://github.com/ratmcu/wikipiifed/blob/master/remote_bert.ipynb) walks through the training of the BERT-base model on the dataset with two remote workers.

notebook can be tested in the colab. 

After running the Installing PySyft code block colab has to be restarted and the remaining cells can be executed. 

Notebook has following sections:

1. Dataset Class - class for loading the dataset from text files
2. BERT Model - Modified version of Huggingface BERT-base and class for the final model
3. Data Iterators - loading training/test/evaluation sets from files to dataset objects
4. Training - loading model, distributing dataset to remote workers and federated training






[![Foo](https://avatars1.githubusercontent.com/u/6571379?s=200&v=4 )](http://imrsv.ai/)
[![Foo](https://d9hhrg4mnvzow.cloudfront.net/discover.mitacs.ca/innovationroi/1qoj9ta-mitacs-transparent_07w02d000000000000001.png)](https://www.mitacs.ca/en)
