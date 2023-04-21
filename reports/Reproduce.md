Reproduce
==============================

| Notebook       | 1-Click Notebook                       |
| -------------- | -------------------------------------- |
| Create a model | [createmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/createmodel) |
| Run the model  | [runmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/runmodel) |
| Validate the model | [validatemodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/validatemodel) |

---------------
# Create a model
Click the link [createmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/createmodel) to access the code for reproducing the swimming pool model detector. Then press "Eidt" in the top right corner. 

## Ensure the correct dataset is loaded
First, you need to add the appropriate dataset to the project. It should already be present, but if for some reason it is not, search for "JENS THUESTAD" and find the "Pool-Detection" dataset. Then, add it to your project. [Kaggle dataset tutorial](https://www.datacamp.com/tutorial/tutorial-kaggle-datasets-tutorials-kaggle-notebooks)

## Run the model
Now, you can click "Run All" and everything should run smoothly. 
There are comments above each code box explaining the code below. 

## Finished running?
Once complete, you can check your output data, and there should be a model named "Pool-Detection-Model.pkl". You can download this and use it later to detect swimming pools. Next, open [runmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/runmodel), which contains the code for running a Gradio application with the model you just created. 


---------------
# Create a Gradio application 
Click the link [runmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/runmodel) to access the code for reproducing how to run the model using Gradio. Then press "Eidt" in the top right corner. 

## Ensure the correct dataset is loaded for validation 
Follow the same process as [above](#ensure-the-correct-dataset-is-loaded). If you want to test some images manually from the validation dataset, you can do so. The model you created should be located in the data folder. If it is not there for some reason, you can download the model you created earlier and add it manually to the data folder (See "CUSTOM DATASETS" headline: [link](https://www.datacamp.com/tutorial/tutorial-kaggle-datasets-tutorials-kaggle-notebooks)). 

## Run the Gradio application
Click "Run All", and everything should run smoothly. 
There are comments above each code cell explaining the code below. 

## Finished running?
After completion, a window displaying the Gradio application will appear. You can take screenshots of satellite images from Google Maps or use the validation dataset to test if the application can detect swimming pools. 

---------------
# Validate the model
Click the link [validatemodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/validatemodel) to access the code for reproducing how to validate the model. Then press "Eidt" in the top right corner. 

## Ensure the correct dataset is loaded for validation2
Follow the same process as [above](#ensure-the-correct-dataset-is-loaded). In this step, we will use the entire validation dataset to evaluate the model's performance. The validation program also requires the model you created in the [createmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/createmodel) file. If the model is not already loaded in the data folder, follow the same process as [above](#ensure-the-correct-dataset-is-loaded-for-validation) to add it manually.

## Run the validation
Click "Run All", and everything should run smoothly.
There are comments above each code cell explaining the code below.

## Finished running?
After completion, you can view the validation results. You will receive a Validation Loss and a Validation Accuracy.
