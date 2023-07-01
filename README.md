# Python Source Code De-Anonymization Using Nested Bigrams

This repository is the codebase for [the research paper](https://ieeexplore.ieee.org/abstract/document/8637444) I published in ICDMW, where I proposed a novel approach for authorship attribution in source code using Nested Bigrams. Note that I obtained the dataset by crawling [Google Code Jam (GCJ)](https://codingcompetitions.withgoogle.com/codejam) in 2018. Here you find the anonymized version to comply with GCJ's guideline.

The primary motivation behind this work is the increasing issue of unauthorized code modifications in cybersecurity. We developed a way to extract features from source code that carry substantial information about the connections between the nodes of the abstract syntax tree. 

## Repository Structure 

The repository is divided into three main folders: `dataframes`, `ranked_features`, and `src`. 

1. **Dataframes**: In this folder, you'll find all the dataframes used in the paper. The users' names have been anonymized and replaced with integers. For more information on how these dataframes were named and used, please refer to Section 4 of the original paper.

2. **Ranked Features**: This folder contains the results of the information gain ranking (IG ranking) and correlation-based ranking (CORR ranking) as explained in Section 4.C of the original paper. 

3. **Src**: This folder contains the source code for this project. You'll find Python scripts like `ast_bigrams.py`, `ast_features.py`, and `feature_ranking.py` that are integral to the functioning of this project. 

   - `ast_bigrams.py`: This script helps to extract all bigrams from a given dataset and return a set of tupled bigrams and their frequency count.
   
   - `ast_features.py`: This script uses the `ast` module to parse and extract bigrams from the source code files.
   
   - `feature_ranking.py`: This script ranks the features extracted from the source code based on their information gain.

## How to Use this Repository 

This repository is built for Python 2, and you will need to have that installed on your system. Once you have cloned this repository, you can directly use the scripts in the `src` folder to extract and rank features from your own source code datasets.

Please note that this repository is designed for research purposes and the scripts provided here are optimized for the use case outlined in the paper. You may need to modify or adapt them based on your own requirements. 


