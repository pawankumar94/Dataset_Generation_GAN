# Synthetic Data Generation 

### This Pipeline could be used for synthesizing any type of tabular medica data.
- The first Process involved finding of freely available medical datasets which could be found at : https://archive.physionet.org/
- Selection of Suitable Dataset for fabrication depending upon the requirements

### Choice of Dataset for this pipeline Selected:
- MIMIC3 dataset which is publically available in relational database format
- Consist of information about 100 patients Vital Signs measurements and various other recording such Medication , Icu Stays, Prescriptions . etc
- Schema for the Dataset could be found at : https://mit-lcp.github.io/mimic-schema-spy/

### Pipeline for Relational Database Querying:
- Reational Databse Querying was done using Sql lite database
- The sql database file and queries could be found at code folder
- The pipeline for dataset construction which was feeded as input to Generative Adversarial Network looks as below:
![Relational Database Pipeline](https://github.com/pawankumar94/Medical_Synthesizing/blob/main/Relational_Pipeline.PNG?raw=true)

### Properties of Synthetic Data:
- Length of the dataset should be arbitrary and data should be randomly generated
- Data should resemble the original  data in shape and size
- Data should be statistically representative and yet anonymous
- Input data can be numerical, category, binary

### Advantages for Synthesizing Data:
- Cost Effective 
- Deals with class Imbalance Problem
- Minimizes the Privacy concerns
- Helps in Generating Data for infrequent Instances 
- Helps in Extending Size of the Input Data in a short span of time 


### Choice of GAN Architecture :
**Conditional Tabular Gan** :
- Data contains mixture of Discrete and continuous columns
- Data contains time series values 
- Continuous Values in dataset are usually non gaussian distribution , transformation might lead to Vanishing Gradient problem 
- Conditional Tabular GAN outperforms Bayesian Network , MedGan , VeeGan, TableGan when trained on 7 simulated and  8 real datasets 

**Architecture**
![CTGAN](https://github.com/pawankumar94/Medical_Synthesizing/blob/main/CTGAN_architecture.PNG?raw=true)



