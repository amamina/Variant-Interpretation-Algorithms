**Protein variation effect analyzer (PROVEAN, v1.1)** is an algorithm that predicts the functional effects of single or multiple amino acid substitutions, insertion and deletion. It was tested on large dataset of both human and non-human protein variation obtained from UniProt, and mutagenesis based experimental datasets from the human tumor suppressor protein TP53, and ATP binding
cassette transporter 1 protein ABCA1. Predictive ability of PROVEAN was highly significant as compared to other popular tools.

It operates on the principle that pairwise sequence alignment scores measures similarity between homologous or related sequences, so any variation that cut down similarity is more likely to cause a damaging effect. This effect is quantified by delta alignment score:


$$
\Delta(Q, V, S) = A(Q', S) - A(Q, S)
$$


Where Q is query sequence, S represents another protein, and V is the variation. Delta score can be used to measure the effect of a variation as low delta score indicates deleterious effects on protein function. While high delta score indicates neutral effects on function of protein. Delta score is advantageous over other scores as it utilizes substitution matrix to assess amino acid changes based on substitution frequency and chemical properties also it is calculated using alignment scores from both flanking regions specifically if the mutation disrupts alignment in gapped regions (Choi et al., 2012). The PROVEAN score uses a default cutoff of -2.5; variants with score less than or equal to this threshold are considered detrimental while higher scores are considered neutral.

Reference:

Choi, Y., Sims, G. E., Murphy, S., Miller, J. R., & Chan, A. P. (2012). Predicting the functional effect of amino acid substitutions and indels. PLoS ONE, 7(10), e46688. https://doi.org/10.1371/journal.pone.0046688
