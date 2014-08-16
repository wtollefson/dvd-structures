Dvd-Structures
==============

Select Protein Structures of Genes Included in the Deafness Variation Database.

This repository acts to compile a list of select homology models (those with 30 percent sequence identity or greater) for genes included in the deafness variation database, which can be accessed at deafnessvariationdatabase.org. Each of the beginning homology models in this repository were acquired from SwissProt, a modeling paradigm that uses a fixed charged potential to generate predicted structures of proteins not determined experimentally by means of sequence alignment to orthologous proteins. Also included in this repository is a corresponding refined structure for each of the input models. The refinements were done using the Force Field X  (FFX) software package that uses the AMOEBA polarizable force field as the potential energy function.

In doing the refinements, two main computational algorithms were used—a local minimization and a rotamer optimization. In summary, the local minimization uses Quasi-newton techniques to approximate the hessian and follow the local energy landscape while the rotamer optimization acts to discretize a set of side chain conformations for each residue, thereby finding the approximate lowest energy conformations given flexible side chain positions and a fixed backbone. The refinement procedure consists of a loose local minimization, followed by a rotamer optimization and then a tighter local minimization, the last step acting to let rigid rotamer conformations relax. 

The organization scheme of the repository is as follows: in the “root” directory (i.e. dvd-structures) subdirectories corresponding to the name of the gene they contain are listed. Within each of those subdirectories, the range of each homology model is displayed as a directory. In each of those directories, there are two files: the original file and the refined file. The original file is named as follows: GENE_MODELRANGE.pdb and the refined structure is: GENE_MODELRANGE_FFX.pdb. As an example, in the directory “dvd-structures” there contains a directory “ACTG1” which corresponds to the gene ACTG1. In that directory, there is a single model range that covers residues 6 to 375. In that directory there are two files, ACTG1_6-375.pdb which corresponds to the original model, and ACTG1_6_375_FFX.pdb which corresponds to the model that was refined using the FFX software package.
