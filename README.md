# College Thesis

## Introduction
This repository includes all code used in my college thesis where I suggest on a new way to measure the efficiency of internal state leveraging by recurrent (an non-recurrent) machine learning models.

All code here has already served its purpose and it is currently not being actively maintained, but nonetheless serves as a *code sample*.

Feel free to contact me at [antonioayllonber@gmail.com](https://antonioayllonber@gmail.com) if you are interested in the contents of the thesis itself and I will answer you as soon as I'm available.

## Repository contents
The contents in this repository are organized into different categories, each contained in a subdirectory with the same name: 
1. Datasets
2. Training
3. Visualization
4. Results

Other than this categories, the `README.md` holds an introduction an information about the repository while the `requirements.txt` file may be used to recreate the python environment in which the experiments have been developed.

### Datasets
This section contains the file named `dataset_generation_preprocessing.ipynb` which was developed and used to create a synthetic dataset for the thesis' experiments.  
It also contains the resulting dataset as a csv file, which was used to train the models in order to comparatively measure their performance in planning tasks.

### Training
This section contains one file per model trained in the thesis, the files are named as the type of model that was trained in each notebook, except for the `control.ipynb` file that corresponds to the "control" model, a regular non-recurrent 2-layer MLP.  

To name the files in the order that they were trained and appear in the thesis:

1. `control.ipynb`: A regular non-recurrent 2-layer MLP.
2. `rnn.ipynb`: A Recurrent Neural Network implementation.
3. `lstm.ipynb`: A Long-Short Term Memory model.
4. `gru.ipynb`: A Gated Recurrent Unit model.
5. `transformer.ipynb`: A non-recurrent, Transformer model.
6. `ntm.ipynb`: A Neural Turing Machine as implemented in the [pytorch-ntm](https://github.com/loudinthecloud/pytorch-ntm) module.

Disclaimer: The contents of the `ntm` subdirectory in the training directory are the creation of  [loudinthecloud](https://github.com/loudinthecloud), and not my own.  

### Visualization
This section contains the `visualization.ipynb` file, which aims to help produce some visualizations of the results obtained when training the models in the "training" section.  

This notebook was used in the creation of most of the plots and data visualizations that are seen in my thesis.

### Results
This section contains an agreggate of the results from the experiments, which are better explained in the actual thesis.  

The `results` directory contains raw csv files in which trainning accuracy, testing accuracy, the mean cost of a path through the graph, and the elapsed time are logged per epoch.

While the `results.zip` file contains all results from every test factorial test performed on each model, one can find the results from only the sequential tests in the `sequential` subdirectory.  
This subdirectory does not include all ofthe trained models as only some of them undergo sequential analysis for reasons better explained in my thesis.
