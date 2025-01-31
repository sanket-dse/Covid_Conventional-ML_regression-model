# Covid_Conventional_ML_regression-model
This repository is for a project based on conventional machine learning models.
## Project Inspiration 
This project was inspired from a series on Bioinformatics by *DataProfessor* on YouTube. I am attaching the relevant YouTube and Github links.
* <ins>YouTube</ins> - https://www.youtube.com/watch?v=plVLRashaA8&t=280s
* <ins>Github</ins> - https://github.com/dataprofessor/code/tree/master/python
## Background info 
**Dihydrorotate dehydrogenase** is a potential host target (i.e *human*) , the inhibition of which can provide with a therapeutic relief for COVID-19 patients. This is a paper that discusses this point - https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7406694/

In this project we will be predicting *pIC50 values* of drugs towards the target mentioned above using *molecular descriptors* as the input data.
>pIC50 is the negative logarithm to the base 10 of IC50 values which indicate the concentration of drug required to inhibit the bioactivity of our target protein by 50 percent.
## Python Notebooks included 
The following jupyter notebooks are included along with their descriptions:

* *Covid\_Ai\_1.ipynb* - This contains all the preprocessing of data , classification of molecules into active and inactive, and calculation 
 and verification of lipnski descriptors.
* *Covid\_Ai\_2.ipynb* - This file contains all the feature selection methods, regression models and their results.
## Files included 
The following files are included :

* *DHODH\_covid\_bioactivities.csv* - This csv file contains the raw data to be processed by the first ipynb file.
* *pIC50+something\_dataframe.csv* - This file contains the pIC50 values, lipinski descriptors and smiles .
* *smile2mol.smi* - This contains all the molecules in smiles format which will be inputted into Mordred to get molecular descriptors.
* *mol\_descriptors.csv* - This file contains the molecular descriptors calculated by Mordred . Some column values are missing from 
 this column.
* *scaled\_mol\_descriptors.csv* - This file contains the cleaned up and scaled molecular descriptor values.

## Calculating Molecular Descriptors 
It should be noted that the *smile2mol.smi* was the file that was feeded to Mordred through command line in the python environment containing the module and outputted to *mol_descriptors.csv.* The command that I used was :
> $ python -m mordred smile2mol.smi -o mol_descriptors.csv
