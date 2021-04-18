# Operationalizing Machine Learning #


This is second project in the Udacity nanodegree - "Machine Learning Engineer with Microsoft Azure". The aim of this project is to configure a cloud-based machine learning production model, deploy it, and consume it. Along with it - create, publish, and consume a pipeline.

The dataset used here is same as used in Project 1 which was about bank marketing, which had 32950 rows and 21 columns - age,job,marital,education,default,housing,loan,contact,month,day_of_week,duration,campaign,pdays,previous,poutcome,emp.var.rate,cons.price.idx,cons.conf.idx,euribor3m,nr.employed and y.

Our target column name is "y" in which entries are - 'yes' and 'no'.

We will be using Azure ML Studio as well as Python SDK to complete this project. 

- - - -

## Architectural Diagram ##

Mainly the project has 7 steps, 8th one is documenttion which is needed for submission of the project. 

![3](https://user-images.githubusercontent.com/34343621/115155839-40a91880-a09f-11eb-8ba4-7dc7069f2d5a.png)

So here are all the steps:

1. Authentication
2. Automated ML Experiment
3. Deploy the best model
4. Enable logging
5. Swagger Documentation
6. Consume model endpoints
7. Create and publish a pipeline
8. Documentation

### 1. Authentication ###
As I used Udacity lab itslef, there was no need for me to perform this step. The goal of this step is: to install the Azure Machine Learning Extension which allows you to interact with Azure Machine Learning Studio, part of the az command. After having the Azure machine Learning Extension, to create a Service Principal account and associate it with your specific workspace.


### 2. Automated ML Experiment ###
In this step, one has to create an experiment using Automated ML, configure a compute cluster, and use that cluster to run the experiment.


### 3. Deploy the best model ###
After the experiment run completes, a summary of all the models and their metrics are shown, including explanations. The Best Model will be shown in the Details tab. In the Models tab, it will come up first (at the top)

### 4. Enable logging ### 
Now that the Best Model is deployed, enable Application Insights and retrieve logs. Although this is configurable at deploy time with a check-box, it is useful to be able to run code that will enable it for one.

### 5. Swagger Documentation ###
In this step, one has to consume the deployed model using Swagger.

### 6. Consume model endpoints ###
Once the model is deployed, use the endpoint.py script provided to interact with the trained model. In this step, one is needed to run the script, modifying both the scoring_uri and the key to match the key for your service and the URI that was generated after deployment.

### 7. Create and publish a pipeline ###
For this part of the project, one has to use the Jupyter Notebook provided in the starter files, also make sure to update the notebook to have the same keys, URI, dataset, cluster, and model names already created.

## Key Steps ##
There needs a dataset present for us to work with, so we need to confirm if dataset is present. Here we can see the dataset. 
![1](https://user-images.githubusercontent.com/34343621/115162401-f33da300-a0c0-11eb-834d-0e758cfa145a.png)

Next thing to do is feed it to AutoML, after fixing the target coloum which in our case was y and Classification is method used by AutoML
![2](https://user-images.githubusercontent.com/34343621/115162442-241dd800-a0c1-11eb-92aa-44741be5a607.png)



