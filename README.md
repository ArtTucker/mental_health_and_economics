# Data Source
This data comes from Open Sourcing Mental Illness, a non profit dedicated to raising awareness, educating, and providing resources to support mental wellness in the tech and open source communities. They survey contains 1434 responses, and measures attitudes towards mental health among tech workers with and without a mental health disorder. 
# Analysis and Research Goals
Our goal is to understand: What factors contribute to a workplace that feel comfortable and receptive to employees with mental health issues?
# Data Cleaning Steps
1. Relabel columns
2. Examine 'self_employed' column and filter set by people who work for a company, and are NOT self-employed
3. Examine 'gender' column and recode responses to 'male' 'female' 'trans' 'nan'
4. Examine 'countries_live' column and remove data, when under 30 people responded
5. Examine 'age' column and remove data, when age falls under 20 or over 100
6. Bin 'age' and create two columns that show age as 4 bins (aka quartiles) and 10 bins (aka deciles)
7. Create a 'new_id' column with unique identifiers
8. Remove columns with over 1000 nan: 'mh_online_resources','mh_dx_revealed_clients','mh_coworkers_reveal_negative_impact','mh_product_impact','mh_product_impact_perceived'
