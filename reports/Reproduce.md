Reproduce
==============================

| Notebook | 1-Click Notebook |
| --- | --- |
| Create a model | [createmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/createmodel) |
| Run the model | [runmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/runmodel) |
| Validate the model | [validatemodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/validatemodel) |

---------------
# Create a model
Press the link [createmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/createmodel) to get the code for reproducing how to crate the swimmingpool model detector. 

## See if the right datset is loaded
First thing you need to do is add the right dataset to the project. 
This should already be there but if for some reason its not surch for "JENS THUESTAD" and find the dataset "Pool-Detection" and add it to your project. [Kaggle dataset turtorial](https://www.datacamp.com/tutorial/tutorial-kaggle-datasets-tutorials-kaggle-notebooks)

## Run the model
Now you can press the "Run All" and everything should run fine. 
There are comments over every code box explaining the code bellow. 

## Finished running?
Now you can check your output data and there should be a model named "Pool-Detection-Model.pkl". 
This you can download and later use to detect swimminpool. Now you can open the [runmodel.ipynb](https://www.kaggle.com/username/example-notebook), this contains the code for running a gradio application with the model thats been crated. 


---------------
# Create a gradio application 
Press the link [runmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/runmodel) to get the code for reproducing how to run the model using gradio. 

## See if the right datset is loaded for validation 
Same as [above](#see-if-the-right-datset-is-loaded). If you want to test some pictures manualy from the validation dataset that the dataset also contains. 
The model you created should be located in the data folder, but if not for some reason you can download the model you created above and add it manualy in the dada folder(See "CUSTOM DATASETS" hedline: [link](https://www.datacamp.com/tutorial/tutorial-kaggle-datasets-tutorials-kaggle-notebooks)). 

## Run the gradio application
Now you can press the "Run All" and everything should run fine. 
There are comments over every code box explaining the code bellow. 

## Finished running?
Now you get a window with a gradio application that you can take some screenshots from the satelite pictures from google maps or just use the validation dataset and see if the application can detect the swimmingpool or not. 


---------------
# Validate the model
Press the link [validatemodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/validatemodel) to get the code for reproducing how to validate the model.

## See if the right datset is loaded for validation2
Same as [above](#see-if-the-right-datset-is-loaded). Here we are going to use the whole validation dataset to see how good the model is. The validation program also need the model you created in the [createmodel.ipynb](https://www.kaggle.com/code/jrgenbjerkan/createmodel) file. Same as [above](#see-if-the-right-datset-is-loaded-for-validation) if not the model is already loaded in the data folder.

## Run the validation
Now you can press the "Run All" and everything should run fine.
There are comments over every code box explaining the code bellow.

## Finished running?
Now you can see the result of the validation. You get an The Validation Loss and a Validation Accuracy. 

