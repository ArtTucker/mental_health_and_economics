# Mental Health and Economics

## Team Members : Roles : Branch Links

- Art Tucker : Git-Hub Repository Administrator : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/tucker_a_branch_01).
- Preeti Suryakumar : Technology Director : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/preeti-01).
- Radhika Tippana : Database Administration : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/rtippana).
- Sylvain Dessagnes : Database Administration : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes).
- Victoria Morales : Machine Learning Engineer : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/morales_v_branch).
- Danielle Stauffer : Machine Learning Engineers : [branch](https://github.com/ArtTucker/mental_health_and_economics/tree/Stauffer_Branch).

## Overview of Project Topic:
An analytical exploration of the connection between mental health and economic status in The US.
Mental illness affect millions of adults in the United States.
- Approximately 1 in 5 adults in the U.S. experiences mental illness in a given year.
- Approximately 1 in 25 adults in the U.S. experiences a serious mental health issue that can substantially interfere with major life activities.

Mental health problems are not moral failings. They are common occurrences, and many people need help to get better. Many factors contribute to mental health problems, including:
- Biological factors, such as genes, physical illness, injury, or brain chemistry.
- Life experiences, such as trauma or a history of abuse.
- Family history of mental health problems.

## Reason
Many of us have battled with depression and anxiety issues for most of our lives. We are intimately aware of how these issues can be exacerbated by as well as lead to financial hardships. We wanted to further explore the statistics and numbers underpinning this relationship.

## Source data:
Our team has put a lot of legwork into finding appropriate, adequate datasets that will help us properly explore this topic. Among the sources we've explored are:
* a Kaggle dataset on ['Unemployment and mental illness survey](https://www.kaggle.com/michaelacorley/unemployment-and-mental-illness-survey),
* data from [data.census.gov](https://data.census.gov/cedsci/table?q=household%20income%20by%20county&tid=ACSST1Y2019.S1902&hidePreview=false) on mean income by US county,
* a dataset from the Kaiser Family Foundation on [Adult Reporting Mental Illness in the Past Year](https://www.kff.org/other/state-indicator/adults-reporting-any-mental-illness-in-the-past-year/?currentTimeframe=0&sortModel=%7B%22colId%22:%22Location%22,%22sort%22:%22asc%22%7D) (for 2018-2019) sorted by state.
* a dataset of the [National Mental Health Service Survey 2019](https://www.datafiles.samhsa.gov/study-dataset/national-mental-health-services-survey-2019-n-mhss-2019-ds0001-nid18959) from the Substance Abuse & Mental Health Data Archive (SAMHDA), which collects "statistical information on the services and characteristics of all known mental health treatment facilities" within the United States,
* a dataset of [Health Professional Shortage Areas](https://console.cloud.google.com/marketplace/product/hhs/health-professional-shortage-areas?project=ucbeconmentalhealth), which are "federal designations that indicate health care provider shortages" in medically under-served areas throughout the United States,
* a dataset from the CDC on [Indicators of Anxiety or Depression Based on Reported Frequency of Symptoms During Last 7 Days](https://data.cdc.gov/NCHS/Indicators-of-Anxiety-or-Depression-Based-on-Repor/8pt5-q6wp), which is a result of a 'Household Pulse Survey' conducted by the Census Bureau, the National Center for Health Statistics, and other agencies, intended to "gauge the impact of the pandemic on employment status, consumer spending, food security, housing, education disruptions, and dimensions of physical and mental wellness,"
* we're also still searching for more datasets that might provide more opportunities for machine learning analysis and might help better direct our project.

## Questions:
In broad terms our project is centered around these two hypotheses:
1. The rate of Depression/anxiety is higher in lower socioeconomic class.
2. There is less mental health resource in lower income states/counties.

Our secondary or tertiary questions are as follows:

3. Has availability of mental health treatment services significantly improved or decreased in recent years?
4. How has COVID-19 affected rates of reported depression and/or anxiety?

Unfortunately we have recently realized that these questions are really limited to linear analysis and don't necessarily lend themselves to extensive machine learning models. We are working on finding better questions and better datasets.

## Machine learning model:
At this time - our ML model will be Supervised learning. We hope to see certain trends to predicts suicide or trends to diagnose depression. We anticipate using prediction models to identify triggers. Depending on our output and what information we use from the data our final presentation may include geolocation data (using javascript) or Tableau. We would also like to explore the data more and see if Tableau can be used to depict other factors such as gender, race, or job titles affecting Mental Health.

We are currently using a random forest classifier, because one of it's biggest advantages is versatility. It can be used for both regression and classification tasks, and it's also easy to view the relative importance it assigns to the input features.
Going forward we are considering utilizing a model to target why somebody could have suicidal thought or action based on gathered features about mental health and economics.

Our current machine learning model can be found [here](https://github.com/ArtTucker/mental_health_and_economics/blob/morales_v_branch/unemployement_random_forest.ipynb). It is built using the Kaggle-sourced "Unemployment and mental illness survey" data noted above.

## Database:

We are using a postgreSQL database. Knowing that we are not going to work with a huge volumes of data, there are more advantages for us to use a relational database management system.
- Data structure.
- Easy access to the network.
- Language (SQL).
- Speed.
- Maintenance.
- Ability to be access by more than one person.

Our current database work can be found [here](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes/Database).
* Entity Relational Diagram [visit](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes/Database/Database_ERD.png).
* SQL code for database creation [visit](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes/Database/Database_Creation_SQL).
