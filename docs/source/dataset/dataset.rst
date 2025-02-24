Prepare the dataset
==============================

To perform efficient *ab initio* electronic structure calculation by DeepH method 
for a class of large-scale material systems, one needs to design an appropriate 
dataset of small structures that have close chemical bonding environment with 
the target large-scale material systems. Therefore, the first step of a DeepH 
study is to perform the DFT calculation on the above dataset to get the DFT 
Hamiltonian matrices with the localized basis. The DeepH-pack only supports DFT 
results made by OpenMX for now and will support SIESTA and ABACUS soon.

Using OpenMX
^^^^^^^^^^^^^^^^^^^^^^^^

One needs to perform the DFT calculation with OpenMX 
to get the Kohn-Sham Hamiltonian output file in a binary 
form. This binary file should be placed in a separate 
folder for each structure in the dataset and should be 
named as ``openmx.scfout``. In order to get this binary file, 
the input file of OpenMX should include keywords like this::

   System.Name   openmx
   HS.fileout    On

Besides, it is required to attach the text output of 
``openmx.out`` to the end of ``openmx.scfout``, which 
means to run::

   cat openmx.out >> openmx.scfout



Using SIESTA
^^^^^^^^^^^^^^^^^^^^^^^^

DeepH-pack will support SIESTA soon.

Using ABACUS
^^^^^^^^^^^^^^^^^^^^^^^^

DeepH-pack will support ABACUS soon.