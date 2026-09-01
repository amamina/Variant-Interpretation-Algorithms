**SNP&GO is a web server that is based on a support vector machine (SVM) **classifier used to predict single amino acid polymorphism (SAP). It uses either a function and sequence-based method (SVM-SEQ) or a structure-based method (SVM-3D), with the latter providing a 3% higher accuracy (Capriotti & Altman, 2011). The input support vector also incorporates the Gene. SVM categorize mutations as either disease-related (output set to 0) and neutral polymorphisms (output set to 1). The decision threshold remains at 0.5 to enhance accuracy. 

Multiple factors are incorporated, including a function based log-odds score calculated from GO (gene ontology) classification and prediction data from PANTHER classification system. The final input vector comprises of 52 values: 40 values represents mutation-specific and local sequence information, four components capture sequence profile based features with an additional bit indicating features presence, four values indicating PANTHER based parameters with one bit indicating their features, and two values indicate the GO log-odds score (LGO) with a binary flag indicating its presence (Calabrese et al., 2009).

Along with results based on its SVM algorithm, this tool also provides data for missense amino acid substitutions using the PANTHER algorithm and PHD-SNP methods. If a variant shows an output greater than or equal to default threshold of 0.5, it is considered deleterious; if the score is less than 0.5, it is considered neutral.

ReferenceS:

Capriotti, E., Calabrese, R., Fariselli, P., Martelli, P., Altman, R. B., & Casadio, R. (2013). WS-SNPs&GO: a web server for predicting the deleterious effect of human protein variants using functional annotation. BMC Genomics, 14(Suppl 3), S6. https://doi.org/10.1186/1471-2164-14-s3-s6

Calabrese, R., Capriotti, E., Fariselli, P., Martelli, P. L., & Casadio, R. (2009). Functional annotations improve the predictive score of human disease-related mutations in proteins. Human Mutation, 30(8), 1237–1244. https://doi.org/10.1002/humu.21047
