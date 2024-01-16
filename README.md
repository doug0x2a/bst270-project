# BST 270 Individual Project

This repository contains my attempt to reproduce the first and third figures found in the FiveThirtyEight article [Congress Today Is Older Than It's Ever Been](https://fivethirtyeight.com/features/aging-congress-boomers/).

The data for this article can be found on [github](https://github.com/fivethirtyeight/data/tree/master/congress-demographics), and should be placed in the `data` directory.

The following command can be used to obtain the file via the command line: 

```
wget -P data https://raw.githubusercontent.com/fivethirtyeight/data/master/congress-demographics/data_aging_congress.csv
```

# Environment

In order to recreate the figures, python 3.11.7 was used with pandas 2.1.4 and matplotlib 3.8.0.  The jupyter notebook can be viewed with [Jupyter](https://jupyter.org/) or with an IDE that supports jupyter such as Visual Studio Code with the Jupyter extension.  The [conda](https://docs.conda.io/en/latest/) can be used with included `environment.yml` to install the required packages along with jupyter notebook.

The following command will create a conda environment with the name  `bst270-project`

```
conda env create -f environment.yml
```

Alternatively, another name for the environment can be selected as follows:

```
conda env create -f environment.yml -n [name]
```

# Document Rendering

Activate the conda environment that was created above:

```
conda activate bst270-project
```

Creation of the pdf file can be performed with the following command:

```
jupyter nbconvert code/congress_age.ipynb --to=pdf --output-dir=.
```

