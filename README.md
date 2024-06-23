
![Minion](https://github.com/bharathkalyanmuthyala/movies_recommendations_system/blob/master/movie.jpg)

## Introduction
>> The Movie Recommendation System is designed to provide movie recommendations based on various features extracted from the movie and credit datasets. It aims to help users discover movies that match their preferences by analyzing movie characteristics and relationships.



## Data Sets
### Movies Dataset (Movies.csv):
The Movies.csv file contains information about various movies. The columns in this dataset include:
+ **movie_id:** Unique identifier for each movie.
+ **title:** Title of the movie.
+ **overview:** Brief summary of the movie plot.
+ **genres:** List of genres associated with the movie.
+ **keywords:** Keywords related to the movie's content.
+ **cast:** List of main actors in the movie.
+ **crew:** List of crew members involved in the movie production, including the director.

### Credits Dataset (Credits.csv)
The Credits.csv file contains detailed information about the cast and crew of the movies. The columns in this dataset include:

+ **cast:** List of actors and their roles in the movie.
+ **crew:**  List of crew members and their roles in the movie production.
+ **title:** Title of the movie.
> These datasets are merged on the title column to create a comprehensive dataset for the recommendation system.


## Steps
1.**Data Loading:**

+ Load Movies.csv and Credits.csv.
+ Merge the datasets on the title column.
+ Data Cleaning:

2.**Remove null values.**

+ Select relevant columns.
  
3.**Feature Extraction:**

+ Convert stringified lists into actual lists for genres and keywords.
+ Extract genre names and keywords.
  
4.**Text Preprocessing:**

+ Combine selected features into a single tags column.
+ Stem the words in the tags column to their root form.
  
5.**Vectorization:**

+ Uses CountVectorizer from scikit-learn to convert text data into vectors of word counts, limited to the top 5000 words.
+ Convert text data into vectors using CountVectorizer.
  
6.**Similarity Calculation:**

+ Computes cosine similarity between the vectors to determine how similar each movie is to every other movie
+ Compute cosine similarity between movie vectors.
  
7.**Recommendation Function:**

+ Define a function recommend(movie) to recommend movies based on cosine similarity.
  
8.**Serialization:**

+ Serialize the processed data and similarity matrix using pickle.

## Installation

#### To run this project, you need to have the following dependencies installed:

+ python 3.x
+ Jupiter Notebook / Vs code
+ Numpy
+ Pandas
+ ast
+ scikit-learn
+ nltk


### Install Dependencies:

``` bash
import pandas as pd
import numpy as np
import ast
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.metrics.pairwise import cosine_similarity
import pickle
```
  

    
## Usage

1.Clone the repository:
   
   ``` bash
   git clone https://github.com/yourusername/Movie_Recommendation_System.git
   
   ```
2.Navigate to the project directory:

``` bash
cd Movie_Recommendation_System

```
3.Open the Jupyter Notebook:
``` bash
jupyter notebook Movie_Recomendation_System.ipynb
```
4.Run the cells in the notebook to execute the code and see the results.



## Methodology

#### The project involves the following steps:

+ **Importing Libraries:** Import necessary libraries such as pandas and numpy.
+ **Loading Datasets:** Read the movie and credit datasets from CSV files. 
+ **Data Exploration:** Explore the structure and content of the datasets.
+ **Data Cleaning and Processing:** Merge datasets and process data to extract relevant features.
+ **Recommendation Engine:** Implement the logic for recommending movies based on selected features.

## Results

The notebook demonstrates how to build a movie recommendation system by processing and analyzing the datasets. The results include recommendations based on various movie attributes such as genres, keywords, cast, and director.
## Contributing

Contributions are welcome! If you have any suggestions or improvements, please create a pull request or open an issue.


## License

[MIT](https://choosealicense.com/licenses/mit/)

