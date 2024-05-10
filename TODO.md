## Overview

Our project involves analyzing genomic variant data (VCF files) to identify mutations 
associated with specific phenotypes. The goal is to create a predictive model 
that can accurately classify genetic variants based on their likelihood to 
contribute to the condition of interest, using primarily categorical data fields.


## Requirements:

VCF Data Processing: Implement a pipeline for reading and processing VCF (Variant Call Format) 
files to extract relevant genomic variant data. Experience with Hail or similar genomic data processing 
libraries is highly desirable.

Data Annotation: Annotate single nucleotide polymorphisms (SNPs) based on a provided list of known mutations, 
adding a binary flag to indicate the presence of a mutation of interest.

Data Preparation: Convert categorical data into a format suitable for machine learning models using OrdinalEncoder 
or a similar approach. The dataset is predominantly categorical, with a few continuous data fields.

Model Development: Develop a binary classifier that predicts whether a genetic variant is likely associated with 
the condition of interest. The model should use categorical features to predict a binary outcome (Yes/No) based 
on a predefined confidence threshold.


### Specific Tasks:

Task 1: Implement functionality to read VCF files using Hail or a similar library, 
converting them into a suitable format (e.g., DataFrame or MatrixTable) for analysis.

Task 2: Annotate the dataset with mutation information based on external metadata, 
marking SNPs with a binary flag to indicate mutation presence.

Task 3: Preprocess the dataset by converting all categorical data into integer arrays, 
preparing it for machine learning model input.

Task 4: Develop and train a binary classification model that can accurately predict the 
likelihood of a variant being associated with the condition, based on the processed and annotated data.

Continious variable example: https://github.com/Ancestry/VCFcontam/tree/main