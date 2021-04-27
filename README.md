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
- Datasource: [visit](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/resources/clean_data/clean_dataset_2016.csv)

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
Each team member have the database on his local server with up-to-date data inside.
<br>
Entity Relational Diagram [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_ERD.png)
<br>
SQL code for database creation [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes_2nd_segment/database/database_creation_SQL)
<br>
Ongoing database work [here.](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes_2nd_segment/database)
### Dashboard:

Click [here]() to review our ongoing story.