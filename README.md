# AMD HPC Training Examples Repo

Welcome to AMD's HPC Training Examples Repo!
Here you will find a variety of examples to showcase the capabilities of AMD's GPU software stack.
Please be aware that the repo is continuously updated to keep up with the most recent releases of the AMD software.

## Repository Structure

Please refer to these instructions to locate the exercises you are interested in sorted by topic. 

1. [`HIP`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP)
   1. Basic Examples
      1. [`Stream_Overlap`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/Stream_Overlap): this example showcases how to share the workload of a GPU offload compation using several overlapping streams. The result is an additional gain in terms of time of execution due to the additional parallelism provided by the overlapping streams. [`README`](https://github.com/amd/HPCTrainingExamples/blob/main/HIP/Stream_Overlap/README.md).
      2. [`dgemm`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/dgemm): A (d)GEMM application created as an exercise to showcase simple matrix-matrix multiplications on AMD GPUs. [`README`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/dgemm/README.md).
      3. [`exercises`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/exercises): a collection of introductory exercises such as device to host data transfer and basic GPU kernel implementation. [`README`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/exercises/README.md).
      4. [`hip_stream`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/hip-stream): modification of the STREAM benchmark for HIP. [`README`](https://github.com/amd/HPCTrainingExamples/blob/main/HIP/hip-stream/README.md).
      5. [`jacobi`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/jacobi): distributed Jacobi solver, using GPUs to perform the computation and MPI for halo exchanges. [`README`](https://github.com/amd/HPCTrainingExamples/blob/main/HIP/jacobi/README.md).
      6. [`matrix_addition`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/matrix_addition): example of a HIP kernel performing a matrix addition. 
      7. [`saxpy`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/saxpy): example of a HIP kernel performing a saxpy operation. [`README`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/saxpy/README.md)
      8. [`stencil`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/stencil): example of a stencil operation with a HIP kernel.
      9. [`stencil_timers`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/stencil_timers): same as `stencil` but with timers.
      10. [`stencil_overlap`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/stencil_overlap): similar to `stencil` but using asyncronous copies with `hipMemcpyAsync`.
      11. [`stencil_overlap_timers`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/stencil_overlap_timers): same as `stencil_overlap` but with timers.
      12. [`vectorAdd`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vectorAdd): example of a HIP kernel to perform a vector add. [`README`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vectorAdd/README.md).
      13. [`vector_addition`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vector_addition): another example of a HIP kernel to perform vector addition.
      14. [`vector_addition_error_check`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vector_addition_error_check): same example as `vector_addition` but with error checks.
      15. [`vector_addition_hipify`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vector_addition_hipify): CUDA version of the `vector_addition` example. 
      16. [`vector_addition_hipifly`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vector_addition_hipifly): example where a header file is used to hipify on the fly the CUDA version of the `vector_addition` code.     
      17. [`vector_addition_shared`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vector_addition_shared): version of the `vector_addition` example using shared memory.
      18. [`vector_addition_timers`](https://github.com/amd/HPCTrainingExamples/tree/main/HIP/vector_addition_timers): version of the `vector_addition` example with timers.

## Run the Tests

Most of the exercises in this repo can be run as a test suite by doing:

```
git clone https://github.com/amd/HPCTrainingExamples && \
cd HPCTrainingExamples && \
cd tests && \
./runTests.sh
```
You can also run a subset of the whole test suite by specifying the subset you are interested in as an input to the `runTests.sh` script. For instance: `./runTests.sh --pytorch`. To see a full list of the possible subsets that can be run, do `./runTests.sh --help`.

**NOTE**: tests can also be run manually from their respective directories, provided the necessary modules have been loaded and they have been compiled appropriately.

## Feedback
We welcome your feedback and contributions, feel free to use this repo to bring up any issues or submit pull requests.
The software made available here is released under the MIT license, more details can be found in `LICENSE.md`.
