# HCC RNA-seq Analysis Pipeline

## Overview
This repository contains a Google Colab notebook for exploring an RNA-sequencing analysis workflow using gene-expression data from The Cancer Genome Atlas (TCGA) through the Genomic Data Commons (GDC) API.

The notebook demonstrates downloading gene-expression files, extracting gene-level information, combining multiple samples into a gene-expression matrix, filtering genes based on expression thresholds, and applying a log₂ transformation.

## Objectives
- Retrieve genomic data files using the GDC API.
- Extract gene identifiers, gene names, and expression-count information.
- Combine multiple samples into a common gene-expression matrix.
- Filter genes with low expression.
- Apply a log₂(x + 1) transformation to expression values.
- Inspect intermediate data structures and outputs.

## Tools and Libraries
The notebook uses Python and the following libraries:

- **Pandas:** Data manipulation and tabular data processing.
- **NumPy:** Numerical operations and mathematical transformations.
- **Requests:** HTTP requests for downloading files from the GDC API.
- **Scanpy and AnnData:** Structured storage and processing of gene-expression data.
- **Matplotlib and Seaborn:** Data visualization.
- **GEOparse:** Accessing and parsing GEO datasets.
- **Lifelines:** Survival analysis and Cox proportional hazards modeling.

The use and suitability of each library depend on the relevant notebook steps.

## Workflow
1. Retrieve file identifiers from a data source.
2. Download gene-expression files from the GDC API.
3. Read the files into Pandas DataFrames.
4. Retain gene-level records and standardize Ensembl gene identifiers.
5. Merge expression data from multiple samples.
6. Filter genes based on expression thresholds.
7. Apply a log₂(x + 1) transformation.
8. Inspect the resulting data and proceed with subsequent analyses as implemented in the notebook.

## Running the Notebook
1. Open `HCC_RNAseq_Pipeline_Colab.ipynb` in Google Colab.
2. Execute the cells in the intended order.
3. Ensure the required Python packages are installed.
4. Verify that the GDC API requests succeed and that downloaded files have the expected format.
5. Inspect intermediate outputs and confirm that sample selection, gene identifiers, and expression values are handled correctly.

## Validation Notes
This repository is being examined to assess the technical execution and scientific suitability of its analysis steps. Successful execution alone does not establish that the pipeline is scientifically valid.

Particular attention should be given to sample selection, HTTP response validation, duplicate gene identifiers, gene loss during merging, and the suitability of normalization and transformation methods for the input data.

## Status
Under review. The complete workflow and its biological conclusions should not be considered validated until the relevant checks have been completed.

## Disclaimer
This notebook is intended for research and educational purposes. Results should be interpreted in accordance with the underlying data, analysis methods, and validation results.
