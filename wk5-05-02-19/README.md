# HPC Training:  Spring 2019
 Week 5: 05/03/2019

## TOPIC:  CUDA/GPU Computing
Presented by: Andreas Goetz (agoetz  at  sdsc.edu)

## READING AND PRESENTATIONS:

Source code and Instructions:

* [gpu-code-examples.tar.gz](gpu-code-examples.tar.gz)
* [sdsc-scc-gpu-computing-2019-05-03.pdf](sdsc-scc-gpu-computing-2019-05-03.pdf)


## TASKS:
### TASK 1:  Using GPU nodes  
         See the README.md files in the tarfile directory and
         following instructions on "How to sue Comet's GPU nodes"

This will launch the command

```
srun -t 00:30:00 --partition=gpu-shared --nodes=1 --ntasks-per-node=7 \
     --gres=gpu:p100:1 --reservation=sccgpures --pty --wait=0 /bin/bash
```

It may take some time to get the interactive node.

### TASKS 2 and 3 begin in the section called:
* "Simple code samples accompanying slides"*

Change to directory cuda-samples, compile with 
```
nvcc example.cu -o example.x
```

### TASK 2:  cd into the GPU code directory: 
```
% cd gpu-code-examples/cuda-samples
```

See the README.md files for instructions.
Run the following examples
 
	- addition
	- hello_world


### TASK 3:  cd into the GPU code directory: gpu-code-examples/cuda-samples
# See directory openacc-samples

Compile with 
```
pgcc example.c -o example.x -acc -Minfo=accel
```

=======================================
TASK 3:  cd into the OpenACC code directory: gpu-code-examples/openacc-samples/saxpy/
```
% cd gpu-code-examples/openacc-samples/saxpy/
```

See the README.md files for instructions.
Run the following example:
 
	 - saxpy.c


