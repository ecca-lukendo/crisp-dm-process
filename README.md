# Project : CRISP-DM applied to Seattle AirBNB Data

### Description

In this project, I will apply CRISP-DM (Cross Industry Process for Data Mining) to Seattle AirBNB Data.
CRISP-DM consists of 6 steps that I describe hereby.

#### Content

1° data : repository with our dataset
2° data-and-business-understanding.ipynb : notebook used to explore data
3° prepare-date.ipynb : notebook showing how to import and prepare data for 
4° model-data-and-results.ipynb: notebook explainig the model we used in this project and the results
5° LICENSE
6° README.md

### Workspace

#### Perequisites 

1. PostgreSQL installed
2. Database "studentdb" with user "student" and password "student" created

#### Running

All the necessary source code are in Jupyter notebooks. To run this project, you have to run notebooks step-by-step in the following order:

1° data-and-business-understanding.ipynb
2° prepare-data.ipynb
3° model-data-and-results.ipynb

The dataset is under the repository <b>/data</b>

### CRISP-DM

#### 1. Business Understanding

By looking at the data, here are some questions that come up:

1. What are the busiest times to visit Seattle?
2. What are the favorite neighbourhoods ?
3. By how much can prices spike ? 

#### 2. Data Understanding

In this step, I try to figure out what are the important features.

Here are some important variables for each file:

1. <b>listings.csv : id, neighbourhood, room_type</b>
2. <b>calendar.csv : listing_id, date, available and price</b>
3. <b>reviews.csv : listing_id, date, comments</b>

Step 1 and 2 are in the notebook : <b>data-and-business-understanding.ipynb</b>

#### 3. Prepare Data

In other to make data quering easy, I transfer my data from csv files to PostgreSQL database. It will then be more eaisier for me to query my data and to answer the three questions.

In this step, I create a database called "studentdb" with 3 tables :

1. <b>listings (id, neighbourhood, room_type)</b>
2. <b>calendar (listing_id, date, available, price)</b>
3. <b>reviews (listing_id, date, comments)</b>

During this data preparation, I am going also to remove NAN values from listings['id','neighbourhood'] columns.

Step 3 is in the notebook : <b>prepare-date.ipynb</b>


#### 4. Model Data

In this step, we are going to query our database in other to answer our three questions:

1. What are the busiest times to visit Seattle?
2. What are the favorite neighbourhoods ?
3. By how much can prices spike ? 


Step 4 and results are in the notebook : <b>model-data-and-results.ipynb</b>







