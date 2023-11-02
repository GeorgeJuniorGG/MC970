# Parallel Mandelbrot Set Generation

This repository contains a C++ exercise to generate the Mandelbrot set in parallel using the std::thread library. A serial code that generates an image of the Mandelbrot set in PPM format is provided.

## Overview

The objective of this assignment is to enhance your understanding of parallel programming by introducing you to a simple program that generates the Mandelbrot set in parallel. The Mandelbrot set is a set of complex numbers that is generated by iterating a simple formula. The set is often visualized as a fractal. If you want to know more, check the [Wikipedia page](https://en.wikipedia.org/wiki/Mandelbrot_set) about the Mandelbrot set.

The serial code provided generates an image of the Mandelbrot set in PPM format. Your task is to modify the code to generate the image in parallel using the std::thread library.

## Build the program

CMake is a tool that automates the build process. Check the CMakeLists.txt file to see how it finds and links your program against the necessary libraries.

To build the program, run the following commands:

```sh
mkdir build
cd build
cmake ..
make
```

After building the program, you can run it with the following command:

```sh
./mandelbrot
```

And, of course, you can open the generated .PPM image to see what your program generated!

## What you need to do

Your task is to modify the code to generate the image in parallel using the `std::thread` library. Compare the time it takes to generate the image in serial with the time it takes to generate the image in parallel. Try different numbers of threads and compare the performance. **Write your solution in the mandelbrotThread.cpp file**.

Try to answer the following questions:

1. What is the optimal number of threads to use?
2. What is the maximum number of threads you can create?
3. What happens if you create more threads than cores in the CPU?

To help answer this question, create a sheet to measure the time it takes to execute versus the number of threads used.

Note that you only need to add code to the `workerThreadStart()` function.

## Acknowledgment

This assiginemnt uses code and ideas from the [Stanford CS149](https://github.com/stanford-cs149/asst1) and from an Intel example code.