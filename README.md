# CRISPRomESKAPE

### Scripts for the paper "Analysis of bacterial pangenomes reduces CRISPR dark matter and reveals strong association between membranome and CRISPR-Cas systems
"
published in Science Advances: https://doi.org/10.1126/sciadv.add8911

In this project we have searched for genes associated with CRISPR-Cas systems from bacteria of the ESKAPE group using Random Forest and we have been able to reduce the percentage of CRISPR black matter, as well as to propose a triad 'Membrane Proteins - Phages - CRISPR' by which bacterial genomes would acquire CRISPR-Cas systems when they have certain useful membrane proteins that can act as viral receptors.

## Python scripts
Package versions:
matplotlib 3.5.0
numpy 1.19.2
pandas 1.3.5
scikit-learn 1.0.2
scipy 1.6.2
seaborn 0.11.2
### Random forest inference
The script utilizes scikit-learns mean decrease in impurity feature importance measre to infer genes that set crispr containing strains apart from those without crispr systems. Cas-genes have been removed in the data, to allow to detect non Crispr-Cas related genes. 
### Jaccard distances
This script computes the Jaccard dissimilarity between the MLST groups which is used as distance measurement for a hierarchical clustering and dendrograms available in the papers supplementary data.
### Correlation plot
This script uses the Jaccard indices of the jaccard-panel.py script, so the latter needs to be run beforehand. It plots the correlation plot featured in the paper. 

## Perl scripts
**addColumnFromABfile.pl**  
Create an output to add to the metadata table, from a file with 2 columns: metadata ID.

**addColumnsFromABfile.pl**  
Creates an output with several columns to add to the metadata table, from a list of files, each with a list of IDs.

**analyseSpacers.pl**  
Calculate proportions of genomes with unique spacer/phages in two different clusters.

**calculatePercentGenesInStrainsID.pl**  
Calculate both absolute and relative frequency of pangenome genes in two clusters of genomes.

**collectGFFMetadata.pl**  
Collect all the information of the different strains and groups them in a final table

**countGenesAndShareGenesFromPangenome.pl**  
Count genes and average number of shared genes for each genome in the pangenome.

**createComparisonMatrix.pl**  
Create matrix for heatmaps comparing genes vs genomes.

**createMatrixPresenceAbsence.pl**  
Create gene presence/absence matrix.

**delete_FP.pl**  
Identify false positives by comparing spacers and direct repeats

**extractSpacers.pl**  
Extract spacers with evidence code 4 from CRISPRCasFinder results.

**filterBlast_vs_db.pl**  
Filter Blast hits with a given identity and subject coverage.

**filter_spacers_vsall.pl**  
Filter the results obtained from the comparison of spacers with different databases

**find_cluster_cas.pl**  
Find cas gene cluster from ccfinder results

**getGroupsFromPangenome.pl**  
Count appearances of each gene in the pangenome.

**joinGFFwithCRISPR_v2.pl**  
Prepare contigs from each genome as a string of gene names.

**phage_vs_spacers.pl**  
Compare a list of spacers against a phages database.

**putSma3sGenenames2roaryClusters.pl**  
Modify gene names assigned by Sma3s to avoid redundant names.

**removeAssemblies.pl**  
Check assembly files and remove those from GenBank when RefSeq is available. 
