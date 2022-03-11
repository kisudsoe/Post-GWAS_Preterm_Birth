# Post-GWAS_Preterm_Birth
This is a repository for the results from post-GWAS analysis for preterm birth



## Files and contents in directory

Candidate SNPs:

* **GWAS_catalog**: TSV files of 3 phenotypes, EFO_0003917-premature birth, EFO_006917-spontaneous preterm birth, and MONDO_0012511-preterm premature rupture of the membranes, downloaded from the GWAS Catalog DB (https://www.ebi.ac.uk/gwas/). And their pivot tables for SNPs (\*\_snp.tsv), studies (\*\_study.tsv), and traits (\*\_trait.tsv).
* **ldlink**: LD-linked SNP lists of 109 lead SNPs downloaded from LDlink DB (https://ldlink.nci.nih.gov/?tab=home).
* LD_116_1E-05.tsv: A list of lead SNPs and their population information corresponding the 1000 Genomes project.
* gwas_ldlink_total.tsv: A combined list of lead SNPs and their LD-linked SNPs pairs retrieved from the LDlink DB.
* gwas_biomart_2443.tsv: A list of 2,443 candidate SNPs before removing an ALU element and an obsolete SNP rs72385215.
* gwas_biomart_2441.bed: A list of 2,441 candidate SNPs for preterm birth to input the Post-GWAS analysis pipeline.
* bedtools_closest_gencode_TSS.tsv: Bedtools closest result from candidate SNPs and gene TSS (Gencode V39, Grch37; https://www.gencodegenes.org/human/release_39lift37.html).
* run-analysis.sh: This is a script to run the post-GWAS analysis program (https://github.com/kisudsoe/PostGWAS-tools).

Roadmap epigenomics:

* **roadmap_18_status**: Bedtools intersect result TSV files from candidate SNPs and Roadmap ChromHMM 18 status results by 98 tissues and cells (https://egg2.wustl.edu/roadmap/web_portal/chr_state_learning.html).
* **roadmap_18_status_bed**: Lists of SNPs in BED format by the Roadmap ChromHMM 18 status
* **enrich**: Permutation test results of 66 SNPs (overlap-2), 18 SNPs (overlap-1), and 228 SNPs (Roadmap & ENCODE), including numbers of overlapped SNPs (\*\_overlap.tsv), p-value (\*\_pval.tsv), and z-score (\*\_zscore.tsv).

ENCODE:

* **encode_tsv**: Bedtools intersect result TSV files from candidate SNPs and ENCODE TFBS ChIP-seq results by 89 cells [wgEncodeRegTfbsClusteredWithCellsV3.bed.gz](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/encodeDCC/wgEncodeRegTfbsClustered/).
* **encode_bed**: Lists of SNPs in BED format by 89 cells of ENCODE TFBS ChIP-seq results.

GTEx:

* **gtex_eqtl**: List of SNPs in BED format by 30 tissues of GTEx database (https://gtexportal.org/home/).

Sakabe et al., 2020:

* **Sakabe_et_al_2020**: Original data of ATAC-seq (countsTable-ATAC.785578.tsv), ChIP-seq (H3K4me3, countsTable-H3K4me3.785840.tsv; H3K4me1, countsTable-H3K4me1.785803.tsv; and H3K27ac, countsTable-H3K27ac.785754.tsv), and pcHi-C (interactions.786677.ibed)
* **Sakabe_processed**: Bedtools intersect results from the original data of Sakabe_et_al_2020. [Results from ATAC-seq and ChIP-seq data will be added soon.]

Summary:

* **genome_tsv**: A collection of bedtools intersect results by data and uniset function results from the post-GWAS analysis.
* **summary_bed**: Lists of SNPs in BED format by SNP groups.
* log-\*.txt files: Program log files generated from the post-GWAS analysis.
