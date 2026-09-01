# Variant-Interpretation-Algorithms
**Evaluation of Computational Tools for Predicting the Impact of Missense Variants**

Next generation sequencing generates thousands of genetic variants, and researchers develop various protocols with multiple parameters in order to classify them. This work shows some efforts to the computational exploration of algorithms underlying SIFT, PolyPhen-2, CADD, PROVEAN, SNP&GO, MutationAssessor, Align-GVGD, PANTHER, P-Mut, and related tools.

From sequencing of small DNA fragments to the identification of disease specific gene panel and today the WGS/ WES have enabled us to track the disease origin, targeted therapy and inherited diseases. The vast amount of data produced by these methods demands advanced expertise and significant computational resources to detect, analyze, and categorize genetic variants which can provide valuable scientific insights (Pereira et al., 2020).

The classification of genetic variants is a complex process that requires multiple levels of evidence, as recommended by ClinGen. In large scale sequencing studies, systematic filtering is crucial for evaluating candidate variants. To exclude those unlikely to be linked to the disease of interest, various filtering criteria should be applied. These include sequencing quality control, clinical evidence, population frequency, variants position in protein and their classification as synonymous, missense, frameshift, nonsense, in-frame or stop loss etc. Since not all prediction tools assess every variant type or location, selecting an appropriate set of tools for studied variants is crucial. Given that a large number of variants in sequencing data remain of unknown clinical significance, employing computational tools can aid in their characterization (De Oliveira Garcia et al., 2022).

Single nucleotide polymorphisms (SNPs) in protein coding regions can cause non-synonymous SNPs (nsSNPs), leading to missense variants that alter protein function. Predicting their disease relevance is challenging as they can disrupt functional sites, protein structure, folding or stability. However not all protein substitution are harmful. Unlike deletions or non-sense mutations with clear consequences, missense mutations are harder to classify, making them a key focus in genetic research (Thusberg et al., 2011). Since each program employs a unique algorithm making significantly different prediction about a variant. Although guidelines for using prediction tools is available, there are no standardized rule for their clinical validation and implementation (Richards et al., 2015).
As each method has its own strength and weakness so integrating multiple prediction tools is a logical approach to improving predictive accuracy (Sun & Yu, 2019).

References:

Pereira, R., Oliveira, J., & Sousa, M. (2020). Bioinformatics and computational tools for Next-Generation sequencing analysis in clinical genetics. Journal of Clinical Medicine, 9(1), 132. https://doi.org/10.3390/jcm9010132 

De Oliveira Garcia, F. A., De Andrade, E. S., & Palmero, E. I. (2022). Insights on variant analysis in silico tools for pathogenicity prediction. Frontiers in Genetics, 13, 1010327. https://doi.org/10.3389/fgene.2022.1010327 

Thusberg, J., Olatubosun, A., & Vihinen, M. (2011). Performance of mutation pathogenicity prediction methods on missense variants. Human Mutation, 32(4), 358–368. https://doi.org/10.1002/humu.21445 

Richards, S., Aziz, N., Bale, S., Bick, D., Das, S., Gastier-Foster, J., Grody, W. W., Hegde, M., Lyon, E., Spector, E., Voelkerding, K., & Rehm, H. L. (2015). Standards and guidelines for the interpretation of sequence variants: a joint consensus recommendation of the American College of Medical Genetics and Genomics and the Association for Molecular Pathology. Genetics in Medicine, 17(5), 405–424. https://doi.org/10.1038/gim.2015.30

Sun, H., & Yu, G. (2019). New insights into the pathogenicity of non-synonymous variants through multi-level analysis. Scientific Reports, 9(1), 1667. https://doi.org/10.1038/s41598-018-38189-9



**This repository contains original written work by the author. The work may be shared for non-commercial purposes with appropriate attribution, but derivative versions or modifications may not be distributed without permission.**

