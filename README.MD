# Introduction:

This contribution contains the MoBi implementation of the skin permeation model described in Dancik et al. 2013 [Design and Performance of a Spreadsheet-Based Model for Estimating Bioavailability of Chemicals from Dermal Exposure. Advanced Drug Delivery Reviews. 65(2): 221-236.](https://www.ncbi.nlm.nih.gov/pubmed/22285584).

In this model, the skin is a multilayered slab into which an applied permeant (drug/chemical) diffuses. Each of the slab layers in the model corresponds to an anatomical skin layer and inherits its diffusion parameters from the physical and chemical properties of the layer. In addition, we have added Michaelis-Menten kinetics in each of the sub-dermis and dermis compartments to account for metabolism.

In MoBi, the user enters parameters describing the skin, ambient conditions, experimental conditions, the permeant, the
vehicle (if any) and dosage conditions.

Simulation of the model returns:

- amounts of permeant present at different skin depths, over the time of the simulation,
- the amount of permeant that has escaped the vehicle and skin through evaporation,
- the cumulative amount and the flux, over time, of permeant that has crossed the entire skin membrane (for in vitro simulations) or cleared the dermis into the bloodstream (for in vivo simulations).

## This repository is organized as follows:

| File name                            | Description                                                                                                                                                                                                                                                                                                                     |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Skin_permeation_model_user_guide.pdf | Includes:<br>1. Introduction to the model and model details<br>2. A description of the model implementation in Mobi<br>3. Step-by-step setup and simulation of an example experiment<br>4. Connecting the dermal model to a whole body PK-Sim model                                                                             |
| skin_permeation_model.mbp3           | Main MoBi project file containing the skin permeation model. This file was made using MoBi 7.4.                                                                                                                                                                                                                                 |
| skin_spatial_structure.pkml          | PKML file containing the spatial structure of the PKML model.                                                                                                                                                                                                                                                                   |
| skin_template.mbdt                   | File containing the graphical layout of the skin model spatial structure.                                                                                                                                                                                                                                                       |
| OSPSuite.Dimensions.xml              | Note: This file is only required if you are using the version 7.4 of MoBi<br>File containing dimension definitions specific to the skin permeation model. For Windows users this file should typically reside in the directory C:\ProgramData\Open Systems Pharmacology\MoBi\X.X, with X.X representing the MoBi release number. |
| skin_favorites.xml                   | File to load list of input parameters for simulating the skin model.                                                                                                                                                                                                                                                            |
