# metagenomic-analysis-notes

personal metagenomic analysis tools

## General sources

### :book: Reviews 

* [Best practices for analysing microbiomes](https://doi.org/10.1038/s41579-018-0029-9)
* [Current challenges and best-practice protocols for microbiome 
  analysis](https://doi.org/10.1093/bib/bbz155)
* [Shotgun metagenomics, from sampling to analysis](https://doi.org/10.1038/nbt.3935).
* [A practical guide to amplicon and metagenomic analysis of microbiome data](https://doi.org/10.1007/s13238-020-00724-8)

## Data quality control

* [paper: Quality-filtering vastly improves diversity estimates from Illumina amplicon 
  sequencing](https://www.nature.com/articles/nmeth.2276), "For datasets where a mock 
  community is not included for calibration, we recommend the conservative threshold 
  of (c = 0.005%). c is the OTU abundance threshold". 
  
  See also in [qiime forum: feature filter](https://forum.qiime2.org/t/filter-features/1493/3): 
  The abundance filtering recommendation was specific to the OTU picking pipelines in 
  QIIME1 (but would probably still apply if you use the OTU picking pipelines in QIIME2),
  and is not tested in conjunction with dada2 or deblur, and are most likely unnecessary 
  (based on the results reported in the original papers for dada2 and deblur) or even 
  conflicting. 

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

* LEfSe, [Metagenomic biomarker discovery and 
  explanation](https://doi.org/10.1186/gb-2011-12-6-r60)
* DESeq2, [Moderated estimation of fold change and dispersion for 
  RNA-seq data with DESeq2](https://doi.org/10.1186/s13059-014-0550-8)
* edgeR, [edgeR: a Bioconductor package for differential expression 
  analysis of digital gene expression data](https://doi.org/10.1093/bioinformatics/btp616)
* metagenomeSeq, [Differential abundance analysis for microbial 
  marker-gene surveys](https://doi.org/10.1038/nmeth.2658)
* ANCOM, [Analysis of composition of microbiomes: a novel method for studying 
  microbial composition](https://www.tandfonline.com/doi/full/10.3402/mehd.v26.27663)
* ANCOMBC, [Analysis of compositions of microbiomes with bias 
  correction](https://www.nature.com/articles/s41467-020-17041-7)
* [animalcules](https://github.com/compbiomed/animalcules), **Note** this R package is 
  not only for differential analysis, it is a comprehensive analysis toolkit for 
  microbiome analysis workflow. Specifically, it supports biomarker identification by 
  training a logistic regression or random forest model with cross-validated biomarker 
  performance evaluation.

## Metabolic network modeling

* [review paper: Reconstructing organisms in silico: genome-scale models and their 
  emerging applications](https://www.nature.com/articles/s41579-020-00440-4),
  review on overrall development of genome-scale models and their applications,
  and the emerging areas in genome-scale modeling of microbioal phenotypes.
* [review paper: Current status and applications of genome-scale metabolic 
  models](https://doi.org/10.1186/s13059-019-1730-3)
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
* [moped - A Python package for metabolic modelling and topological 
  analysis.](https://www.biorxiv.org/content/10.1101/2020.12.04.411512v1)
* [MICOM: Metagenome-Scale Modeling To Infer Metabolic Interactions in the 
  Gut Microbiota.](https://msystems.asm.org/content/5/1/e00606-19.abstract)

## Applications of genome-scale metabolic modeling

* [paper: Using Genome-scale Models to Predict Biological 
  Capabilities](https://www.cell.com/cell/abstract/S0092-8674(15)00568-1)
* [paper: Understanding the host-microbe interactions using metabolic 
  modeling](https://doi.org/10.1186/s40168-020-00955-1)

## Interactions in microbial communities

* [review paper: Microbial interactions: from networks to 
  models](https://www.nature.com/articles/nrmicro2832)
* [paper: Metabolic dependencies drive species co-occurrence in diverse 
  microbial communities](https://doi.org/10.1073/pnas.1421834112). 
  [software: smetana](https://github.com/cdanielmachado/smetana), a tool to 
  analyse interactions in microbial communities.
* [paper: MMinte, an application for predicting metabolic interactions 
  among the microbial species in a community](https://doi.org/10.1186/s12859-016-1230-3).
* [paper, algorithm: Ecology-guided prediction of cross-feeding interactions 
  in the human gut microbiome](https://www.nature.com/articles/s41467-021-21586-6),
  GutCP:  a new ecology-guided method to infer and predict cross-feeding interactions 
  in the human gut microbiome. It can also be used to pridict the metabolomic composition
  based on a original cross-feeding network (in which nodes are metabolites or microbes).

## Ecological network modeling

* [manta: a Clustering Algorithm for Weighted Ecological 
  Networks](https://msystems.asm.org/content/5/1/e00903-19), used for
  networks with negative edges (microbial community ecological networks). 


## Multiple-omics

* [Learning representations of microbe–metabolite 
  interactions](https://www.nature.com/articles/s41592-019-0616-3), 
  inferring microbio-metabolite interactions using neural networks 
  (https://github.com/biocore/mmvec) to estimate the conditional
  probability that each molecule is present given the presence of a
  specific microorganism.

## Database

* [HumanMetagenomeDB](https://webapp.ufz.de/hmgdb/), explore and download 
  curated human metagenomes metadata, [paper in 2021 NAR 
  database](https://doi.org/10.1093/nar/gkaa1031).
* [MASI](http://www.aiddlab.com/MASI/index.html), interaction between 
  human microbiota and active substances, especially for those
  therapeutically-relevant substances such as clinical used drugs and 
  traditional medicines/herbs, [paper in 2021 NAR 
  database](https://doi.org/10.1093/nar/gkaa924)
* [GIMICA](https://idrblab.org/gimica/), host genetic and immune factors 
  shaping human microbiota, [paper in 2021 NAR 
  database](https://doi.org/10.1093/nar/gkaa851)
* [gutMDisorder](http://bio-annotation.cn/gutMDisorder), a manually 
  curated database, aims at providing a comprehensive resource of dysbiosis 
  of the gut microbiota in disorders and interventions. [paper in 2020 NAR 
  database](https://doi.org/10.1093/nar/gkz843)
* [GMrepo](https://gmrepo.humangut.info/),  a database of curated and
  consistently annotated human gut metagenomes. [paper in 2020 NAR 
  database](https://doi.org/10.1093/nar/gkz764)
* [HMPDACC](https://portal.hmpdacc.org/), Human Microbiome Project
  Multi-omic data resource, [paper in 2021 NAR 
  database](https://doi.org/10.1093/nar/gkaa996)
* [Peryton](https://dianalab.e-ce.uth.gr/peryton), database of 
  experimentally supported microbe-disease associations. [paer in 2021 NAR
  database](https://doi.org/10.1093/nar/gkaa902).
* [TerrestrialMetagenomeDB](https://webapp.ufz.de/tmdb), a public
  repository of curated and standardized metadata for terrestrial
  metagenomes, [paper in 2020 NAR dabase](https://doi.org/10.1093/nar/gkz994).
* [MicrobiomeDB](https://microbiomedb.org/), a systems biology platform for
  integrating, mining and analyzing microbiome experiments, can be used to
  identify experimental variables associated with changes in microbial 
  community structure. [paper in 2018 NAR database](https://doi.org/10.1093/nar/gkx1027).
* [MGnify](https://www.ebi.ac.uk/metagenomics/), formely EBI metagenomics, 
  provides a free to use platform for the assembly, anal- ysis and
  archiving of microbiome data derived from sequencing microbial
  populations that are present in particular environments. papar in 
  2020 NAR database](https://doi.org/10.1093/nar/gkz1035)
