An exploration of one tiny fealt of Satelite Data
==============================

# Part 1 -- Background information

## What is Satelite Data?
Satellite data refers to information and images gathered by satellites orbiting the Earth. Satellites can capture a wide range of data, including weather patterns, land use, ocean currents, atmospheric conditions, and more. This data is transmitted back to Earth and can be used for a variety of applications, including weather forecasting, disaster management, natural resource management, urban planning and detecting swimmingpools.

## What is Satelite Data used for today?
* Weather forecasting
* Climate monitoring
* Natural resource management
* Disaster management
* Urban planning
* Agriculture
* Navigation
* Communication
* Military surveillance and intelligence
* Oceanography
* Geology and mineral exploration
* Environmental monitoring and conservation

## What could Satelite Data be used for in the future(now)?
* Environmental monitoring and conservation
* Security and surveillance
* AI-driven predictive analytics and modeling for various fields
* AI-powered natural language processing for analysis of satellite data
* AI-assisted image recognition for analyzing satellite images
* AI-powered algorithms for identifying patterns and anomalies in large amounts of data
* AI-assisted autonomous satellite navigation and control systems.

## What are some challenges in Satelite Data?
* Cost: Launching and maintaining a satellite is a costly endeavor, and the cost of accessing satellite data can be prohibitive for some users.
* Privacy concerns: Satellite imagery can capture sensitive information about individuals, organizations, and countries, raising concerns about privacy and security.
* Legal and regulatory challenges: Ownership and use of satellite data can be subject to legal and regulatory challenges, particularly when it comes to cross-border data sharing and intellectual property rights.
* Limited coverage and resolution: Despite the wide coverage of satellites, there are still limitations in terms of resolution and the ability to capture certain types of data.
* Interference: Satellites can be subject to interference from other satellites, ground-based equipment, or natural sources, which can affect data quality and accuracy.

# Part 2 -- My project

## Experiment detecting swimming pool by satelite images
The experiment of detecting swimming pools through satellite images involves using low-resolution satellite data to identify and locate swimming pools on the ground. This approach has the potential to enable more efficient and accurate monitoring of swimming pools, who builds them, and whether they have approval or not. If there is a database of approved swimming pool construction, you could cross-reference this information and fine individuals who have built pools illegally.

## Why did i choose this task?
The idea for this project was inspired by a recent effort by French authorities who used satellite images and artificial intelligence to find unregistered swimming pools. As reported by Jaron Schneider, the French tax office worked together with Google and a French IT firm called Capgemini to develop an AI system. This system analyzes satellite pictures to spot undeclared pools and then cross-references them with property and tax databases. The technology has been quite successful, finding over 20,000 unregistered private pools and potentially recovering millions of euros in unpaid taxes. By using FastAI to develop a similar model for detecting swimming pools in satellite images, I wanted to see if I could make a simple model like the one used by the French authorities. 

Reference: [references.md](../references/references.md)

## Finding Data
When I first started, I did a lot of research to find data that had a classification of images with pools and not pools. I thought this would be easy, but in every case I saw someone doing something similar, the dataset was not public. So in the end, I found a dataset containing approximately 3,000 pictures, 1,398 pictures with pools and 1,325 without pools. It's not the biggest dataset, but I went with it and I do not regret it now. The dataset also containd a validation set so i could test the model on brand new sets of photos afterwords. Maybe not the best dataset since it is so litte but i figurd it should work for this project. Click [here](/data/) to se the data set. 

## Problems
### Problems with imorting data
In the beginning, I had a lot of problems with Kaggle and how to use the dataset I found. I found the dataset on GitHub by someone named @yacine-benbaccar, who had used it for the same purpose but had not used FastAI, so I figured it should be perfect. Click [here](https://github.com/yacine-benbaccar/Pool-Detection) for the link to the GitHub. I tried to import the data with Kaggle's GitHub implementation, but that did not work for some reason. So with the TA´s help, we imported the dataset to Kaggle, and that worked fine.

### Problems with kaggle
There were some minor problems with Kaggle and different imports, especially Gradio.

## Results
When I am training the model, I get an error rate of approximately 0.025, which I think is really good. While a larger dataset could potentially help to further improve my model's performance. On the validation set, I get a validation accuracy of 0.8450704216957092, which is still good but a bit worse. This discrepancy could indicate that my model is maybe overfitting to the training data and not generalizing as well as I hoped to unseen data.

While a 15% error rate might be acceptable for some applications, it depends on the specific requirements of the project and the desired level of accuracy. In the beginning, I had a validation accuracy of 0.78 or something, but when I changed some parameters in the datablock, mainly this "batch_tfms=aug_transforms(mult=1.0, do_flip=True,max_rotate=45.0,max_lighting=0.4)"(see [code](https://www.kaggle.com/code/jrgenbjerkan/createmodel) for more information of the different meaning of variables), it improved to something like 0.82. Lastly, I added an unfreeze and played around with the values in the line "lr_max=slice(1e-4, 1e-3)". Then I got the validation accuracy of 0.8450704216957092, which I think is quite good.

### Future improvements 
To improve my model's performance further, I could do some more data augmentation, such as rotation, scaling, flipping, and cropping, to artificially increase the diversity of my training data. This helps the model generalize better to new images. I could also increase the dataset size, maybe collect more images to expand my dataset, particularly focusing on underrepresented cases or images that resemble the validation set. Here, I also could have tried to experiment with some different architectures, but I did a bit of research and found that ResNet18 was quite good with small datasets. Lastly i could have trided to do some un-supervised learning. 

# Conclusion and discussion
In conclusion, the project aimed at detecting swimming pools from satellite images using FastAI has achieved promising results. Despite the relatively small dataset of 3000 images, the model managed to achieve an error rate of 0.025 during training and a validation accuracy of 0.845, which indicates a satisfactory performance in identifying swimming pools in satellite imagery.

The project demonstrates the power of AI and satellite imagery in addressing real-world challenges. Although the model's performance could be enhanced further, it serves as a valuable learning experience and provides insights into the potential applications of AI-driven image analysis. 
