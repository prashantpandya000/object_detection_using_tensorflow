# object_detection_using_tensorflow
This project is object detection using labelimg for creating train and test data.Uses tensorflow pretrained model SSD MobileNet V2 FPNLite 320x320 which can check on runtime webcam for object detection. I have created 4 object iamges of hand sign from Naruto anime. Created 10 train set and 5 test set of each object with train_steps=3000
<br/>
![image](https://user-images.githubusercontent.com/47704891/123641925-63df0980-d840-11eb-83cb-34e31ab0befc.png)
![image](https://user-images.githubusercontent.com/47704891/123641956-6ccfdb00-d840-11eb-91be-dae2a13aaf54.png)
![image](https://user-images.githubusercontent.com/47704891/123641989-72c5bc00-d840-11eb-8ac0-76f5ebebc933.png)
![image](https://user-images.githubusercontent.com/47704891/123642029-78bb9d00-d840-11eb-9a00-40ef423ad43e.png)


## Steps
<br />
<b>Step 1.</b> Clone this repository: https://github.com/prashantpandya000/object_detection_using_tensorflow
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv tfod
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfodj
pip install jupyter
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="https://github.com/prashantpandya000/object_detection_using_tensorflow/blob/master/1.%20Image%20Collection.ipynb">1. Image Collection.ipynb</a> - ensure you change the kernel to the virtual environment as shown below
<img src="https://i.imgur.com/8yac6Xl.png"> 
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\TFODCourse\Tensorflow\workspace\images\train<br />
\TFODCourse\Tensorflow\workspace\images\test
<br/><br/>
<b>Step 7.</b> Begin training process by opening <a href="https://github.com/prashantpandya000/object_detection_using_tensorflow/blob/master/2.%20Training%20and%20Detection.ipynb">2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
