# Seed classifier

This is a pipeline written in Python with a Python Notebook to aid in 
classifying the ploidy level of Arabidopsis embryos that were the result 
of interploidy parental crosses: paternal excess tetraploid crossed to 
maternal diploid. This was a foundational model that is intended to be 
built upon once additional skills and data have been acquired.

To run:
1.	Download MachineLearning_code.ipynb and MachineLearning_data.txt 
into a single directory.
2.	Make sure to edit the “pd.read_csv()” function so that it includes 
your directory path to the data file.

In the analysis, it was found that 1-3 n_neighbors were better suited than 
the original 5 n_neighbors for the hyperparameter. This resulted in a more 
accurate coloring of the plotted points. 

Future models may include additional data, e.g. maternal excess crosses 
and ecotype information, which will extend the use of this machine 
learning tool.

