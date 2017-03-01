Description of data tables that served as input for the gene set enrichment analysis, as described in: 
**Evidence for Polygenic Adaptation to Pathogens in the Human Genome**. Daub et al. (2013). 
Mol Biol Evol. doi: 10.1093/molbev/mst080

- HGDP_SNP_zval.txt
- biosys.tsv
- biosys_gene.tsv
- gene_entrez.tsv



-----------------------------------------------------------------------------
####HGDP_SNP_zval.txt 
-----------------------------------------------------------------------------
(Added on April 30, 2013)

**Description:**
This file contains the z-scores calculated from global hierarchical FSTs of HGDP SNPs.

**Details:**

Description of the columns:

- **id**: SNPID in our database
- **chr.hg18**: chromosome in hg18 build
- **pos.hg18**: chromosome position in hg18 build
- **dbsnp.hg18**: original dbsnpID in hg18 build
- **fst**: global hierarchical FST
- **pfst**: probabilies of the FST value compared to null distribution (left or right tail of distribution)
- **qfst**: quantiles of the FST value compared to null distribution
- **chr.hg19**: chromosome after conversion to hg19 build
- **pos.hg19**: chromosome position after conversion to hg19 build
- **dbsnp.hg19**: dbsnpID after conversion to hg19 build
- **zval**: z-score corresponding to qfst

During conversion from hg18 to hg19 build, 194 SNPs could not be mapped and were not used in further analysis.

Before calculation of z-scores, we rounded extreme low and high pfst/qfst values to 1e-7 or (1-1e-7) resp.:

	For all SNPs with pfst < 1e-7 & qfst > 1-(1e-7): we set qfst: 1-(1e-7)
	For all SNPs with pfst < 1e-7 & qfst < 1e-7: we set qfst: 1e-7
	For all remaining SNPs with qfst=1: we set qfst: 1-pfst


**References:**

Excoffier L, Hofer T, Foll M. 2009. Detecting loci under selection in a hierarchically structured population. Heredity 103:285-298.

Hofer T, Foll M, Excoffier L. 2012. Evolutionary forces shaping genomic islands of population differentiation in humans. BMC Genomics 13:107.

Daub JT, Hofer T, Cutivet E, Dupanloup I, Quintana-Murci L, Robinson-Rechavi M, Excoffier L. 2013. Evidence for Polygenic Adaptation to Pathogens in the Human Genome. Mol Biol Evol. doi: 10.1093/molbev/mst080


-----------------------------------------------------------------------------
####biosys.tsv 
-----------------------------------------------------------------------------
(Added on July 2, 2014)

**Description:**
This file contains the gene sets downloaded from the NCBI Biosystems database on March 23, 2011

**Details:**

Description of the columns:

- **setBiosysID**: gene set ID in Biosystems 
- **setSourceID**: gene set ID in source database
- **setName**: gene set name
- **setSource**: source database

**References:**

Daub JT, Hofer T, Cutivet E, Dupanloup I, Quintana-Murci L, Robinson-Rechavi M, Excoffier L. 2013. Evidence for Polygenic Adaptation to Pathogens in the Human Genome. Mol Biol Evol. doi: 10.1093/molbev/mst080

Geer LY, Marchler-Bauer A, Geer RC, Han L, He J, He S, Liu C, Shi W, Bryant SH. 2010. The NCBI BioSystems database. Nucleic Acids Res. 38:D492–D496.

-----------------------------------------------------------------------------
####biosys_gene.tsv 
-----------------------------------------------------------------------------
(Added on July 2, 2014)

**Description:**
This file contains the list of genes and the gene set(s) they are part of
downloaded from the NCBI Biosystems database on March 23, 2011

**Details:**

Description of the columns:

- **setBiosysID**: gene set ID in Biosystems	
- **geneEntrezID**: Entrez gene ID

**References:**

Daub JT, Hofer T, Cutivet E, Dupanloup I, Quintana-Murci L, Robinson-Rechavi M, Excoffier L. 2013. Evidence for Polygenic Adaptation to Pathogens in the Human Genome. Mol Biol Evol. doi: 10.1093/molbev/mst080

Geer LY, Marchler-Bauer A, Geer RC, Han L, He J, He S, Liu C, Shi W, Bryant SH. 2010. The NCBI BioSystems database. Nucleic Acids Res. 38:D492–D496.

-----------------------------------------------------------------------------
####gene_entrez.tsv
-----------------------------------------------------------------------------
 (Added on July 2, 2014)

**Description:**
This file contains the list of genes downloaded from the NCBI gene database on January 4, 2012

**Details:**

Description of the columns:

- **chr**: chromosome
- **geneEntrezID**: Entrez gene ID
- **startpos**: start position on chromosome
- **endpos**: end position on chromosome
- **strand**: 1 or -1
- **symb**: gene symbol
- **multi_loc**: did we find multiple start and end positions?
- **length**: in bp, simply endpos - startpos

**References:**

Daub JT, Hofer T, Cutivet E, Dupanloup I, Quintana-Murci L, Robinson-Rechavi M, Excoffier L. 2013. Evidence for Polygenic Adaptation to Pathogens in the Human Genome. Mol Biol Evol. doi: 10.1093/molbev/mst080

Maglott D, Ostell J, Pruitt KD, Tatusova T. 2011. Entrez Gene: gene-centered information at NCBI. Nucleic Acids Res. 39:D52–D57

