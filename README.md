# CUDA-and-Deep-learning-CPP
This repos shows some works about CUDA fundamentals and deep learning with GPU using C\C++ programming.

## Tools: 
   - CUDA C++
   - nvcc
   - nvprof

## CUDA:

  - Code that runs on the *GPU* is often called *device code, while code that runs on the *CPU* is called *host code*

  - To turn a function into a function that the GPU can run, called a kernel in CUDA, we just is add the specifier *__global__* to the function, which tells the CUDA C++ compiler that this is a function that runs on the GPU and can be called from CPU code.

## Memory Allocation in CUDA:

To compute on the GPU, we need to allocate memory accessible by the GPU. *Unified Memory* in CUDA makes this easy by providing a single memory space accessible by all GPUs and CPUs in your system.

Call:
   - *cudaMallocManaged()* : to allocate data in unified memory, it returns a pointer that you can access from host (CPU) code or device (GPU) code.
   - *cudaFree()*: to free the data.

For example: replace the  *new* in the c++ code with *cudaMallocManaged()*, and replace *delete []* with *cudaFree*.

Memory Allocation:
