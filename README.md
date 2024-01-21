# GenomeMLModels

## Introduction
This project aims to generate usable machine learning models for clinical datasets. Clinical datasets generated through several generations of improvements in bioinformatics in the past decade hold potentially missed findings. Easy sifting through years of data is complex due to evolving data structures and new reference databases. Better sequencing speeds and prices generate ever larger amounts of data for clinical analysis.

The project incorportes the Hail (https://hail.is/) data handling layer enabling VCF/gVCF input that coerces tabular data from different generation datasets: https://github.com/OligoGeneticDiseases/gen-toolbox. An example model will be trained on the Illumina Trusight Cancer(TM) and Trusight(TM) Hereditary Cancer panel VCFs. The dataset contains known pathogenic monogenic variants causative for hereditary cancer types (e.g. breast cancer). The final model is expected to annotate variants in new VCFs for potential pathogenicity based on input phenotype (i.e. breast cancer - hereditary). A decision boundary will be selected for single high probability variants. This tool would enable to quickly downselect a large number of variants or even tag batches of VCF files for potential monogenic variants. This project serves as the proof-of-concept for machine learning on genomic datasets using the aforementioned libraries.

## Data structure
Most VCFs of different generations can be re-annotated with up-to-date frequency data using VEP. This project expects all VCFs or gVCFs to have the genotype caller allele data, VEP annotations for IMPACT, MAX_AF, HGNC_ID, (HPO phenotype terms) available. All columns are converted into features available to the model. 

## Boosted decision tree
A boosted decision tree will be used as the base model for simple tabular containing both strings and float values using available open source machine learning frameworks.
