# Knowledge Graphs Outlier Detection Using KumoAI

## Setup

```conda create -n kumo-hackathon-py311 python=3.11```

Dependencies
- install graphviz , prefer mac ports 
- seaborn
- 



## Data Preparation

Experiments use the processed / derived dataset from datasets/fb15k-237/exp4

1) Download datasets from Kaggle

- Freebase 15k cleaned dataset

```
import kagglehub
path = kagglehub.dataset_download("latebloomer/fb15k-237")
```

- Freebase vs Wiki mapping 

```
path = kagglehub.dataset_download("latebloomer/freebase-wikidata-mapping")
```

2) Scrape summaries from Wikipedia, join back with Freebase

- Wiki scrape scripts under notebooks/wiki_processing
- Randomize time stamps to use prediction APIs from KumoRFM , script notebooks/v1/explore_kg_use_cases.ipynb
- join back with Freebase
- All train samples are before '2025-01-01' , test samples are after (notebooks/data_preprocessing/prepare_test_subset.ipynb)


## Knowledge Graph Perturbation

Sample pairs of edges and swap their end points
- notebooks/exp4/freebase_perturbations.ipynb


## Graph model and results presented in Demo

notebooks/fb_exp5.ipynb
