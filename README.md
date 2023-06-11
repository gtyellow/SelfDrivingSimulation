# SelfDrivingSimulation
This repository takes a video from a webcam attached to a vehicle as the feature data and pairs it with the angle of the steering wheel as the target.  We then apply datatransformers to manipulate the data.  The artificial intelligence model uses the DAVE2 neural network to predict the wheel's steering angle.

Initially tried a method without data cleaning.  The results were extremely poor.

The next attempt used data cleaning and the results were much better. 

I tested this repository on a Mac with an intel chip.  I do not believe it will work in Colab without workarounds as Colab tends to crash while using openCV.  Windows will likely work.

To use this program, select the folder either with or without datacleaning (with data cleaning works much better).  The folder contains a file that constructs the model, and a file that runs the model and builds the video. You will also need to download the two key files and the image of the steering wheel.  

You will also need to download the images from the training folder and the testing folder.  We use the training dataset (0-57,999) as well as the 0-57999 key file for building the model.  We then use the remaining images (test) and the 58,000plus key file for building the model.  You will need to edit your python scripts to point at the correct paths where the files are located in several places.

Running the Model building python file will build a model but if you don't have access to a GPU, it will take a very long time.  I've included the two models (with and without datacleaning) that I have built which you can use to run the model.  The run the model file builds video of the car driving as well as the models predictions of the steering wheel turning.  I stiched them together using Imovie from my Mac.
