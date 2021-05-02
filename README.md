# Overview of Project:

An analytical exploration more focus toward tech-industry of the connection between mental health and economics status in The US. As today, mental illness affect millions of adults in the United States.
 

### Reason:
Many of us have battled with depression and anxiety issues for most of our lives. We are intimately aware of how these issues can be exacerbated by as well as lead to financial hardships. We wanted to further explore the statistics and numbers underpinning this relationship.

### Data Source:
We source our data from kaggle more specifically datasets including surveys focusing on individual working in tech-company from 2014 to 2021.<br>
[Visit](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment/resources) our resources.

### Team Members : 
- Art Tucker : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/tucker_a_branch_01) 
- Preeti Suryakumar : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/preeti-01)
- Radhika Tippana : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/rtippana_segment_2)
- Sylvain Dessagnes : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment)
- Victoria Morales : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/morales_v_branch)
- Danielle Stauffer : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/Stauffer_Branch)

### Machine learning model:

Our goal is to predict an output from a previous experience, to achieve this goal, we will use supervised machine learning model.<br>
This kind of model allow us to use training data to learn a link between the input, and the output. Compared to unsupervised learning, it is a more accurate and trustworthy method.<br>
- Datasource: [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/resources/clean_data/clean_dataset_2016.csv)
<br>
  
To start off we pre-process our data, make sure the values in the columns are consistent [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/notebook/cleaning_dataset_2016.ipynb). Our interest here is to focus on individual who work in a tech-company.<br> 
Then we encode the dataset using a label encoder.
As now, we try to predict two different target:
1) Can we predict if an individual is more susceptible to get a leave from work if there is suspicion or confirmation of mental health issue.
[Script.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/machine_learning/machine_learning_test1.ipynb)

**Target**: If a mental health issue prompted you to request a medical leave from work, asking for that leave would be?
We reduce the data values in the leave columns to 3.(easy/difficult/neither easy nor difficult)
<br>
Our decision-making process for this selection was to find information related to mental health who can help predict the need for a work leave due to mental illness.
<br>   
To train and test our dataset, we use demographics information features (age/gender/place of habitation and work), information on current and past employer(provide or not mental health insurance plan, anonymity respected in case of mental illness issue), and also some information about individual mental health status(diagnose with mental illness or treated by a professional, currently and in the past, family history)

   
2) Can we predict if an individual is diagnosed with mental illness.
[Script.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/machine_learning/machine_learning_test2.ipynb)

**Target**: Do you currently have a mental health disorder?
<br>
**Features**: We use demographics information(age/gender/place of habitation), as well as facts on current and previous employer(mental health coverage plan, sensitisation towards mental illness in the company, anonymity preserved) and also insight on previous mental illness.    
<br>

For both model, we decide to split our entry data into 75% for training set and 25% testing set, because any train-test split which has more data in the training set will most likely give you better accuracy as calculated on that test set. like that the training dataset for the model can learn and effectively map input to output. 
When splitting the dataset, we stratify it so that each split is similar. In a classification setting, it is often chosen to ensure that the train and test sets have approximately the same percentage of samples of each target class as the complete set.
<br>
As now, we are using a Random Forest Classifier because of his versatility, it can be used for both classifications and regression task. It provides higher accuracy through cross validation. Compared to simple decisions trees, instead of searching for the most important feature while splitting a node, it searches for the best feature among a random subset of features.
<br>
<br>
**Benefits**:
- Robust to outliers.
- Works well with non-linear data.
- Lower risk of over-fitting.
- Better accuracy than other classification algorithms.

**Limitations**:
- The main limitation of random forest is that many trees can make the algorithm too slow and ineffective for real-time predictions.

In addition, we pursue our machine learning exploratory by using an Oversampling and Undersampling algorithm.
<br>
Oversampling is capable of improving resolution and signal-to-noise ratio, and can be helpful in avoiding aliasing and phase distortion by relaxing anti-aliasing filter performance requirements but this method can result in overfitting for some models due to duplicates examples from the minority class in the training dataset.
So far Oversampling look better because we keep all the information in the training dataset. With undersampling we drop a lot of information. Even if this dropped information belongs to the majority class, it is useful information for a modeling algorithm.


### Database:

For our project we use an SQL database, more specifically Postgres and pgadmin to interact with it. In our case, knowing that we are not going to work with a huge volumes of data, there are more advantages for us to use a relational database management system.

For example:
- Data structure.
- Easy access to the network.
- Language (MySQL).
- Speed.
- Maintenance.
- Ability to be access by more than one person.

Using python package sqlalchemy, and the needed modules (create_engine/session) we build a database with our selected data and are able to preprocess it using python/pandas and then upload it into our database **Final_project_mental_health**, as well as imported it from the database into any python script we are working on.
We also can directly query the database in our pandas jupyter notebook using SQL code.
<br>
[Checkout](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_connection.ipynb) our *database_connection* script.
Running this script will update any changes applied to our datasets on the database tables.
Each team member have the database on his local server with up-to-date data inside. We also will deploy our database on AWS server for all around access from our team.
<br>
Entity Relational Diagram [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_ERD.png)
<br>
SQL code for database creation [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_creation_SQL)
<br>
Ongoing database work [here.](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment/database)
### Dashboard:

Click [here]() to review our ongoing story.