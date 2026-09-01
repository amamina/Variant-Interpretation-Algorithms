**PANTHER (protein analysis through evolutionary relationships) ** employs a **PSEP (Position Specific Evolutionary Preservation) method to predict non-synonymous SNPs that affect protein function. This method searches for evolutionary preservation of amino acid positions within a protein family rather than simple conservation for identifying harmful mutations. Preservation involves reconstructing ancestral sequence to trace evolutionary changes. This tracing stops under two conditions: when a different amino acid appears in the ancestral sequence, or when the default probability of reconstruction falls below a preset threshold. Its method has been tested in experiments using the human ** MTHFR** protein and in **E.coli lacI **protein where it performed better than traditional conservation based methods.

Once the tracing stops, the age of last ancestor with a preserved amino acid is calculated in millions of years. If the conservation time is greater than 450my, the substitution is considered probably damaging; if it is between 450 and 200my, it is considered possibly damaging. Variants below 200my are regarded as neutral (Tang & Thomas, 2016; Thomas et al., 2022).

References:

Thomas, P. D., Ebert, D., Muruganujan, A., Mushayahama, T., Albou, L., & Mi, H. (2021). PANTHER : Making genome‐scale phylogenetics accessible to all. Protein Science, 31(1), 8–22. https://doi.org/10.1002/pro.4218

Tang, H., & Thomas, P. D. (2016). PANTHER-PSEP: predicting disease-causing genetic variants using position-specific evolutionary preservation. Bioinformatics, 32(14), 2230–2232. https://doi.org/10.1093/bioinformatics/btw222
