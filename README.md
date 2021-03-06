# SimiC

## Installation
Please make sure that you are using Python 3.x, and the packages in `requirements.txt` are properly installed. If you are using `pip` then you can run:

```
pip install -r requirements.txt
```

To install SimiC in Python, go to the repository folder, and run:
```
python setup.py install
```

After the Python package is installed, you need to install the R package `reticulate` in order to use the R API for SimiC.

## Running the code in Python
To run SimiC with Single-cell RNA-seq of a small test example, go to folder `exmaple`. The test data provided here is a subsample of the hepatocypte dataset we used in [our paper](https://www.biorxiv.org/content/10.1101/2020.04.03.023002v1). The test data contains 500 cells from 3 different states.

For Python package, use the jupyter notebook `SimiC-full-pipeline` to genereate the GRNs and wAUC score matrices. Or you can run the scirpt in terminal:
```
python SimiC_exmaple.py
```
The default output contains 3 GRNs with 50 driver genes and 100 target genes.

## Running the code in R
To run SimiC with same settings as the python script, go the folder `example/R_API/`. Run the script `SimiC_example.R` in R or Rstudio.

## Evaluation of outputs
After running SimiC with the test dataset you will have two outputs: `incident_matrices` and `wAUC_matrices`. To evaluate the performance of the inferred GRNs, we proposed two different metrices: **Importance Dynamics** and **wAUA Score** (see [our paper](https://www.biorxiv.org/content/10.1101/2020.04.03.023002v1) for more detail). The example jupyter notebooks for them are in `example/eval/`. 
