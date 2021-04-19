# Overview of Project:

An analytical exploration of the connection between mental health and economics status in The US.
As today, mental illness affect millions of adults in the United States.
- Approximately 1 in 5 adults in the U.S. experiences mental illness in a given year.
- Approximately 1 in 25 adults in the U.S. experiences a serious mental health issue that substantially interferes with one or more major life activities.

Mental health problems are not moral failings. They are common occurrences, and many people need help to get better. Many factors contribute to mental health problems, including:
- Biological factors, such as genes, physical illness, injury, or brain chemistry.
- Life experiences, such as trauma or a history of abuse.
- Family history of mental health problems.

### Data Source:

Machine Learning dataset from kaggle [visit.](https://www.kaggle.com/michaelacorley/unemployment-and-mental-illness-survey)
<br>
Income per individual by state [visit.](https://data.census.gov/)


### Problematic:

Couple problematics can be raised but this project mainly focus on :

- Is there a relation between mental illness and individual economic status?
- Is there a correlation between mental health resources, infrastructures and mental illness rate by state?
- How mental health resources and treatment evolved during the last years?

### Git Hub:

- Art Tucker : Git-Hub repository administrator [branch.](https://github.com/ArtTucker/mental_health_and_economics/tree/tucker_a_branch_01)
- Preeti Suryakumar : Technology coordinator [branch.](https://github.com/ArtTucker/mental_health_and_economics/tree/preeti-01)
- Radhika Vinodh Tippana : Database Administration [branch.](https://github.com/ArtTucker/mental_health_and_economics/tree/rtippana)
- Sylvain Dessagnes : Database Administration [branch.](https://github.com/ArtTucker/mental_health_and_economics/tree/SylvainDessagnes)
- Victoria Morales : Machine Learning engineer [branch.](https://github.com/ArtTucker/mental_health_and_economics/tree/morales_v_branch)
- Danielle Stauffer : Machine Learning engineers [branch.](https://github.com/ArtTucker/mental_health_and_economics/tree/Stauffer_Branch)


### Machine Learning Model:

Knowing that we want to predict an accurate output, we will use a supervised learning model, as it is we are still looking for the good questions to answers and dataset to answer it. The target will be to predict is someone will be touch by mental illness based on multiple features.<br>
We are using so far a random forest classifier because one of it's biggest advantage is versatility. It can be used for both regression and classification tasks, and it's also easy to view the relative importance it assigns to the input features.
Going forward we are thinking about using a model to target why somebody could have suicidal thought or action based on gathered features about mental health and economics.


### Database:

We use in our case an SQL database, more specifically Postgres. Knowing that we are not going to work with a huge volumes of data, there are more advantages for us to use a relational database management system.
- Data structure.
- Easy access to the network.
- Language (MySQL).
- Speed.
- Maintenance.
- Ability to be access by more than one person.

Entity Relational Diagram [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes/Database/Database_ERD.png)
<br>
SQL code for database creation [visit.](https://github.com/ArtTucker/mental_health_and_economics/blob/SylvainDessagnes/Database/Database_Creation_SQL)