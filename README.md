# MavenStudyArtifacts
This repository provides a comprehensive, step-by-step guide for reproducing the study's results, starting from data extraction.

## Reproducing Results



### Prerequisites

Install neo4j (version 4.x)

Use Python version 3.*, tested with 3.12.2

Install git (any version)

Run the below commands to install git lfs and pull datasets links_all and release_all 
```sh
git lfs install
git lfs pull
```

Note: To install dependencies on MacOs, you may need to use 'brew' command

### Steps

#### Step 1: Acquire dataset from [Jaime, Damien et al paper](https://dl.acm.org/doi/10.1145/3643991.3644879) paper and convert the database dump to csv using neo4j

| Input | Output |
| --- | --- |
| [Zenodo dataset](https://zenodo.org/records/13734581) | `script` |
| Script | cypherQuery|

#### Step 2: Merge and clean datasets 

| Script | Input | Output |
| --- | --- | --- |
| `scripts/cleanGoblinData.py`|`path to dataset/links_all.csv`, `path to dataset/release_all.csv` |`path to dataset/cleaned_final_output.csv`


#### Step 3: Aggregate GAV to GA 
| Script | Input | Output |
| --- | --- | --- |
|GAVtoGA.py |  path to dataset/cleaned_final_output.csv | `plots/GAV_GA_counts`|
|


#### Step 4: Compute gini
| Script | Input | Output |
| --- | --- | --- |
|GAVtoGA.py |  path to dataset/cleaned_final_output.csv | `plots/GAV_GA_counts`|
|







