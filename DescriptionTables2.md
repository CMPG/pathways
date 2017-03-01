Description of data tables that served as input for the 2DNS test as described in: **Inference of Evolutionary Forces Acting on Human Biological Pathways**. Daub et al. (2015). Genome Biol Evol. doi: 10.1093/gbe/evv083

- 2DNS_mut.txt
- 2DNS_gene.txt

-----------------------------------------------------------------------------
####2DNS_mut.txt
-----------------------------------------------------------------------------
(Added on March 1, 2017)

**Description:**
This file contains the list of polymorphic and fixed mutations

**Details:**

Description of the columns:

- **geneEnsemblID**: Ensemble gene ID
- **chr**: chromosome
- **pos**: position on chr (using build hg19)
- **N**: nonsynonymous mutation (0/1: yes/no)
- **S**: synonymous mutation
- **P**: polymorphic SNP
- **D**: fixed mutation (only fixed mutations located on the human branch!)
- **afrSNP**: SNP private to African populations
- **nonAfrSNP**: SNP private to non-African populations
- **sharedSNP**: SNP shared between African and non-African populations
- **SNPsGC**: SNP from Complete Genomics (GC). **Filter on (SNPsGC=1 & SNPs1000G=0) if you want to use the GC data set**. If fixed substitution: substitution is assessed by comparison with CG data set (if difference between human and chimp sequence is at same position as CG SNP and is the same as one of the alleles of this SNP, this will not count as fixed substitution, but as SNP)
- **SNPs1000G**: SNP from 1000G project. **Filter on (SNPsGC=0 & SNPs1000G=1) if you want to use the 1000G data set**. If fixed substitution: substitution is assessed by comparison with 1000G data set (if difference between human and chimp sequence is at same position as 1000G SNP and is the same as one of the alleles of this SNP, this will not count as fixed substitution, but as SNP)
- **covHC**: part of human chimp alignment. 
- **covCG**: part of exome fully sequenced in all 42 CG samples
- **cov1000G**: part of exome targeted by 1000G project

Filter on 2 or 3 of the *covxx* flags if you only want to use mutations that are located in the overlap of the covered genomic regions between the different projects.

Examples: Filter on **covHC=1 & covCG=1** if you require to only use mutations that are covered by both the human chimp alignment and that are part of the exome that is fully sequenced in all 42 CG samples (Table S11 in the paper). 
Flags **covCG=1 & cov1000G=1** were set for tables S6 and S7 in the paper

**References:**

Daub, J. T., Dupanloup, I., Robinson-Rechavi, M. & Excoffier, L. Inference of Evolutionary Forces Acting on Human Biological Pathways. Genome Biol Evol 7, 1546–1558 (2015).


-----------------------------------------------------------------------------
####2DNS_gene.txt
-----------------------------------------------------------------------------
(Added on March 1, 2017)

**Description:**
This file contains the list of genes, their lengths and chimp/mouse ortholog status

**Details:**

Description of the columns:

- **geneEnsemblID**: Ensemble gene ID
- **chr**: chromosome
- **length**: total exon length
- **cov.HC.CG.length**: total exon length covered by Human-Chimp alignment and all samples of Complete Genomics project
- **cov.HC.1000G.length**: total exon length covered by Human-Chimp alignment and 1000G project
- **cov.CG.1000G.length**: total exon length covered by all samples of Complete Genomics project and 1000G project
- **cov.HC.CG.1000G.length**: total exon length covered by Human-Chimp alignment, all samples of Complete Genomics project and the 1000G project
- **ChimpOrtholog**: gene has chimp ortholog
- **ChimpGeneStatus**: status of chimp ortholog
- **MouseGeneStatus**: status of mouse ortholog
- **KnownChimpOrMouseOrtholog**: does the gene has a chimp ortholog with status KNOWN or does it have a chimp ortholog and mouse ortholog where the mouse status is “KNOWN”. In our paper, we only used genes for which this value is TRUE.


Use the cov.xx.length exon lengths when you require mutations to fall within genomic overlap between parts of exome covered by 2 or 3 projects. See also the covHC, covCG, cov1000G flags in the table 2DNS_mut.txt.

**References:**

Daub, J. T., Dupanloup, I., Robinson-Rechavi, M. & Excoffier, L. Inference of Evolutionary Forces Acting on Human Biological Pathways. Genome Biol Evol 7, 1546–1558 (2015).
