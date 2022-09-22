# Hackathon 2022!
## Developing a pipeline for calculating image similarity

# Sagemaker Environment
    -ml.g5.2xlarge
    -Amazon linux 2, jupyter lab 1
    -Volume size: 20gb

# Explanation
The training set consists of groups of images that belong to a certain animal or 'individual'. 
E.g. 5 pictures of bottlenose dolphin Harry, or 57 pictures of blue whale John. 
The goal of this hackathon is to identity which image belongs to which individual as accurately as possible.
To develop an algorithm please only use the images in the train folder. 
The holdout folder contains images that will be used for a final evaluation of your algorithm at the end of this hackathon.
The test folder contains images that can be classified for evaluation at kaggle.
Some pictures in the holdout or test set will have no equivalent in the training set, these have to be called 'new_individual'. 
The goal is to make 5 predictions per image. 
The final score is a MAP@5 of all images. 
For more info on the evaluation have a look at evaluation.ipynb.

# Data structure:
    - train folder: These are the images to be used for developing an algorithm.
    - test folder: These are the images to be classified for the kaggle evaluation.
    - holdout folder: These are the images for evaluating your algorithm for this hackathon (do not touch until the end of hackathon).
    - effnet files: These are pretrained image embeddings of the train data based on pretrained efficientnet-b7.
    - train_minus_holdout.csv: This is the mapping of train images to the individuals.
    - Other files you see can be ignored....

# Notebook info:
    - setup.ipynb: Setting up the environment. Already done so ignore!
    - create_holdout.ipynb: For creating holdout set. Already done so ignore!
    - evaluation.ipynb: An explanation of the hackathon evaluation function.
    - exploration.ipynb: Some data exploration
    - hackathon.ipynb: Some code to help you get started, also contains example output.
    - holdout_evaluation.ipynb: The final evaluation of your work! Don't run until the end of the hackathon.
    