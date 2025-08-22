# Environment Setup for GTEx Bulk Tissue Expression Data

This document provides instructions for downloading and organizing the GTEx bulk tissue expression data, reference files, and metadata. The data will be stored in specific directories for easy access and analysis.

# pixi Environment Setup

Ensure you have the `pixi` tool installed and configured in your environment. This tool will be used to run commands for downloading the data.
To install the libraries needed to run the code in this repository, you can use the following command: `pixi install`

# GTEx Bulk Tissue Expression Data 

| File description                                                                                                                          | file name                                           | url                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Gene Expression Read Counts from RNASeQCv2.4.2.                                                                                           | GTEx_Analysis_v10_RNASeQCv2.4.2_gene_reads.gct.gz   | https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_reads.gct.gz   |
| Gene Expression Transcripts Per Million (TPM) from RNASeQCv2.4.2.                                                                         | GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm.gct.gz     | https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm.gct.gz     |
| Gene Expression Transcripts Per Million (TPM) from RNASeQCv2.4.2. This file contains all the Laser Capture Microdissection (LCM) samples. | GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm_lcm.gct.gz | https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm_lcm.gct.gz |
| Median gene-level TPM by tissue. Median expression was calculated from the file GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm.gct.gz           |                                                     |                                                                                                                    |
|                                                                                                                                           |                                                     |                                                                                                                    |
|                                                                                                                                           |                                                     |                                                                                                                    |

# GTEx Reference File

The gene-level GTF files based on the GENCODE 39 transcript model, where isoforms were collapsed to a single transcript per gene. It can be found at the following URL: [https://storage.googleapis.com/adult-gtex/references/v10/reference-tables/gencode.v39.GRCh38.genes.gtf]

# GTEx Metadata Download

Metadata files that contain sample attributes and subject phenotypes.

| File description                                                                                           | file name                                              | url                                                                                                                             |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| A de-identified, open access version of the sample annotations available in dbGaP.                         | GTEx_Analysis_v10_Annotations_SampleAttributesDS.txt   | https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SampleAttributesDS.txt   |
| A data dictionary that describes each column in the GTEx_Analysis_v10_Annotations_SampleAttributesDS.txt.  | GTEx_Analysis_v10_Annotations_SampleAttributesDD.xlsx  | https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SampleAttributesDD.xlsx  |
| A de-identified, open access version of the subject phenotypes available in dbGaP.                         | GTEx_Analysis_v10_Annotations_SubjectPhenotypesDS.txt  | https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SubjectPhenotypesDS.txt  |
| A data dictionary that describes each column in the GTEx_Analysis_v10_Annotations_SubjectPhenotypesDS.txt. | GTEx_Analysis_v10_Annotations_SubjectPhenotypesDD.xlsx | https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SubjectPhenotypesDD.xlsx |