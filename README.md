# Mental Health and Economics

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

Our goal is to predict an output from a previous experience, to achieve this goal, we will use a supervised machine learning model.<br>
This kind of model allow us to use training data to learn a link between the input, and the output. Compared to unsupervised learning, it is a more accurate and trustworthy method.<br>
- Datasource[Link.](https://github.com/ArtTucker/mental_health_and_economics/blob/main/database/filestoload/2016_surveydata.csv)
<br>
  
To start off we pre-process our data, make sure the values in the columns are consistent. Our interest here is to focus on individual who work in a tech-company.<br> 
Then we encode the dataset using a label encoder.
As now, we try to predict three different target:
1) Can we predict if an individual is more susceptible to get a leave from work if there is suspicion or confirmation of mental health issue.


**Target**: If a mental health issue prompted you to request a medical leave from work, asking for that leave would be?
We reduce the data values in the leave columns to 3.(easy/difficult/neither easy nor difficult)
<br>
Our decision-making process for this selection was to find information related to mental health who can help predict the need for a work leave due to mental illness.
<br>   
To train and test our dataset, we use demographics information features (age/gender/place of habitation and work), information on current and past employer(provide or not mental health insurance plan, anonymity respected in case of mental illness issue), and also some information about individual mental health status(diagnose with mental illness or treated by a professional, currently and in the past, family history)

   
2) Can we predict if an individual is diagnosed with mental illness?


**Target**: Do you currently have a mental health disorder?
<br>
**Features**: We use demographics information(age/gender/place of habitation), as well as facts on current and previous employer(mental health coverage plan, implication towards mental illness in the company, anonymity preserved) and also insight on previous mental illness.    


3) Can we predict which work position is more likely to develop mental illness?

**Target**: Which of the following best describes your work position?
<br>
**Features**: We use demographics information(age/gender), as well as facts on current and previous employer(mental health coverage plan), insights on previous mental illness(if diagnosed/which type of illness), and also correlation with the size of the company.  

For all models, we decide to split our entry data into 75% for training set and 25% testing set, because any train-test split which has more data in the training set will most likely give you better accuracy as calculated on that test set. like that the training dataset for the model can learn and effectively map input to output. 
When splitting the dataset, we stratify it so that each split is similar. In a classification setting, it is often chosen to ensure that the train and test sets have approximately the same percentage of samples of each target class as the complete set.
<br>
As now, we are using a Random Forest Classifier because of his versatility, it can be used for both classifications and regression task. It provides higher accuracy through cross validation. Compared to simple decisions trees, instead of searching for the most important feature while splitting a node, it searches for the best feature among a random subset of features.
After training and testing, If we get a good accuracy score, we will be able when more data is added to predict the output of our target in an accurate way, even if we are missing data entries for it.
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
- Language (SQL).
- Speed.
- Maintenance.
- Ability to be access by more than one person.


[Checkout]()


Entity Relational Diagram [visit.]()




