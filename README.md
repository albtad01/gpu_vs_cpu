# GPU Accelerated Matrix Softening

This repository contains an implementation of matrix softening using GPU acceleration (using CUDA) to improve performance compared to running the same program on CPU.

## Description

Matrix softening is a process where, for each cell in a 3D matrix `A`, the average of all cells in a cube of size `SOFTERING_RANGE` is calculated and saved in the corresponding cell of matrix `B`. This process is computationally intensive and can benefit from parallel processing offered by GPUs.

## Implementation

The main focus of this repository is the implementation of the `gpu_matrix_softening` function using CUDA. This function takes two 3D matrices `A` (input values) and `B` (output values), calculates the softening operation on GPU, and saves the results in matrix `B`. The execution time on GPU is measured from the beginning of data transfer to the retrieval of results.

## Performance
The GPU version of the software has demonstrated a significant performance boost compared to the CPU version. 

Tests have shown that:
- the GPU version takes only 474ms to execute the software, while
- the CPU version requires 75787ms to complete the same operation.

These results highlight the notable advantage of exploiting GPU acceleration for computationally intensive applications such as matrix softening. The GPU implementation thus provides an efficient and fast alternative for computations demanding high computational resources.

## Contributors

- [Alberto Taddei](https://github.com/albtad01)
