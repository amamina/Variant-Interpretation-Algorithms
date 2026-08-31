SIFT is a computational tool that distinguishes intolerant from tolerant amino acid substitutions by analyzing sequence homology. It works on the principle that evolution of protein is linked to its function. Certain amino acid positions are important for protein function and remain conserved in an alignment of protein family, while positions with less functional importance exhibit more variability (Ng & Henikoff, 2001).

SIFT begins its analysis with a query protein sequence and searches similar sequences from protein database such as SWISS-PROT, based on the observation that proteins with common ancestors tend to have similar sequences. The retrieved sequences are grouped if they share >90% identity in the aligned regions and a consensus sequence is generated for each group by selecting the most frequently occurring amino acids at each position. MOTIF algorithm (Henikoff & Henikoff, 1991; Smith & Smith, 1990) identifies conserved regions in the consensus sequence by comparing them to the query sequence. Conserved regions that share >90% identity are further grouped. A PSI-BLAST check point file is generated incorporating these conserved and consensus sequences serving as the starting dataset. Additional conserved sequences are incorporated to this only if they do not decrease conservation in the conserved region (Rc). Conservation at a given position c is quantified using:

$$
R_c = \log_2 20 - \sum_{a=1}^{20} p_a \log_2 p_a
$$

After multiple iteration highly conserved sequences tend to align globally with the query protein. The PSI-BLAST alignments are converted into a position specific scoring matrix (PSSM), which is lx20 matrix where l represents sequence length. Each matrix entry, pca, represents the probability of amino acid a at position c and is calculated as

$$
P_{ca} = \frac{N_c}{N_c + B_c}G_{ca} + \frac{B_c}{N_c + B_c}F_{ca}
$$

Where Nc is total number of sequences in alignment, gca is the sequence weighted frequency. fca represents pseudocounts (calculated from a 13-component Dirichlet mixture), and Bc is the total number of pseudocounts.

SIFT provided better performance than substitution scoring matrix BLOSSUM62 (Cargill et al., 1999) when tested against experimental data sets, where mutagenesis was performed across the entire protein including LacI (Markiewicz et al., 1994), HIV 1 Protease (Loeb et al., 1989) and Bacteriophage T4 lysozyme (Rennell et al., 1991). To streamline SIFT’s automation a single cutoff is applied to all PSSM columns. In order to avoid misclassification of highly variable positions as deleterious, pca values are normalized using consensus amino acid in each column. Positions with normalized probabilities below 0.05 are predicted to be deleterious, while those greater than or equal to 0.05 are predicted to be tolerated (Sim et al., 2012).

References: 

Ng, P. C. (2003). SIFT: predicting amino acid changes that affect protein function. Nucleic Acids Research, 31(13), 3812–3814. https://doi.org/10.1093/nar/gkg509 

Henikoff, S., & Henikoff, J. G. (1991). Automated assembly of protein blocks for database searching. Nucleic Acids Research, 19(23), 6565–6572. https://doi.org/10.1093/nar/19.23.6565 

Smith, R. F., & Smith, T. F. (1990). Automatic generation of primary sequence patterns from sets of related protein sequences. Proceedings of the National Academy of Sciences, 87(1), 118–122. https://doi.org/10.1073/pnas.87.1.118

Cargill M, Altshuler D, Ireland J, Sklar P, Ardlie K, Patil N, Lane C, Lim EP, Kalyanaraman N, Nemesh J, et al. Characterization of single-nucleotide polymorphisms in coding regions of human genes. Nat Genet. 1999;22:231–238. doi: 10.1038/10290

Markiewicz P, Kleina L, Cruz C, Ehret S, Miller JH. Genetic studies of the lac repressor XIV. Analysis of 4000 altered Escherichia coli lac repressors reveals essential and non-essential residues, as well as “spacers” which do not require a specific sequence. J Mol Biol. 1994;240:421–433. doi: 10.1006/jmbi.1994.1458

Loeb DD, Swanstrom R, Everitt L, Manchester M, Stamper SE, Hutchison CA., III Complete mutagenesis of the HIV-1 protease. Nature. 1989;340:397–400. doi: 10.1038/340397a0 

Rennell D, Bouvier SE, Hardy LW, Poteete AR. Systematic mutation of bacteriophage T4 lysozyme. J Mol Biol. 1991;222:67–87. doi: 10.1016/0022-2836(91)90738-r 

Sim, N., Kumar, P., Hu, J., Henikoff, S., Schneider, G., & Ng, P. C. (2012). SIFT web server: predicting effects of amino acid substitutions on proteins. Nucleic Acids Research, 40(W1), W452–W457. https://doi.org/10.1093/nar/gks539 
