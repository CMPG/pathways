Welcome to the CMPG Pathways repository

CONTENTS:

- HGDP_SNP_zval.txt (Added on April 30, 2013)

DESCRIPTION:
This file contains the z-scores calculated from global hierarchical FSTs of HGDP SNPs.

DETAILS:

- Description of the columns:
id = SNPID in our database
chr.hg18 = chromosome in hg18 build
pos.hg18 = chromosome position in hg18 build
dbsnp.hg18 = original dbsnpID 
fst = global hierarchical FST
pfst = probabilies fo the FST value compared to null distribution (left or right tail of distribution)
qfst = quantiles of the FST value compared to null distribution
chr.hg19 = chromosome after conversion to hg19 build
pos.hg19 = chromosome position after conversion to hg19 build
dbsnp.hg19 = dbsnpID after conversion to hg19 build
zval = z-score corresponding to qfst

- After conversion from hg18 to hg19, 194 SNPs couldn't not be mapped and were not used in further analysis.

- Before calculation of zscores, we rounded extreme low and high p.fst/q.fst values to 1e-7 or (1-1e-7) resp.
For all SNPs with p.fst < 1e-7 & q.fst > 1-(1e-7): we set p.fst = 1e-7, q.fst = 1-(1e-7)
For all SNPs with p.fst < 1e-7 & q.fst  1e-7: we set p.fst = 1e-7, q.fst = 1e-7
For all remaining SNPs with q.fst=1: we set q.fst = 1-p.fst


REFERENCES:
Excoffier L, Hofer T, Foll M. 2009. Detecting loci under selection in a hierarchically structured population. Heredity 103:285-298.
Hofer T, Foll M, Excoffier L. 2012. Evolutionary forces shaping genomic islands of population differentiation in humans. BMC Genomics 13:107.
Daub JT, Hofer T, Cutivet E, Dupanloup I, Quintana-Murci L, Robinson-Rechavi M, Excoffier L. Evidence for Polygenic Adaptation to Pathogens in the Human Genome. Mol Biol Evol.


