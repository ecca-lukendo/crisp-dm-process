# Project : CRISP-DM applied to Seattle AirBNB Data

### Description

In this project, I will apply CRISP-DM (Cross Industry Process for Data Mining) to Seattle AirBNB Data.
CRISP-DM consists of 6 steps that I describe hereby.

### Workspace

#### Perequisites 

1. PostgreSQL installed
2. Database "studentdb" with user "student" and password "student" created

All the necessary source code are in Jupyter notebooks. To run this project, you have to run notebooks step-by-step in the following order:

1. data-and-business-understanding.ipynb
2. prepare-date.ipynb
3. model-data-and-results.ipynb

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

#### 5. Results

##### Question 1: What are the busiest times to visit Seattle ?

| month | count |
| ------| ------|  
|  01   | 12073 |
|  02   |  9656 |
|  03   |  8957 | 
|  04   |  9727 | 
|  05   |  9485 |
|  06   |  8962 |
|  07   | 10446 |
|  08   |  9675 | 
|  09   |  8400 | 
|  10   |  8107 |
|  11   |  7290 | 
|  12   |  6884 | 

We can see that January and July are the busiest times to visit Seattle.

##### Question 2 : What are the favorite neighbourhoods ?

| neighbourhood | count |
| --------------| ------|  
|  Belltown     | 28394 |
|  Queen Anne   | 23369 |
|  Minor        | 20597 | 
|  Wallingford  | 15797 | 
|  Ballard      | 15447 |

The 5 favorite neighbourhoods are : Belltown, Queen Anne, Minor, Wallingford, Ballard.

##### Question 3 : By how much can prices spike ?  

| month | price  |
| ------| -------|  
|  01   | 999.00 |
|  02   | 999.00 |
|  03   |  99.00 | 
|  04   |  99.00 | 
|  05   |  99.00 |
|  06   |  99.00 |
|  07   |  99.00 |
|  08   |  99.00 | 
|  09   | 999.00 | 
|  10   | 999.00 |
|  11   | 999.00 | 
|  12   | 999.00 | 

Prices can spike up to $999.00. But the most expensive months do not correspond to the busiest ones.

Step 4 and 5 are in the notebook : <b>model-data-and-results.ipynb</b>







