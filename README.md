# QDN-A-Quadruplet-Distributor-Network-for-Temporal-Knowledge-Graph-Completion

## Installation
Create a conda environment with pytorch and scikit-learn :
```
conda create --name QDN_env python=3.7
source activate QDN_env
conda install --file requirements.txt -c pytorch
```

Then install the kbc package to this environment
```
python setup.py install
```

## Datasets

Once the datasets are downloaded, go to the tkbc/ folder and add them to the package data folder by running :
```
python process_icews.py
```

This will create the files required to compute the filtered metrics.

## Reproducing results of QDN

In order to reproduce the results of QDN on the four datasets in the paper, go to the tkbc/ folder and run the following commands

```
python learner.py --dataset ICEWS14 --model TeLM --rank 2000 --emb_reg 0.0075 --time_reg 0.01 

python learner.py --dataset ICEWS05-15 --model TeLM --rank 2000 --emb_reg 0.0025 --time_reg 0.1

```
