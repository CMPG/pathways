Welcome to the CMPG Pathways/altitude repository

CONTENTS:

Data tables that served as input for the gene set enrichment analysis to detect pathways showing signals of adaptation to living in high altitudes, as described in:
Foll, M. et al., 2014. Widespread Signals of Convergent Adaptation to High Altitude in Asia and America. 
The American Journal of Human Genetics

altitude_snp_stat.txt 
altitude_gene_stat.txt

***********************************************************************************
altitude_snp_stat.txt (Added on March 2, 2016)
***********************************************************************************

DESCRIPTION:
This file contains the SNP selection scores.

DETAILS:

- Description of the columns:
snpID = internal SNPID
chr = chromosome (build hg19)
pos = chormosome position  (build hg19)
dbsnp = dbsnpID
stat.conv = selection score for convergent selection
stat.all = selection score for any selection

- The selection scores stat.conv is calculated as 1-qconv, where qconv is 
the q value of a SNP computed from the probability of convergent selection.
In the same way stat.all is calculated from 1-qall, where qall is the 
q value of a SNP computed from the probability of any selection model.


***********************************************************************************
altitude_gene_stat.txt (Added on March 2, 2016)
***********************************************************************************

DESCRIPTION:
This file contains the genes and their selection scores

DETAILS:

- Description of the columns:
geneEntrezID = Entrez gene ID
geneName = HUGO gene symbol
stat = selection score for convergent selection
dbsnp = dbsnpID for the SNP assigned to the gene
snpcnt = number of SNPs assigned to gene
bin = snpcnt bin (genes are assigned to bins according to their SNP density)
chr = chromosome (build hg19)
startpos = start position on chromosome (build hg19)
endpos = end position on chromosome (build hg19)
strand = 1 or -1
length = in bp, simply endpos - startpos

- The selection scores stat is calculated as 1-qconv, where qconv is 
the q value of a SNP computed from the probability of convergent selection.

REFERENCES:
Foll, M., Gaggiotti, O.E., Daub, J.T., Vatsiou, A., and Excoffier, L. (2014). 
Widespread Signals of Convergent Adaptation to High Altitude in Asia and America. 
The American Journal of Human Genetics

Daub JT, Hofer T, Cutivet E, Dupanloup I, Quintana-Murci L, Robinson-Rechavi M, Excoffier L. (2013) 
Evidence for Polygenic Adaptation to Pathogens in the Human Genome. Mol Biol Evol.



