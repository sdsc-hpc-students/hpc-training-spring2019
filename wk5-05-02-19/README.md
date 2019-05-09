# HPC Training:  Spring 2019
 Week 5: 05/03/2019

## TOPIC:  CUDA/GPU Computing
Presented by: Andreas Goetz (agoetz  at  sdsc.edu)

## READING AND PRESENTATIONS:

Source code and Instructions:
(gpu-code-examples.tar.gz)[gpu-code-examples.tar.gz]
(sdsc-scc-gpu-computing-2019-05-03.pdf)[sdsc-scc-gpu-computing-2019-05-03.pdf]

## TASKS:
1.  See the README.md files in the tarfile directory and subdirectories


Content
=======
This directory contains the slides and exercises for the SCC 2019 
training in GPU computing and programming.
Andreas Goetz, SDSC (agoetz@sdsc.edu)


How to use Comet's GPU nodes
============================

# Obtain interactive shared GPU node on SDSC Comet (3h allocation)
`getgpu` 

This will launch the command

```
srun -t 00:30:00 --partition=gpu-shared --nodes=1 --ntasks-per-node=7 \
     --gres=gpu:p100:1 --reservation=sccgpures --pty --wait=0 /bin/bash
```


# Load CUDA and PGI compiler modules
```
module purge
module load gnutools
module load cuda
module load pgi
```


# Check nvcc compiler version
` nvcc --version`


# Check installed GPUs with NVIDIA System Management Interface (nvidia-smi)
`nvidia-smi`

This will also show any currently running jobs on GPUs.


# Check visible devices (should be set to free GPU)
`echo $CUDA_VISIBLE_DEVICES`

This environment variable should be set by the queuing system to the 
ID of the free GPU.



NVIDIA CUDA Toolkit code samples
================================

# Copy and compile CUDA code samples that come with the CUDA Toolkit
Install into current directory:
```
cuda-install-samples-7.0.sh ./
cd NVIDIA_CUDA-7.0_Samples
```

Compile the samples:
```
make -j 6
```

Or compile only samples of interest, e.g. `deviceQuery`:
```
cd 1_Utilities/deviceQuery
make
```


# Check out the many code samples
This is a very instructive resource, it is a good idea to have a look
at these.


# Run deviceQuery to query information on available GPUs
```
cd 1_Utilities/deviceQuery/
./deviceQuery
```


Simple code samples accompanying slides
=======================================

# See directory cuda-samples
Compile with 
```
nvcc example.cu -o example.x
```

=======================================
TASK 2:  cd into the GPU code directory: gpu-code-examples/cuda-samples

See the README.md files for instructuions.
Run the following examples
 
	- addition
	- hello_world


# See directory openacc-samples
Compile with 
```
pgcc example.c -o example.x -acc -Minfo=accel
```

=======================================
TASK 3:  cd into the OpenACC code directory: gpu-code-examples/openacc-samples/saxpy/

See the README.md files for instructuions.
Run the following example:
 
	 - saxpy.c


