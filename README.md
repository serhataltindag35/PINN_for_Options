# Physics-Informed Neural Network-based Option Pricing
# Overview
This repo contains the code and dataset of the study done for the thesis titled Physics-Informed Neural Network-based Option Pricing. Our goal is to solve the Partial Differential Equations BS, CEV, Heston and SABR models for both European and American style call options using the Physics-Informed Neural Network structure developed by Raissi (https://github.com/maziarraissi/PINNs).
# Datasets
The Dataset folder contains the datasets used in the project. The datasets and their descriptions are as follows:
  - american_options: Dataset used for American-style option study
  - european_options: Dataset used for European-style option study
  - option_price_comparison_random: Random dataset used to compare option models. Generated with the torch random library.
  - option_price_comparison_beta1_nu0: Synthetic dataset used to compare option models. Generated with the SABR model.
# Codes
All codes are in .ipynb format. They can be run on Google Colab or Jupyter Notebook. All .ipynb files can be run independently because each one includes all the required libraries. The necessary functions and libraries are imported separately in every .ipynb files. The general parts used in the codes are as follows:
  - ***CONNECTING TO GOOGLE DRIVE:*** It includes code that connects to Google Drive. If you're working on Google Colab, you need to connect to Google Drive to load datasets and save results.
  - ***MODEL:*** Activation function is defined using the sinus and sofplus functions and neural network is defined. Transformer structures such as encoder-decoder used in PINNFormer codes are also under this section.
  - ***RANDOM DATASET GENERATION FOR PDE AND OTHER CONDITIONS:*** The part used to generate the data required during model training. The data required for the initial and boundary conditions, as well as the collocation points required for the PDE, are randomly generated.
  - ***PDE AND PINN CONDITIONS:*** PDEs of financial models and necessary initial-boundary conditions are created under this section.

  - ***ANALYTICAL BS - MANTO CARLO - SABR PATH GENERATION:***  It includes the analytical Black Scholes and Monte Carlo method used for benchmarking. In addition to the analytical Black-Scholes and Monte Carlo methods, it also includes the SABR path that will create the dataset to be used during the synthetic dataset study.
  - ***CALIBRATION:*** It contains the functions required to find the Heston and SABR parameters of the real dataset.
  - ***CALLING REAL DATASET:*** The actual dataset containing real market data is being called. Your own file path must be entered. If working on Google Colab, files must be uploaded to Google Drive.
  - ***TRAINING:*** Training of the model is carried out under this section.
  - ***SAVING:*** Saving of the results is carried out under this section.
