# Deep Neural Network

**Deep Neural Network** is a an analysis tool for model prediction and classification.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
  - [Deep Neural Network](#deep-neural-network)

## Installation

### Cloning the Repository

To get started with the `Deep Neural Network`, clone the repository from GitHub:

```bash
git clone https://github.com/KrishnaRauniyar/Nucleotide_Analysis.git
cd Nucleotide_Analysis/dnn
```

### Installing the Package
1. It's recommended to create a virtual environment:

```bash
python3 -m venv tsrenv
source tsrenv/bin/activate  # Mac/Linux
tsrenv\Scripts\activate  # Windows
```

2. Install the necessary dependencies:

```bash
pip install -r requirements.txt
```

## Usage
### Deep Neural Network
The analysis involves two main steps:

1. Generate Key Frequency File
First, you need to generate a frequency file that will create the input CSV for the DNN model, the key frequency files can be created from the triplets file which we create from the Nuclotide section (https://github.com/KrishnaRauniyar/TSR_NUCLEOTIDE_PACKAGE.git). We just need to specify the acutual directory path of the triplets keys. Use the following command to generate the input file:

```bash
python key_frequency_drug.py -p triplets_directory -H yes
```

Parameters:
- -p: Path to the directory containing protein files
- -H: Set to 'yes' to include headers in the output CSV

This will generate an input CSV file with the frequency of triplet keys for each protein.

### CSV file information as input (input_csv_file.csv)
input_csv_file.csv will have the following format.

| Protein       | key1       | key2        | key3                   | 
|---------------|------------|-------------|------------------------|
| 4NGF_H_15_U   | 4          | 0           | 0                      |
| 5VM9_D_3_A    | 1          | 5           | 9                      |

Here key1, key2 and key3 are the triplets keys in the respective protein. Based on this input file we can perform dnn analysis and make prdiction. The code is able to generate accuracy plot, loss plot and confusion matrix which are important for model accuracy and prediction analysis.

2. Run DNN Analysis after generating the input CSV, run the DNN model:

```bash
python drug_model.py -p input_csv_file
```
The input_csv_file is a csv file that contains all the features as the keys and their respective frequency or occurrence in certain protein file. 

## Result
Three files will be generated:
- accuracy_plot.png (This is the accuracy plot of the dnn model)
- loss_plot.csv (This is the loss plot of the dnn model)
- confusion_matrix.csv (This is the confusion matrix of the dnn model)

