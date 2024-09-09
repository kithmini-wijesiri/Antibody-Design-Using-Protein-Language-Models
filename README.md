# Protein language models (pLMs) for antibody structure prediction and directed evolution studies

Protein language models are machine learning models trained to understand and predict protein sequences. They operate similarly to natural language models but are designed for biological sequences.
ESM-1b and ESM-1v are specific protein language models developed by Facebook AI Research (FAIR). They are trained on different datasets. **ESM-1b** is trained on UniRef50, a database containing protein sequences with 50% sequence identity cutoff. **ESM-1v** is trained on UniRef90, a similar database but with a 90% sequence identity cutoff. These models learn the statistical properties of amino acid sequences and can generate embeddings (vector representations) for protein sequences. These embeddings capture the underlying biological and evolutionary information, which can be used to predict protein structures and functions.

The mutation scheduler in Hie et al.'s study involves systematically mutating every residue in the antigen-binding region of the antibody to every other possible residue. This exhaustive approach helps identify which mutations are likely to improve or alter the antibody's binding properties. After generating mutant sequences, the likelihood of each sequence is computed using the protein language model. Sequences with likelihoods greater than or equal to the wild-type (WT) sequence are selected for experimental validation. Instead of using an exhaustive mutation scheduler, a more practical approach involves selecting the **top-k mutations** based on their likelihood scores. This reduces the computational burden while still identifying potentially valuable mutations.



