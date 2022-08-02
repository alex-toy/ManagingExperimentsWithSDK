# Managing Experiment With the SDK

In this project, we'll use the SDK in a Jupyter notebook to manage experiments. We will do this by first connecting the Azure workspace, and then passing that into the Experiments API.

You can do everything in the default Jupyter notebook provided by Azure. To open it, go to Compute and, under Appliation URI click on Jupyter. Then, go to the AzureML Samples tab, and open How to Use AzureML > Machine Learning Pipelines > Intro to Pipelines. This is a sample project that we will Clone and look through to see how we can use a notebook to manage an experiment.

<img src="/pictures/azure_pipeline_samples.png" title="azure pipeline samples"  width="700">

Then clone all the sample :
<img src="/pictures/cloning_azure_sample.png" title="cloning azure sample"  width="700">


## Introducing AutoML

We will now take the NBA data we used earlier and use **AutoML** on it.

- Create a new Automated ML Job. Choose position as target column ; choose classification and enable deep learning.
<img src="/pictures/nba-automated-ml-job.png" title="nba-automated-ml-job"  width="700">

- Observe the result from the best model
<img src="/pictures/automl_models.png" title="automl models"  width="700">

- Retrieve explanation from the model
<img src="/pictures/model_explanation.png" title="model explanation"  width="700">

- Retrieve metrics from the model
Confusion matrix :
<img src="/pictures/confusion_matrix.png" title="model explanation"  width="700">
Precision recall :
<img src="/pictures/precision_recall.png" title="precision recall"  width="700">
ROC :
<img src="/pictures/ROC.png" title="ROC"  width="700">


## AutoML and the SDK / Typical AutoML Workflow
We previously have worked with the dataset the GUI way. Now let's do it programmatically. We will create an **AutoML** run using the SDK in a Jupyter Notebook.

- Create a compute instance

- Create a dataset and upload **nba-2017-players-with-salary-wiki-twitter.csv**

- Upload **nba_notebook.ipynb** and run all cells.

That should create resources such as a running experiment :
<img src="/pictures/experiment.png" title="experiment"  width="700">

In the end you can retrieve all the results such as the explanation :
<img src="/pictures/model_explanation_notebook.png" title="explanation"  width="700">

- Create Pipeline and AutoMLStep
<img src="/pictures/pipeline_notebook.png" title="pipeline"  width="700">
