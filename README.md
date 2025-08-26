# ScientificComputing-VectorMatrixOps

C program implementations of vector-vector, matrix-vector, and matrix-matrix multiplication with performance analysis.  
Includes both serial and MPI-based parallel versions, scalability tests, and plotting scripts for results.

## Contents
- serial/ : Serial implementations in C (vector and matrix operations, timing).
- parallel/ : MPI-based parallel implementations.
- Makefile or scripts/ : For compiling, running, and plotting results.
- report/ : Project report in PDF.

## Features
- Vector-Vector multiplication
- Matrix-Vector multiplication
- Matrix-Matrix multiplication
- Scalability tests for large vectors (up to N = 2.5 × 10^8)
- Strong scaling analysis with 1–8 cores
- Plotting scripts (Python/gnuplot)

## Usage

### Compile and Run
```bash
# Serial version
gcc -o serial main.c vector.c matrix.c -lm
./serial

# Parallel version (MPI)
mpicc -o parallel main.c vector.c matrix.c -lm
mpirun -np 4 ./parallel
