# Placevent algorithm

## Installation
Placevent algorithm can be cloned from this repository: https://github.com/dansind/Placevent.git and run setup.py. Note that Grid and Numpy packages are required.

## Running Placevent
Placevent takes in an oxygen population density .dx file (output from either GIST or 3D RISM) and does explicit water placement, outputing a PDB file of placed waters (with resname BCD)

Typical usage is as follows:
```
python placevent.py mydxfile.dx waterconc cutoff > output.pdb
```
Waterconc is the water concentration, typically set at 55.5. Cutoff is the cutoff population density value at which to stop placing waters. Typically it is set to 1.5, meaning that all waters placed would be 1.5 times more likely to be present compared to bulk.

## Running test case
For the test case, run the the following in command line:
```
python placevent.py g.O.1.dx 55.5 > 1fjs_output.pdb
```
Reference output file is provided.
