# Genotyping-by-sequencing-in-Lolium-multiflorum
GBS Work Applied to Lolium multiflorum November 2026 — 100 accessions from Amazonas, Peru
# Description of the research work on Lolium multiflorum
Ryegrass samples had previously been collected in Chachapoyas, Pomacochas, Cajamarca, Bongora, and Luya.
# DNA Extraction and Genotyping by Sequencing
Ryegrass leaves were collected following the protocol described by Bobadilla et al., 2026 (https://doi.org/10.3389/fpls.2026.1818688) and genotyping by sequencing was performed according to the sequencing standards of (https://doi.org/10.1371/journal.pone.0090346)
# Bioinformatics Analysis
The bioinformatics analysis was performed using the TASSEL v5 pipeline on an HPC system, utilizing Rmarkdown templates for the analyses
# GBS Data Validation
For the analysis, we used the VCFtools v0.1.17 tool (Minor Allele Frequency), with the following filters: MAF > 0.05, missing data ≤ 0.1, and MAC (Minor Allele Count) ≥ 3 . In addition, the cyvcf2 and scikit-allel tools were used to perform linkage disequilibrium analysis with r² = 0.5 using Python v3.12.3.
# Analysis of population structure and genetic diversity
The poppr and adegenet tools were used for AMOVA analysis, and ade4 was used to perform 999 permutations. Additionally, ADMIXTURE was used to perform population structure analysis with k ranging from 1 to 20, with 10 replications. Furthermore, the vcfR, adegenet, hierfstat, ggplot2, ggExtra, tidypopgen and AGHmatrix packages were used to perform analyses of genetic diversity and genetic structure.
# Phylogenetic analysis
For the phylogenetic analysis, the cleaned SNPs that passed the filters were used to construct the phylogenetic tree using PGPGspider, RAXmlHPC, ggtree, ggtreeExtra, and ANNOVAR to visualize the phylogenetic tree, specifying its K-structures with the specific SNPs previously annotated to determine the genetic population of ryegrass.
# Genetic Similarity Networks
For the analysis of genetic similarity networks, we used the previous results from the G matrix of AGHmatrix, along with the igraph package
