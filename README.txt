				HOW TO CREATE MUTANTS!

	For this example I will be using the Trp-Cage mini protein (TC5b) 1l2y.pdb.
First we need to initialize VMD (http://www.ks.uiuc.edu/Development/Download/download.cgi?PackageName=VMD)
This can be done by typing the following in a command terminal (given VMD has been properly installed):
	
	vmd 1l2y.pdb

	First we need to generate the necessary psf (protein strcuture  file) files.
PSF are needed to carry out MD simulations. PSF files contain all information regarding atom types, bonds, dihedrals,
etc. To generate PSF files we will use the Automatic PSF generator plug in.

	Once the PDB has been loaded, in the VMD main window go to Extensions->Modeling->Automatic PSF Builder.
A new window will pop up (4 steps). During step 1, one can specify the protein strucutre, PDB file, for which we desire 
to generate a PSF file, also, one can specify the name of the putput file.
Let's say we desire the output to be called 't_autopsf'. 
Click on 'Load input files', 'Guess and split chains using current selections', and 'create chains'. This is for simple modifications.
For more complicated modifications one would need to apply patches.
This will generate variaous files. The ones we need are called: t_formatted_autopsf.pdb and t_formatted_autopsf.psf.
Notice that we created a second PDB file!

	Now to create the mutants. Load the recently created PDB and PSF files t_formatted_autopsf.pdb and t_formatted_autopsf.psf.
We will use the mutator plug in to introduce mutations into our protein sequence. In the VMD main window go to 
Extensions->Modeling->Mutate residue. A new window will appear. If not already done for you, specify the path to our PSF and PDB 
files in the imput. In the next field specify the desired name for the output. For this example we will here type 'N1G', 
(we will replace the first Asparagine in TC5b by a glycine). On the 'ID of target residue' type 1 (for this example we want to modify 
the first residue). Next to 'Mutation (three letter residue name)' type GLY. After this click on 'Run mutator'.
This should output the desired files: N1G.pdb N1G.psf.

If in doubt go back to the VMD main window Extensions->Analysis->Sequence Viewer.

			:-) Happy mutating (-:


