PolyPhen-2 predicts the effect of missense mutations. It differs from earlier version of PolyPhen (Ramensky et al., 2002) as it incorporates three structure-based and eight sequence-based predictive features through an iterative greedy algorithm and optimizes multiple sequence alignment. It compares properties and functional importance of allele replacement from wild to mutant type using naive Bayes classifier by calculating posterior probabilities. One of its most significant predictive feature assess the likelihood of two human alleles on amino acid replacement pattern in multiple sequence alignment; evolutionary distance between the protein showing the first deviation from wild type protein or whether the mutation arose in hypermutable site (Adzhubei et al., 2010).

Polyphen-2 is designed using two pairs of training and testing datasets: HumDiv and HumVar. The former includes 3,155 UniProt annotated damaging alleles, associated with Mendelian diseases along with 6,321 non-damaging human proteins and their closely related homologs. The latter pair consists of 13,032 disease causing mutations from UniProt and 8,946 non-damaging human nsSNPs.

It uses 11 predictive features out of 19 sequence based and 13 structure based machine learning approaches. Irrelevant features can reduce classifier performance. Both classifier testing and feature selection is done in 5-fold cross validation where folds are not randomized but created to make sure that mutation in same protein would fall into same fold. After initial testing on HumDiv, HumVar was also used to further improvement of retained features and classifier. Feature selection is done by both forward selection and backward elimination. In the forward greedy approach, features are added continuously based on each’s feature solo performance until there is no further increment in prediction accuracy during cross-validation. Prediction accuracy is determined by area under the ROC curve (AUC), which represents integral of sensitivity across all specificity cutoffs. Conversely in backward elimination process features are systematically removed until a decline in prediction accuracy occurs. Final feature selection is further refined by assessing their performance on holdout HumVar datasets. Both approaches led to the 11 feature selection as stated below:


**Sequence based features:**

1. PSIC score of wild type amino acid
2. PSIC score difference between wild type and mutant amino acid
Positon specific independent counts (PSIC) (Sunyaev et al., 1999) estimates the likelihood of an amino acid occupying a specific position in a protein sequence based on substitution pattern. PSIC algorithm incorporates sequence relatedness and prior probabilities from BLOSSUM 62 matrix.
4. Sequence identity to closest homologue
5. Congruency of the mutant allele to the multiple alignment. For each amino acid sequence identity between analyzed protein and its closest homologue is computed.
6. CpG Context
7. Alignment depth (excluding gaps)
8. Change in amino acid volume between wild type and mutant type
9. Site of the mutation residues in Pfam domain

**Structural features:**

1. The accessible surface area of wild type amino acid
2. Change in the hydrophobic propensity
3. Crystallographic B-factor reflecting conformational mobility of the wild type amino acid residue.

Classification method is based on supervised machine learning Naïve Bayes, coupled with entropy discretization. This classifier has several advantages, as it is simple and does not require complex hyperparameters. It relies only on factored probabilities and smoothening, which is performed using Laplace estimator to predict the likelihood of mutation being damaging. It efficiently handles complex, mixed data types (both discrete and continuous features) and scattered missing values. A mutation is classified as “probably damaging” if its probabilistic score exceeds 0.85, and “possibly damaging” if score is above 0.15, and benign for lower scores.

References:

Ramensky, V. (2002). Human non-synonymous SNPs: server and survey. Nucleic Acids Research, 30(17), 3894–3900. https://doi.org/10.1093/nar/gkf493 

Adzhubei, I., Jordan, D. M., & Sunyaev, S. R. (2013). Predicting functional effect of human missense mutations using PolyPhen‐2. Current Protocols in Human Genetics, 76(1), Unit7.20. https://doi.org/10.1002/0471142905.hg0720s76 

Sunyaev, S. R., Eisenhaber, F., Rodchenkov, I. V., Eisenhaber, B., Tumanyan, V. G., & Kuznetsov, E. N. (1999). PSIC: profile extraction from sequence alignments with position-specific counts of independent observations. Protein Engineering Design and Selection, 12(5), 387–394. https://doi.org/10.1093/protein/12.5.387


