# Study melt ice shelf lake

[![DOI](https://zenodo.org/badge/1322980906.svg)](https://doi.org/10.5281/zenodo.21792650)

This repository contains the notebooks of the analyses done in Fiol et al. "Ice shelf basal melting in giant proglacial lakes".

----

The Python environment used to run these notebooks is available on Zenodo here: https://zenodo.org/records/21791113

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo..21791113.svg)](https://doi.org/10.5281/zenodo.21791113)

To have it locally (if you are on Linux), follow these steps:

- Download the tar.gz file where you want to have it
- Create a folder with the name you want for the Python environment, e.g., **mkdir env_melt_ice** 
- Go inside the folder, e.g., **cd env_melt_ice**
- Run the command: **tar -xvf path_tar_file/condapack_irene_pyjup.tar.gz** with "path_tar_file" the path to "condapack_irene_pyjup.tar.gz"

Then to use the environment:

**source path_env/env_melt_ice/bin/activate** with "path_env" the path to the "env_melt_ice" folder

Run the command: **jupyter notebook** to use the notebooks (/!\ On a cluster it could be more difficult than that to run the notebooks. See your cluster documentation for more information.)

If you cannot use the Python environment provided, here are the libraries used for the analyses and their version:

- matplotlib==3.7.3
- numpy==1.24.4
- xarray==2023.1.0
- netCDF4==1.7.1
- cmocean==4.0.3
- gsw==3.6.19
- scipy==1.10.1

others:

- Python==3.8
- jupyter==1.1.1

----

Quick explanation of the content of the different notebooks:

- Analyse_results_article_main_vf.ipynb : contains the main analyses of the paper

- Melt_param_article_vf.ipynb : contains the method used to fit the coefficients of the new parameterisation presented in the paper and all the analyses surrounding the parameterisations
  
- Fit_simplified_EOS.ipynb : contains the method used to fit the coefficients of the simplified equation of state used in the paper, its evaluation and the comparison of polyTEOS10-bsq (Roquet et al., 2025) to TEOS10 (IOC et al., 2010) in our ranges of interest

- Linearise_Tfus_heat_capacity.ipynb : contains the method used to fit the coefficients of the linear freezing temperature used in the paper and the computation of the new value for the isobaric specific heat capacity of water

- Compare_TEOS10_to_Chen_and_Millero_1986.ipynb : contains the comparison made between the TEOS10 formulation (IOC et al., 2010) and the equation of state proposed by Chen and Millero (Chen and Millero, 1986)

- quick_study_turbidity.ipynb : contains the quick study made on the potential impact of turbidity

----
### References

Chen, C.-T. A. and Millero, F. J.: thermodynamic properties for natural waters covering only the limnological range1, Limnology and
Oceanography, 31, 657–662, https://doi.org/10.4319/lo.1986.31.3.0657, 1986.

IOC, SCOR, and IAPSO: The international thermodynamic equation of seawater - 2010: Calculation and use of thermodynamic properties,
UNESCO, https://www.teos-10.org/pubs/TEOS-10_Manual.pdf, intergovernmental Oceanographic Commission, Manuals and Guides
No. 56, 196 pp., 2010.

Roquet, F., Madec, G., McDougall, T. J., and Barker, P. M.: Accurate polynomial expressions for the density and specific volume of seawater
using the TEOS-10 standard, Ocean Modelling, 90, 29–43, https://doi.org/10.1016/j.ocemod.2015.04.002, 2015.
