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
For dnn analysis run the following command:

```python
python drug_model.py -p input_csv_file
```
The input_csv_file is a csv file that contains all the features as the keys and their respective frequency or occurrence in certain protein file. 

### CSV file information as output (input_csv_file.csv)
input_csv_file.csv will have the following format.

| Protein       | key1       | key2        | key3                   | 
|---------------|------------|-------------|------------------------|
| 4NGF_H_15_U   | 4          | 0           | 0                      |
| 5VM9_D_3_A    | 1          | 5           | 9                      |

Here key1, key2 and key3 are the triplets keys in the respective protein. Based on this input file we can perform dnn analysis and make prdiction. The code is able to generate accuracy plot, loss plot and confusion matrix which are important for model accuracy and prediction analysis.

