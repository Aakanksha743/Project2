This is an end-to-end machine learning project on Microsoft Azure where I have configured a cloud-based machine learning production model, 
deployed, and consumed it. Using the Bank Marketing Dataset, I trained a machine learning model leveraging the AutoML feature of Azure Machine Learning Studio,
deployed it into production using Azure Container Instance (ACI) 
and consumed it using REST endpoints. I also created, published and consumed a pipeline to automate the whole process.
![image](https://github.com/Aakanksha743/Project2/assets/151511734/5dbd07c3-1683-419d-ac9a-ab07407c2912)
The architectural diagram above shows the flow of operations from start to finish. Let's understand each step:

Register the Dataset: This involves uploading the dataset into Azure Machine Learning Studio. This can be done using the URL or uploading directly from a local folder.
![image](https://github.com/Aakanksha743/Project2/assets/151511734/5b100b8a-c806-4f76-9a14-3bb034b4ad1a)


AutoML run: Here we set up configurations like compute cluster, type of machine learning task (in this case classification), exit criterion, etc. This trains different models on our uploaded dataset.
![image](https://github.com/Aakanksha743/Project2/assets/151511734/74653b4f-513f-4023-892c-cc48214abcb0)


Deploy the best model: Here we select the best performing model from our AutoML run and deploy into production using Azure Container Instance (ACI) or Azure Kubernetes Service (AKS).
![image](https://github.com/Aakanksha743/Project2/assets/151511734/43bac607-f484-4d83-9466-d1456987cf8c)


Enable logging and Application Insights: This can be done either when deploying the model into production from the studio or afterwards using a python script. 
This helps us keep track of deployed model performance and number of successful/failed requests.


Consume Model Endpoints: After deploying the model, a REST endpoint is generated and this enables other services to interact with our deployed model. We can send requests to the deployed model and get responses (predictions).
![image](https://github.com/Aakanksha743/Project2/assets/151511734/52f4edb3-7d14-4f8b-ab7f-db6c3fb2125a)


Create and Publish a Pipeline: Using the Azure Python SDK with the aid of a Jupyter Notebook, we can create and publish a pipeline. 
This requires a config.json file to be present in the working directory. Using pipelines, we can automate the whole process of training and deploying our model.
