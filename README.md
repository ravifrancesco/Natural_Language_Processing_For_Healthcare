# Natural Language Processing For Healthcare

## Database

The notebooks are supposed to work on the [Pubmed_200k_RCT database](https://github.com/Franck-Dernoncourt/pubmed-rct/tree/master/PubMed_200k_RCT).

## Setup

The notebooks are supposed to run on Google Colab (it is possible to run it locally by changing the file paths and removing the drive mount for Google drive.

### Packages
It may be required to install the following libraries to make the notebooks work:

```bash
$ pip install yellowbrick
$ pip install gensim
$ pip install seaborn
$ pip install transformers
$ pip install datasets
```

### Using preprocessed data and trained models

Because of the size of the trained models and preprocessed data, these file can be found [here](https://www.dropbox.com/sh/d10caanbn8tnggl/AACoUFDn_RhiGNucrRLTLW7qa?dl=0).

### Preprocessing

The motebook `Task1.ipynb` requires to have the preprocessed dataset. To use this either use the preprocessed data mentioned in the above mentioned folder or run the notebook `Task1_preprocessing.ipynb`. The preprocessed files should be in the path indicated by `model_path`. For the notebook `Task2.ipynb` either set `is_preprocess_enabled=True` to let the notebook do the preprocessing or set it to `False` and use the preprocessed data mentioned in the above mentioned folder or run the notebook `Task1_preprocessing.ipynb`. The preprocessed files should be in the path indicated by `model_path`.

### Train
In the first cells of each notebook you can find the following line:

```python
train = <True|False>
```

This indiates that the model will be loaded. To train the model simply change the previous cell to:

```python
train = True
```

### File paths
In the first cells of each notebook you can find 2 paths:

```python
data_path = path/to/data/
model_path = path/to/saved/models/
```

The first path indicates the directory of the datasets, the second path indicates the file from which the model will be loaded (or saved if training is enabled). For the ensemble models, the ```model_path``` variable should point to the folder which contains the model files.

## Contributors

* [@Matteo-Omenetti](https://github.com/Matteo-Omenetti)
* [@ravifrancesco](https://github.com/ravifrancesco)
