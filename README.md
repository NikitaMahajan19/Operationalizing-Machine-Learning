


# Operationalizing Machine Learning

In this project, I have used the Bank Marketing dataset. The aim is to operationalize machine learning by creating a model, deploying it and consuming it, so that we can get an endpoint that can easily be used by the end-user. Also, I will be creating, publishing, and consuming a pipeline by creating a pipeline endpoint.
The following step will be followed in this project: Creating Automated ML model Deploy the model Consuming the deployed model ( Swagger documentation) Create Pipeline Consume created Pipeline and Deploy it.


## Architectural Diagram
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/architecture%20diagram.JPG)

## Key Steps
### 1. Registered Dataset

Following Dataset is used for the project

![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/Registered%20Dataset.JPG)

### 2. Automated ML Experiment

I created an Automated ML Experiment on Bank Marketing dataset with target column as 'y'. For compute cluster I have used Standard_DS12_v2 and 1 as the minimum number of nodes. The experiment is using classification. Details of the same are shown in the image below.

![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/auto%20ml%20run.JPG)

### 3. Deploy the best run model

I deployed the best run model using Azure Container Instance with Authentication enabled.
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/deployed%20model.JPG)

The model is sucessfully deployed.
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/model%20healthy.JPG)

### 4. Enabled logging

To enable logging I made changes in logs.py file by putting configuration from Azure workspace and added it to the project and then enabled application insights.
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/logs1.JPG)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/logs2.JPG)

### 5. Swagger Documentation



I configured swagger docs by installing swagger.json from endpoints and changed the port number in bash script file and run it.
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/swagger.sh1.JPG)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/swagger.sh%202.JPG)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/sw.png)

Then, I started the server by running serve.py file to serve my project's swagger.json file.

![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/swagger%20output.png)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/swagger1.png)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/swagger2.png)

### 6. Consume Endpoints

Then I added  scoring_uri and key in endpoint.py from the deployed model consume section and ran the file.

![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/endpoint%20file.JPG)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/output.png)

### 7. Create and publish Pipeline

I uploaded the sample notebook provided to us and made the required changes in the cell and ran all the cells of the notebook. This created pipeline and the REST endpoint in Azure ML Studio is with active status.

![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/pipeline1.JPG)
![alt text](https://github.com/NikitaMahajan19/Operationalizing-Machine-Learning/blob/master/image/pipeline2.JPG)




## Screen Recording
Url for screencast video

![link](https://drive.google.com/file/d/1TqjI3MxM867Ppd8Vn8z0S6qoqrkKO_qB/view?usp=sharing)
