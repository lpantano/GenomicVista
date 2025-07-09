# GTEx Data Download

Download data from GTEX (https://www.gtexportal.org/home/downloads/adult-gtex/bulk_tissue_expression#bulk_tissue_expression-gtex_analysis_v10-rna-seq) and store it in the `gtex_bulk_tissue_expression` directory.

```{bash}
mkdir -p gtex_bulk_tissue_expression
# 	Gene Expression Read Counts from RNASeQCv2.4.2.
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_reads.gct.gz
# Gene Expression Transcripts Per Million (TPM) from RNASeQCv2.4.2.
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm.gct.gz
# 	Gene Expression Transcripts Per Million (TPM) from RNASeQCv2.4.2. This file contains all the Laser Capture Microdissection (LCM) samples.
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm_lcm.gct.gz
# Median gene-level TPM by tissue. Median expression was calculated from the file GTEx_Analysis_v10_RNASeQCv2.4.2_gene_tpm.gct.gz
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RNASeQCv2.4.2_gene_median_tpm.gct.gz
# Exon-exon junction read counts from STARv2.7.10a.
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_STARv2.7.10a_junctions.gct.gz
# Expressed Transcript read counts from RSEMv.1.3.3.
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RSEMv1.3.3_transcripts_expected_count.txt.gz
# Transcript TPMs (matrix of 19788 samples as named in each column by 244940 transcripts as named in each row) from RSEMv.1.3.3.
pixi run wget -P gtex_bulk_tissue_expression https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/GTEx_Analysis_v10_RSEMv1.3.3_transcripts_tpm.txt.gz
```

# GTEx Reference Download

Download gene-level GTF files based on the GENCODE 39 transcript model, where isoforms were collapsed to a single transcript per gene. Store it in the `gtex_reference` directory.

```{bash}
mkdir -p gtex_reference
pixi run wget -P gtex_reference https://storage.googleapis.com/adult-gtex/references/v10/reference-tables/gencode.v39.GRCh38.genes.gtf
```

# GTEx Metadata Download

Download metadata files that contain sample attributes and subject phenotypes. Store it in the `gtex_metadata` directory.

```{bash}
mkdir -p gtex_metadata
# A de-identified, open access version of the sample annotations available in dbGaP.
pixi run wget -P gtex_metadata https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SampleAttributesDS.txt
# A data dictionary that describes each column in the GTEx_Analysis_v10_Annotations_SampleAttributesDS.txt.
pixi run wget -P gtex_metadata https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SampleAttributesDD.xlsx
# 	A de-identified, open access version of the subject phenotypes available in dbGaP.
pixi run wget -P gtex_metadata https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SubjectPhenotypesDS.txt
# 	A data dictionary that describes each column in the GTEx_Analysis_v10_Annotations_SubjectPhenotypesDS.txt.
pixi run wget -P gtex_metadata https://storage.googleapis.com/adult-gtex/annotations/v10/metadata-files/GTEx_Analysis_v10_Annotations_SubjectPhenotypesDD.xlsx

```