# Multiobjective De Novo Drug Design with Recurrent Neural Networks and Nondominated Sorting
A cycle to generate and optimize molecules on many properties for pharmaceutical drug design.

# Requirements
* BeautifulSoup
* MatPlotLib
* Numpy
* Pandas
* PyTorch
* RDKit
* Scikit-Learn
* Selenium 

# Data
A text file containing all 500,000 molecules used as training data is provided in data.zipx

# Jupyter Notebooks
* WebScraper.ipynb: collects SMILES strings from the open source ChEMBL dataset of drug-like molecules
* DataPreprocessing.ipynb: processes training data to properly format the text file of SMILES strings 
* LSTM.ipynb: trains an LSTM recurrent neural network model on the dataset of SMILES molecules
* Generator.ipynb: generates novel and valid molecules from the LSTM model
* DataPostprocessing.ipynb: tests generated molecules for validity and pharmacokinetic properties, then selects the most optimal with the nondominated sorting algorithm
* fineLSTM.ipynb: fine-tunes the LSTM model on the most optimal (selected) molecules from the previous iteration
