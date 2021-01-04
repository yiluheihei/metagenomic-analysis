# metagenomic-analysis-notes

personal metagenomic analysis tools

## General sources

### :book: Papers

* [Best practices for analysing microbiomes](https://doi.org/10.1038/s41579-018-0029-9)
* [Current challenges and best-practice protocols for microbiome analysis](https://doi.org/10.1093/bib/bbz155)


## Normalization and differential analysis

### :book: Papers

* [A broken promise: microbiome differential abundance methods do not control 
  the false discovery rate](https://doi.org/10.1093/bib/bbx104)
* [Analysis of microbial compositions: a review of normalization and 
  differential abundance analysis](https://doi.org/10.1038/s41522-020-00160-w)
* [Normalization and microbial differential abundance strategies depend upon 
  data characteristics](https://doi.org/10.1186/s40168-017-0237-y)
* [Waste Not, Want Not: Why Rarefying Microbiome Data Is 
  Inadmissible](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003531)

### :hammer_and_wrench: Softwares

* DESeq2
* edgeR
* metagenomeSeq
* ANOCOM
* LEfSe

## Metabolic network modeling

* [paper: CoBAMP: a Python framework for metabolic pathway analysis in 
  constraint-based models](https://doi.org/10.1093/bioinformatics/btz598).
  [software: CoBAMP](https://github.com/BioSystemsUM/cobamp). 
* [paper: Fast automated reconstruction of genome-scale metabolic models for 
  microbial species and communities](https://doi.org/10.1093/nar/gky537).
  [software: carveme](https://github.com/cdanielmachado/carveme), a 
  python-based tool for genome-scale metabolic model reconstruction.
* [paper: reconstruction of genome scale metabolic models directly from 
  metagenomes](https://www.biorxiv.org/content/10.1101/2020.12.31.424982v1).
  [software: metaGEM](https://github.com/franciscozorrilla/metaGEM), a 
  Snakemake pipeline for the generation of MAGs, reconstruction of GEMs, and 
  simulation of cross-feeding interactions within microbial communities.

## Interactions in microbial communities

* [paper: Microbial interactions: from networks to 
  models](https://www.nature.com/articles/nrmicro2832)
* [paper: Metabolic dependencies drive species co-occurrence in diverse 
  microbial communities](https://doi.org/10.1073/pnas.1421834112). 
  [software: smetana](https://github.com/cdanielmachado/smetana), a tool to 
  analyse interactions in microbial communities.

## Ecological network modeling