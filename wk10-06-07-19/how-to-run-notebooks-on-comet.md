# HPC Training:  Spring 2019
## WEEK 10:  06/07/19	

## TOPICS: 
### 1.  Jupyter Notebooks
Using Jupyter Notebooks (by Mary Thomas): see below

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
Learn how to run/edit a jupyter notebook on comet using Python notebooks 

* Log onto comet.sdsc.edu  
```
ssh -Y -l <username> comet.sdsc.edu
```

* create a test directory, or ```cd``` into one you have already created
* Clone this repository (developed by Bob Sinkovits):   [https://github.com/sinkovit/PythonSeries](https://github.com/sinkovit/PythonSeries)
```
git clone git@github.com:sinkovit/PythonSeries.git
```

Get an interactive node:
```
srun --pty --nodes=1 --ntasks-per-node=24 -p compute -t 02:00:00 --wait 0 /bin/bash
srun: job 24000544 queued and waiting for resources
srun: job 24000544 has been allocated resources
[mthomas@comet-18-29:~/hpctrain/python/PythonSeries] 
```
Wait for your node to be allocated.
Load the singularity module that knows about jupyter notebooks and get an interactive shell
```
module load singularity
singularity shell /share/apps/gpu/singularity/sdsc_ubuntu_tf1.1_keras_R.img
```
Check out the Readme.md file, it will explaing what is in the different notebooks.
Launch the Jupyter Notebook application. 
Note: this application will be running on comet, and you will be given a URL which will connect your local web browser the interactive comet session:
```
ipython notebook --no-browser --ip=`/bin/hostname`
```
This will give you an address which has localhost in it and a token. Something
like:
```
http://comet-14-0-4:8888/?token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
You can then paste it into your browser. You will see a running Jupyter
notebook and a listing of the notebooks in your directory. From there everything should be working as a regular notebook.
Note: This token is your auth so don't email/send it around. It will go away when you stop the notebook. 

To learn about Python, run the ```Python basics.ipynb```   notebook.
To see an example of remote visualization, run the  ```Matplotlib.ipynb```  notebook!



