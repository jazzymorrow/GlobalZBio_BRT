# Global Distribution of Zooplankton Biomass - Machine Learning
This repository contains the machine learning models for producing estimates of zooplankton biomass globally. I used boosted regression trees (BRTs), and this project is submitted a part of my Master in Quantitative Biology at The University of Queensland. 

Zooplankton biomass data used in this project were sourced from the global Coastal and Oceanic Plankton Ecology, Production, and Observation Database (COPEPOD) and from the Australian Zooplankton Biomass database. The complete dataset can be found in `Data/` folder. 

The BRT model was developed using a train-test approach. A grid-search was conducted to find optimal hyperparameter values, after which the final model was training. This process can be recreated using `GlobalZBio_01_Training.Rmd`. The results of the grid-search are also stored in `Output/BRT_eval.rds` and this final model is also stored `Output/BRT_final.rds`. 

The global zooplankton biomass estimates was produced using `GlobalZBio_02_Predict.Rmd`. The one-degree gridded satellite SST, satellite Chlorophyll a and bathymetry data used in the mapping can be found in `Data/`. The output map of the prediction is stored in `Figures/`. 
