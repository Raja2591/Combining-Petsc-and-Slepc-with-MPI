

_____________________________________________________________________________________________________________________________________
This repository contains a fully optimized code that calculates Charge Modulation/IR spectrum, polaron coherence and photoluminiscence for organic materials. You will learn how to code using sparse matrix techniques (Petsc and Slepc) along with MPI. The code successfuly runs on multiple nodes in a single processor or on multiple nodes on multiple processors. 
      
                                                          Author: Raja Ghosh 
                                                          contact: raja.ghosh@temple.edu, raghosh@ucsd.edu
--------------------------------------------------------------------------------------------------------------------------------------
Citations
----------------

If you use the results from this program in a publication, please cite the following papers. This program is distributed 
under the MIT liscense.


1. R. Ghosh, C.M. Pochas and F.C.Spano, “Polaron Delocalization in Conjugated Polymer Films”,J. Phys. Chem.C, 2016, 120 (11394-11406).

2. Ghosh, R.,Luscombe, C. K., Salleo, A., Spano, F. C., “Anisotropic Polaron Delocalization in conjugated Ho-mopolymers and Donor Acceptor Copolymers”,Chem. Mater., 2019, 31 (7033).

3. Ghosh, R., Chew, A.R., Onorato, J., Pakhnyuk, V., Luscombe, C. K., Salleo, A., Spano, F. C., “Spectral Signaturesand Spatial Coherence of Bound and Unbound Polarons in P3HT Films: Theory vs Experiment”,J. Phys. Chem.C, 2018, 122 (18048).

4. A.R. Chew,R. Ghosh, Z. Shang, F.C. Spano and A. Salleo, “Sequential Doping Reveals the Importance of Amor-pous Chain Rigidity of Charge Transport of Semi-Crystalline Polymers”,J. Phys. Chem. Lett., 2017, 20 (4974-4980).

5. Scholes, D. T., Yee, P. Y., Lindemuth, J. R., Kang, H., Onorato, J.;Ghosh, R.; Luscombe, C. K.; Spano, F. C.; Tol-bert, S. H.; Schwartz, B. J., “The Effects of Crystallinity on Charge Transport and the Structure of SequentiallyProcessed F(4)TCNQ-Doped Conjugated Polymer Films.”,Adv. Funct. Mater., 2017, 27 (17025654).

6. Chew, A.R.,Ghosh, R., Pakhnyuk, V., Onorato, J.; Davidson, E.C., Segalman, R.A., Luscombe, C. K., Spano, F. C.,Salleo, A., “Unraveling the Effect of Conformational and Electronic Disorder in the Charge Transport Processes of Semiconducting Polymers”, Adv. Funct. Mater., 2018,(1804142)

7. Ghosh, R.; Spano, F. C. Excitons and Polarons in Organic Materials. Acc. Chem. Res.2020, 53, 2201-2211.

8. Ghosh, R.; Paesani, F. Unraveling the Efect of Defects, Domain Size, and Chemical Doping on Photophysics and Charge Transport in Covalent Organic Frameworks. Chem.
Sci. 2021, 12, 8373-8384.

9.  Ghosh, R.; Paesani, F. Topology-Mediated Enhanced Polaron Coherence in Covalent Organic Frameworks. J. Phys. Chem. Lett. 2021, 12, 39, 9442–9448.

# Combining-Petsc-and-Slepc-with-MPI

This is an optimized version of the code that has been provided in the respository "Polaron Coherence in 2D aggregates." I have used Petsc and Slepc along with MPI. The new optimized code runs almost 20 times faster and requires a lot less memory. Please check the file "polaron_cmsf90" for the full optimized code.

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

Here is a link where you can learn about sparse matrix; there are several other very good tutorials available in the net.

https://www.geeksforgeeks.org/sparse-matrix-representation/


Running the code
----------------

I have provided my makefile, but it is recommended that you make your own. You will need lapack, slepc, petsc, mpi installed for the succesful compilation of the code. Once the code runs, it will generate three dat files which will contain information about the polaron absorption spectrum, polaron coherence and polaron photoluminiscence spectrum.




Thanks!



