# HPC Training:  Spring 2019
## WEEK 10:  06/07/19	

## TOPICS: 
### 1.  Jupyter Notebooks
**Using Jupyter Notebooks**, by Mary Thomas: see https://github.com/sdsc-hpc-students/hpc-training-spring2019/blob/master/wk10-06-07-19/how-to-run-notebooks-on-comet.md

Link to Bailey Passmores GitHub repos: [github.com/bailatrix/repositories](github.com/bailatrix/repositories)
  * PharmaPy: Reading csv files. Almost no data cleaning. Lots of detailed graph building with matplotlib. 
  * WeatherPy: Uses openweathermap API to import data. Minimal data cleaning and formatting in pandas. 
  * London-Traffic-Trends: Lots of data cleaning in pandas and simple use of matplotlib for visualizations. 
Note: Some of the notebooks don't load on the first try, but they are all there and working!

### 2.  Overview of ML/DL frameworks -TensorFlow, PyTorch, and Horovod
* [Presentation on Machine learning (Horovod):](https://github.com/sdsc-hpc-students/hpc-training-spring2019/blob/master/wk10-06-07-19/DL_TensorFlow_PyTorch_Horovod.pdf) 

PRESENTED BY: Dr. Mahidhar Tatineni

## TASKS:
### 1. Using Jupyter Notebooks (by Mary Thomas): 
Learn how to run/edit a jupyter notebook on comet using Python notebooks. See:
**Using Jupyter Notebooks**, by Mary Thomas: see https://github.com/sdsc-hpc-training/basic_skills/tree/master/how_to_run_notebooks_on_comet


Link to Bailey Passmores GitHub repos: [github.com/bailatrix/repositories](github.com/bailatrix/repositories)
  * PharmaPy: Reading csv files. Almost no data cleaning. Lots of detailed graph building with matplotlib. 
  * WeatherPy: Uses openweathermap API to import data. Minimal data cleaning and formatting in pandas. 
  * London-Traffic-Trends: Lots of data cleaning in pandas and simple use of matplotlib for visualizations. 
Note: Some of the notebooks don't load on the first try, but they are all there and working!


### 2.  Machine Learning examples:
Try one of the MINST example from Mahidhar's presentation. See slide 42. 
First, create a directory in week10 to put the codes into (e.g. mach.learn)
Copy the directory below into your ```mach.learn``` directory:
```
cp -R /share/apps/examples/SCC/ML_Tensorflow .
```
You will see a jupyter notebook in the directory:  
```
[mthomas@comet-ln2:~/hpctrain/mach.learn/ML_Tensorflow] ls -al 
total 4072
drwxr-xr-x 2 mthomas use300       8 Jun 12 20:38 .
drwxr-xr-x 3 mthomas use300       3 Jun 12 20:38 ..
-rw-r--r-- 1 mthomas use300   41066 Jun 12 20:38 LabMNIST_Final.ipynb
-rw-r--r-- 1 mthomas use300    3416 Jun 12 20:38 LabMNIST_v1_py3.py
-rw-r--r-- 1 mthomas use300 7840080 Jun 12 20:38 X_test.npy
-rw-r--r-- 1 mthomas use300 3920080 Jun 12 20:38 X_train5k.npy
-rw-r--r-- 1 mthomas use300   10080 Jun 12 20:38 Y_test.npy
-rw-r--r-- 1 mthomas use300    5080 Jun 12 20:38 Y_train5k.npy
```
Follow the directions in Task 1, and grab an interactive node.
Paste the URL into the local browser. Once you see the Jypyter notebook, 
click on the ```LabMNIST_Final.ipynb``` file.
When the browser opens, run the notebook in steps so you can see the machine learning develop.

You can make the following changes, to see how the filter efficiency and effectiveness are impacted: does the code take longer? does it have better resolution?
* modify the filter size: 2x2, 3x3, 5x5, ... 
* change the number of layers: 8, 12, 16, 24 
* change the back propagation algorithm: currently set to stochastic gradient descent

