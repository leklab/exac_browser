# Legacy gene model framework

The older versions of gnomAD browser used the same gene model framework as the ExAC browser dependent on a mongo database. In fact this is the only reason why mongo is currently required.  

For the SFARI and PCGC Browser there are plans to move away from using this and have gene model data in the elastic search database.


## Dependent data sets
* Gencode v29 GTF
* Canonical transcripts
* OMIM data

## Installation
```
# Clone the repo
git clone https://github.com/leklab/exac_browser.git

# Setting up virtual environment
virtualenv exac_env
source exac_env/bin/activate

# Install python requirements
pip install -r requirements.txt
```

## Load gene models
```
python manage.py load_gene_models
```

## Known issues
There are some python 2 dependencies that are no longer supported. As this code is only used to upload the gene model data this isn't really needed so there are plans to remove.
