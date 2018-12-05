# Combining-Petsc-and-Slepc-with-MPI

This is an optimized version of the code that has been provided in the respository "Polaron Coherence in 2D aggregates." I have used Petsc and Slepc along with MPI. The new optimized code runs almost 20 times faster and requires a lot less memory.

What is included?
-----------------

I have included the full code along with the makefile. 

#There are some additional subroutines which deals with P3HT stacks doped with F4TCNQ anions.

#I have also added subroutines which deal with photoluminiscence spectrum of polarons. 


Petsc and Slepc
---------------
In order to understand this code, you need to know the basics of Petsc and Slepc. There are a lot of tutorials in the internet where you can learn about Petsc and Slepc. 

Here are some links:

Slepc : http://slepc.upv.es/documentation/

Petsc : https://www.mcs.anl.gov/petsc/documentation/tutorials/HandsOnExercise.html

There are a lot of good pdfs available on the internet which will explain how to use petsc and slepc for C++, python and Fortran. 


Sparse Matrix
---------------

Sparse matrix is very different from a dense matrix and has lot of zeroes. There are several efficient ways you can store a sparse matrix. In this program, you will discover sparse matrix (please look into the subroutines : subroutine hamiltonian_1p_sparse, subroutine hamiltonian_1p2p_sparse and subroutine hamiltonian_2p_sparse). I build the one particle, two particle Hamiltonian and the onetwo particle hamiltonian differently than what I have done in my other repositories. This not only saves memory but helps running the calculations faster. 

Here is a link where you can learn about sparse matrix:

https://www.geeksforgeeks.org/sparse-matrix-representation/


Running the code
----------------

I have provided my makefile, but it is recommended that you make your own. You will need lapack, slepc, petsc, mpi installed for the succesful compilation of the code. Once the code runs, it will generate three dat files which will contain information about the polaron absorption spectrum, polaron coherence and polaron photoluminiscence spectrum.

Thanks!



