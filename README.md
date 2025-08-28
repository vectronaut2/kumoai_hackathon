# Knowledge Graphs Outlier Detection Using KumoAI

## Setup

```conda create -n kumo-hackathon-py311 python=3.11```

Dependencies
- install graphviz , prefer mac ports 
- seaborn
- 



## Data Preparation

Experiments use the processed / derived dataset from datasets/fb15k-237/exp4

1) Freebase 15k cleaned dataset from Kaggle

```
import kagglehub
path = kagglehub.dataset_download("latebloomer/fb15k-237")
```

2) Freebase vs Wiki mapping 

```
path = kagglehub.dataset_download("latebloomer/freebase-wikidata-mapping")
```

3) Scrape summaries from Wikipedia

- scripts under notebooks/wiki_processing


4) Randomize time stamps to use prediction APIs from KumoRFM

- script notebooks/v1/explore_kg_use_cases.ipynb

