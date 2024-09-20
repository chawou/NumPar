# NumPar

The NumPar project allows you to determine the minimum number of particles required to reach a specific statistical precision in electron microscopy based measurements of particle size, shape or other measurands. Based on subsampling from a large particle measurement dataset, the code will find and fit a relation between the number of measured particles and the precision of a measured parameter (e.g. the minimum Feret diameter, the aspect ratio,..).

## Installation

Download the repository as a ZIP file, save it to a location on your computer and extract all files.

## Usage

### Prepare your data
Ensure your particle data is in csv file format, with columns corresponding to the measurands of interest (e.g. minimum Feret diameter, aspect ratio). Place your file in the same directory as the notebook. 

### Modify the notebook
Open the notebook NumPar.ipynb in Jupyter notebooks.
In section 1.1, update the following line to point to your data file:

  frame = pd.read_csv('ParticleSizer_data.csv')

If needed, adapt the names of the columns you want to read in:

  frame.rename(columns={'Min. Feret': 'Fmin'}, inplace=True)
  
  frame.rename(columns={'Feret': 'Fmax'}, inplace=True)
  
  frame.rename(columns={'Area equivalent circle diameter': 'ECD'}, inplace=True)
  
  frame.rename(columns={'Maximum inscribed circle diameter': 'MICD'}, inplace=True)
  
  frame.rename(columns={'Aspect Ratio': 'AR'}, inplace=True)

At some later points in the code you will be able to specify the measurand for which you want to execute a specific piece of code (e.g. measurand = 'Fmin')

### Run the notebook

Run the code cells to process your data. Some cells are optional, so read carefully the supporting text to check whether the code block applies to your case.

## Example data

For reference, you can use the example data 'ParticleSizer_output.csv' provided to see how the notebook functions.

##
