# tcga-endometrial-hotspot
Somatic mutational analysis and clinical hotspot report for a POLE ultra-mutated endometrial carcinoma patient using TCGA data.
# Background 
Endometrial carcinoma can be molecularly subtyped based on mutational profile, with a subset of tumors characterized by mutations in POLE, the gene encoding the catalytic subunit of DNA polymerase epsilon. POLE mutations result in a defective proofreading mechanism, leading to an ultra-mutator phenotype with thousands of somatic variants. While this exceptionally high tumor mutational burden complicates the identification of individual driver mutations, POLE ultra-mutated tumors are associated with distinct clinical behavior and may have implications for immunotherapy response. This analysis characterizes the mutational landscape of a single POLE ultra-mutated endometrial carcinoma patient (TCGA-A5-A0G2) within the context of a high-TMB endometrial carcinoma cohort.
# Data Source 
Data were obtained from the TCGA Uterine Corpus Endometrial Carcinoma (UCEC) dataset via cBioPortal. Two files are required to reproduce this analysis:

- data_mutations.txt — somatic mutation annotation file (MAF format)
- ucec_tcga_gdc_clinical_data.tsv — clinical metadata

Dataset available at: https://www.cbioportal.org/study/summary?id=ucec_tcga_gdc

# Analysis Overview (Jupyter notebook) 
- Filters the TCGA UCEC cohort to patients with tumor mutational burden ≥10,000 somatic variants
- Identifies the most frequently mutated genes across the high-TMB cohort
- Isolates POLE mutations and visualizes their frequency across the cohort via lollipop plot
- Confirms presence of clinically significant driver mutations in the patient of interest
- Identifies TP53 co-mutations and their functional classifications

# Key Findings
Patient TCGA-A5-A0G2 harbors 22,936 somatic variants, consistent with a POLE ultra-mutator phenotype driven by the pathogenic POLE V411L mutation. A co-occurring TP53 S241F mutation, located in the DNA-binding domain, results in loss of p53 tumor suppression function and is associated with the aggressive serous histological subtype. The probable mutational ordering (POLE-driven genome instability preceding TP53 loss) is discussed in the accompanying clinical hotspot report.

# Requirements 
- Python 3.8+
- pandas
- matplotlib
