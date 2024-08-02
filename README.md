Author: Jovey Osagie,  SULI intern Summer 2024
Protonatation Sotware:
  In this repository are functions I made to compare Marvin and MolGpKa predictions
  I used MolGpKa, an Open-Source pKa prediction software. https://pubs.acs.org/doi/10.1021/acs.jcim.1c00075
 
  Below is more detailed information

Environment:
  First and foremeost, if you want access the conda environments I created in jupyter lab (if they exist past my internship)
  you can navigate to my home directory (cd~ -> /home/josagie) and use the command ". ~/.bashrc" to activate the base environment,
  then "conda activate MOLGPKA" to get to conda environment I've created. 
  The environment files themselves are located in the directory "/home/josagie/anaconda3"

  GitHub:
  MolGpKa's Github repo has their own yml files to recreate their environment,
  but I had consistent problems trying to recreate the environment, primarily due to conflicting packges.
  My suggestion is to not recreate MolGpKa environment directly from the yml and instead
  1. conda install rdkit (use conda forge for conda installations, ie. conda install -c conda-forge rdkit)
  2. pip install torch, torch-cluster, torch-geometric, torch-scatter, torch-sparse, torch-spline-conv, torchvision
     (Make sure you install based on if your using a cpu or gpu, I used cpu)
  4. conda install numpy
  5. conda install matplotlib, for graphing
  6. conda install other libraries

  Most of my package conflicts arose due to disagreements between numpy, rdkit, and torch, so I've included the package version's that worked for me
  
  torch                     2.3.1 
  torch-cluster             1.6.3 
  torch-geometric           2.5.3 
  torch-scatter             2.1.2 
  torch-sparse              0.6.18
  torch-spline-conv         1.2.2 
  torchvision               0.18.1
  rdkit                     2024.03.4
  numpy                     1.26.4 
  
Notebooks:
   
  
  
molecule_utils:
  Within the molecule_utils folder are functions I implement in my Notebooks
  Pipeline.py: Data transformations stored as classes, these are not meant to be robust (I encourage altering them for your own purposes),
               they're meant to help clarify what data transformations I'm performing. 
  Analysis.py: Produces R2, RMSE, and MAE measurements. Plots linear regression plot
  Modified_MolGpKa: Nothing different, 
  
