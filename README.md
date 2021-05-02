
# Project Overview
Mental illness affects 1 out of every 5 adults. It costs the US about $1 trillion in lost productivity. Despite how common it is, people often avoid support. This analysis examines responses to mental health concerns in the technology industry, a market worth $1.6 trillion to ask: what factors contribute to a workplace that feels comfortable and receptive to employees with mental health concerns?

### Team Members : 
- Art Tucker : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/tucker_a_branch_01) 
- Preeti Suryakumar : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/preeti-01)
- Radhika Tippana : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/rtippana_segment_2)
- Sylvain Dessagnes : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment)
- Victoria Morales : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/morales_v_branch)
- Danielle Stauffer : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/Stauffer_Branch)

## Reason:
Many of us have battled with depression and anxiety issues for most of our lives. We are intimately aware of how these issues can be exacerbated by as well as lead to financial hardships. We wanted to further explore the statistics and numbers underpinning this relationship.

## Data Sources:
The primary source for our data was Kaggle -- specifically, datasets from survey results focusing on individuals working in the tech industry from 2014 to 2021.<br>
[Visit](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment/resources) our resources.

# Methods
This data comes from Open Sourcing Mental Illness (OSMI), a nonprofit dedicated to raising awareness, educating, and providing resources to support mental wellness in the tech and open-source communities. The survey contains 1,434 responses, and measures attitudes towards mental health among tech workers with and without a mental health disorder. Our primary analysis of the dataset from 2016 (the year with the greatest number of respondents) included 1,004 responses, after data cleaning.
Data was filtered or dropped by these criteria:
1.	Dropped rows/respondents by people who work for a company, and are NOT self-employed
2.	Reduced rows/respondents by people who lived in countries where over 30 people contributed to the survey. 
3.	Removed columns/answers to survey questions with over 75% NaN

# Results
Most people identified as male in the survey. 722 respondents (72% of the total number of respondents) identified as male. 259 respondents (26% of the total number of respondents) identified as female. An exceedingly small group identified as non-binary (2%).
\
\
Most respondents said they felt comfortable talking about mental health with their supervisors. 95 women (37% of all female respondents) and 272 men (38% of all male respondents) affirmed that they would talk to their supervisor about mental health. This suggests people had similar levels of comfort discussing mental health issues, regardless of gender. However, ‘yes’, ‘no’, and ‘maybe’ responses were almost evenly split into thirds. This demonstrates people, overall, had distributive approaches.
\
\
**Figure A**
!["gender_and_mh_discus_supv"](https://github.com/ArtTucker/mental_health_and_economics/blob/main/images/gender_and_mh_discus_supv.png)
\
\
Despite some inclination to share about their mental health, almost half of all respondents believed that being identified as having a mental health diagnosis would hurt their career. 134 (52%) of women believed a mental health diagnosis either had or would hurt their career. Comparatively, 313 (43%) of men believed a mental health diagnosis either had or would hurt their career. Women feared retribution more than men in this scenario. 
\
\
**Figure B**
\
!["gender_and_mh_hurt_on_career"](https://github.com/ArtTucker/mental_health_and_economics/blob/main/images/gender_and_mh_hurt_on_career.png)
\
\
Nevertheless, when asked if they had observed co workers receiving negative consequences for revealing a mental health condition, almost 90% of both men and women said ‘no.’ Even though people feared for their careers if they were identified with a mental health condition, they also lacked any observable evidence of others receiving different treatment because of a mental health condition.
\
\
It also appeared respondents did not know if the workplace treated physical health and mental health the same. Just over 40% of men and women said, ‘I don’t know.’ 80 women (31% of female respondents) and 219 men (30% of male respondents) commented, ‘yes.’ Gender did not affect perception in this case. It could be implied that factors, such as uncertainty rather than observation of negative workplace practices, are influencing people and their choices about mental health in the workplace. 
\
\
When asked about awareness of mental health coverage, 412 (41%) of respondents answered, “I am not sure.” Most people, with no difference among men or women, did not know about their workplace’s coverage for mental health conditions. Employers also lacked efforts to spread awareness of available resources. 708 (71%) of respondents said their employers had not discussed mental health options. This perception did not vary by gender. 


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

For both model, we decide to split our entry data into 75% for training set and 25% testing set, because any train-test split which has more data in the training set will most likely give you better accuracy as calculated on that test set. like that the training dataset for the model can learn an effective mapping of input to output. 
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
- Language (SQL).
- Speed.
- Maintenance.
- Ability to be access by more than one person.

Using python package sqlalchemy, and the needed modules (create_engine/session) we build a database with our selected data and are able to preprocess it using python/pandas and then upload it into our database **Final_project_mental_health**, as well as imported it from the database into any python script we are working on.
We also can directly query the database in our pandas jupyter notebook using SQL code.
<br>
[Checkout](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_connection.ipynb) our *database_connection* script.
Running this script will update any changes applied to our datasets on the database tables.
Each team member have the database on his local server with up-to-date data inside.
<br>
Entity Relational Diagram [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_ERD.png)
<br>
SQL code for database creation [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_creation_SQL)
<br>
Ongoing database work [here.](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment/database)

### Dashboard:

Click [here]() to review our ongoing story.

# Summary
Without information, people make decisions based on personal biases, opinions or best guesses. Despite evidence to the contrary, workers believed that if an employer identified them with a mental health condition, then their careers would suffer. This felt more probable for women than men, a possible amplification of women’s minority status in the tech industry. Representing only 1 out every 4 workers, women already face different characterizations than men, because of their poorer remonstrance. While workers had not seen negative consequences for a mental health diagnosis among coworkers, they also did not notice employers spreading awareness of mental health resources or coverage. Omission in discussions prevents normalization of the subject. It could be affecting people’s willingness to be identified as having a mental health condition. Even for this survey, only 420 (41%) of the total respondents were willing to answer if they had a current mental health diagnosis.

# Recommendations for Employers
1.	Amplify communication about wellness opportunities to prevent stress from becoming a mental health condition. Normalize mental health by openly discussing it during presentations about resources and health coverage.
2.	Acknowledge and name gender dynamics in the workplace. Women perceive penalization is possible more often than men. More research is needed to understand why, but it starts by naming that men outnumber women dramatically.
3.	Workplace culture is affected by many factors. Psychological safety affects people’s productivity and retention, which has financial consequences. Do right by people. Do right by your bottom line. Consider a corporate social responsibility department. Incorporate data about employee wellness into a part of how the workplace success is defined. Measure it so there’s accountability.
4.	The world is in the middle of a health care crisis. Unfortunately, the Covid 19 pandemic represents only part of a larger story. Anxiety and depression are also on the rise. People cannot find the help that they need to address these mental health conditions. According to an American Psychological Association poll of nearly 1,800 psychologists, 74 percent said more patients were seeking treatment for anxiety disorders than before the pandemic. Nearly 30 percent of providers reported seeing more patients overall (New York Times, 2021). Employers can and must step up to meet this crisis. It is about changing how and what we communicate regarding mental health services to staff in order to maintain or improve business operations.
