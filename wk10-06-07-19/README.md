# HPC Training:  Spring 2019
## Week 10:  06/07/19

## TOPICS: 
* Data Analytics (Tensor flow; torch) 
* Machine learning (Horovod) 
## PRESENTED BY: Dr. Mahidhar Tatineni ( )	

## READING AND PRESENTATIONS:
* [Presentation on Machine learning (Horovod):](https://github.com/sdsc-hpc-students/hpc-training-spring2019/blob/master/wk10-06-07-19/DL_TensorFlow_PyTorch_Horovod.pdf)

## TASKS:
1. Try to run a jupyter notebook on comet
* Accessing via Jupyter Notebook
Get an interactive node:
```
srun --pty --nodes=1 --ntasks-per-node=24 -p compute --t 02:00:00 --wait 0
/bin/bash
```
Load the singularity module and get an interactive shell
```
module load singularity
singularity shell /share/apps/gpu/singularity/sdsc_ubuntu_tf1.1_keras_R.img
```
Launch the notebook
```
ipython notebook --no-browser --ip=`/bin/hostname`
```
This will give you an address which has localhost in it and a token. Something
like:
```
http://comet-14-0-4:8888/?token=389587c9d1b69f8f595e7d8bfdd83c9961ed26b8b3f1bb3e
```
You can then paste it into your browser. That should get you into the running
notebook. From there everything should be working as a regular notebook.
Note: This token is your auth so don't email/send it around.

2. Try one of these examples:

