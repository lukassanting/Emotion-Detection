# Emotion Detection
 A Jupyter notebook for emotion detection, using the FER-2013 dataset


Assignment for Computer Vision course at Maastricht University
Jannik Wirtz,Lukas Santing


Included you will find the code, which is in a Jupyter Notebook.
The code is written and tested in Google Colab. In the code there is a library and a code block that we have used specifically because they work in Colab, whereas the "normal" alternative did not work in Colab. It is possible then, that running the code outside of Colab will not allow these two functions to work. This is only relevant in the imports (Section 0) and the Real Life Test experiment (Section 7). The code will be marked.

We have tried to explain as best we could  at each step what it is for, but we will give a quick run down here.

Section 0: 
	- Library imports
Section 1: Data Pre-processing.
	- This block assumes that you have the already loaded into either your Google drive, or the local runtime. Modifying the "path" variable to suit the location should work for all data downloads in the whole code.
	- This block will download the data, restructure it into a suitable array shape, normalize the data, etc.
	- Running all of these blocks (including the "Test Blocks") should create all relevant variables for use throughout the notebook.
Section 2: Build Model Functions
	- This code houses most of the functions that we need to create, compile and test our models, as well as the data augmentation code.
Section 3: 
	- This block simply houses our model hyperparameter optimization code. Nothing needs to be run here unless you want to replicate out experiments.
Section 4: 
	- This block simply houses our data augmentation hyperparameter optimization code. Nothing needs to be run here unless you want to replicate out experiments.
Section 5:  Final model Test
	- This block is where we create and test our final models, and test them on the validation and test data, as well as through k-fold cross validation.
Section 6: This block is for the visualisation  of the filters learned by the final model.
Section 7: 
	- Here is the code to save and load models into .json and .h5 format, as well as
	- Code for video capture in Colab (linked to the original author)
	- Emotion recognition on a provided video.
	- To run the emotion recognition, you need to either capture a video of yourself expressing emotions in section 7.2, or simply upload a prerecorded video into the runtime. By default it expects the video to be called "test.mp4".
Running 7.3 will perform classification on the video, provided the "model" variable is a model that has been trained to perform this task.
