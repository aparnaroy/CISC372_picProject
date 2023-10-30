# CISC372 HW3
For this assignment we will be modifying a simple image convolution program that can load an image and apply a standard filter to that image.  The program will output the results as a png image called output.png.  Available filters are: edge detection, sharpen, blur, gaussian, emboss, identity.  These are RUDIMENTARY filters, and results are very poor compared to most commercial software, but it is sufficient to play with for our purposes.  I have provided some pictures for you to work with, but you can try your own as well. 
#### Example of how to run the image.c file: <br>
Compile: `cc image.c -o image -lm` <br>
Run: `./image pic1.jpg edge`

## Program 1: pthreads
Modify the program image.c to make it multi-threaded using pthreads.  You may do this any way you wish, but you must make sure you avoid race conditions, and that your choice of what to parallelize and how to parallelize it makes sense.  Compile your code with -lthread and see what the results of your parallelization.
#### Example of how to run the image_pthreads.c file: <br>
Compile: `cc image_pthreads.c -o image_pthreads -lm -lpthread` <br>
Run: `./image_pthreads pic1.jpg edge 30`

## Program 2: OpenMP
Modify the program image.c again (save in a new file) to make it multi-threaded using pragmas in OpenMP.  You may do this any way you wish, but you must make sure you avoid race conditions, and that your choice of what to parallelize and how to parallelize it makes sense.  Compile your code with -fopenmp and see what the results of your parallelization.  
#### Example of how to run the image_openmp.c file: <br>
Compile: `cc image_openmp.c -o image_openmp -lm -fopenmp` <br>
Run: `./image_openmp pic1.jpg edge`