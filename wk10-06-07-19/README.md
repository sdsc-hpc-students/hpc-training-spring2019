# HPC Training:  Spring 2019
## Week 10:  06/07/19

## TOPICS: 
* Data Analytics (Tensor flow; torch) 
* Machine learning (Horovod) 
## PRESENTED BY: Dr. Mahidhar Tatineni ( )	

## READING AND PRESENTATIONS:
* [Presentation on Machine learning (Horovod):](https://github.com/sdsc-hpc-students/hpc-training-spring2019/blob/master/wk10-06-07-19/DL_TensorFlow_PyTorch_Horovod.pdf)

## TASKS:
1. Run a jupyter notebook on comet
* Accessing via Jupyter Notebook
Clone this repository:   https://github.com/sinkovit/PythonSeries
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
Launch the Jupyter Notebook application. Note: this application will be running on comet, and you will be given an https URL which you will connect to using your local web browser:
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


2. Try one of this Machine Learning examples:
```
module load singularity
singularity shell /share/apps/gpu/singularity/sdsc_ubuntu_tf1.1_keras_R.img
```
