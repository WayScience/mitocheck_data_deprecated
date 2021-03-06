# 0. Preprocess Movies

In this module, we present our pipline for preprocessing mitosis movies.

## A. Quality Control

Mitosis movies were pre-preprocessed by Mitocheck in a two-step quality control procedure based on automatic and manual inspection of data (see [quality control](https://static-content.springer.com/esm/art%3A10.1038%2Fnature08869/MediaObjects/41586_2010_BFnature08869_MOESM58_ESM.pdf) section of original paper's methods for more details).
This procedure was applied before the movies were uploaded to IDR and thus the downloaded data only includes data that has been pre-preprocessed by MitoCheck.

We discard well A1 from each plate, as each of these wells had an irregular illumination function. 

![Illumination Functions](images/illumination_functions.png "Logo Title Text 1")
**Figure 1**: *Illumination function of an A1 well (left) vs a typical illumination function (right).*

While a typical microscopy illumination function involves vignetting in the image (as demonstrated in every well besides A1), this was not the case for any A1 well that was manually inspected (figure 1).
This irregular illumination function led to errors in illumination correction later in preprocessing.

## B. Illumination Correction 

We use the BaSiC method for illumination correction of each well.
BaSiC was first introduced in [Peng, T., Thorn, K., Schroeder, T. et al., 2017](https://doi.org/10.1038/ncomms14836) and we use the [BaSiCPy implementation](https://github.com/peng-lab/BaSiCPy).


In the future we hope to implement a newer method of illumination correction introduced in [Peng, T et al., 2020](https://doi.org/10.1007/978-3-030-59722-1_17) once this method is [made available in python](https://github.com/peng-lab/BaSiCPy/issues/65).

