# Data Sources
Due to confidentiality laws, mental health data is hard to find. However, Data.Medicaid.gov publishes drug utilization data. The CDC and drugbank.com also releases drug information, and its uses. The file "Drug_Utilization_2020_California" contains 144,876 data points. By coupling this information with the CDC/DrugBank codes for the drugs, we can affiliate the drug with a disease/treatment-purpose.
# Analysis and Research Goals
Our goal is to conduct a cluster analysis. Clustering or cluster analysis is an unsupervised learning problem. It is often used as a data analysis technique for discovering interesting patterns in data, such as groups of customers based on their behavior. In this case, we are going to look at people's drug-use patterns to understand if mental illness is grouped in patterns. Further analysis may also test if there are correlations between MH and certain latitudes/longitudes or areas of California.
# Proposed Next Steps
1. Merge Medicaid and CDC data to associate drugs with a treatment-purpose; e.g. Mental Health
3. Filter the information by drugs used to treat mental illness.
4. Further classify type of MH by type of drug; E.g. antispychotics address psychotic disorders; selective serotonin reuptake inhibitors treat depression
5. Clean data for machine learning; e.g. remove NaN.
6. Conduct cluster analysis. 
