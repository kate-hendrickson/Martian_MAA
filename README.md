# Martian_MAA
A repository for code, inputs, one one major output for performing Mineral Association Analysis on samples from Mars. See Morrison et al. (2023) PNAS Nexus for original model development, Prabhu et al. (2022) for an rds file of the model, and Hendrickson et al. (2026) in review for details of this application and interpretation of outputs.

# Files
- Martian_MAA.R
- Martian_MAA_Leave_One_Mineral_Out.R
- data/All_Predictions_Output_Sheet.xlsx
- data/mars_data/mars_export.csv


"Martian_MAA.R" Applies the ruleset available at https://doi.org/10.48484/1k4t-f534 (Prabhu et al., 2022; model is titled “Allmin_USA_localities_subset_cleaned.rds”) to a set of minerals in Gale Crater studied by the Curiosity rover with the CheMin instrument. The apriori ruleset model used is not original to this work and is too large to be on a GitHub, so it is not directly included but necessary for the code. This file will be need to be placed in "data/association_data" for the code to run as is. See References.

"Martian_MAA_Leave_One_Mineral_Out.R" removes one input mineral at a time to see how well the model currently validates internal phases. These validations can be used to support the existence of phases, document model bias (i.e., towards hydrated phases), and understand in what ways CheMin samples on Mars deviate from trends expected on Earth (minerals that are not internally validated are not consistently in assemblages with the same minerals in our reference dataset.)

"All_Predictions_Output_Sheet.xlsx" is a file of all matching association rules from “Allmin_USA_localities_subset_cleaned.rds” that can be used as predictions, saved as printed lines while the code was executing. For machine-readable summaries and interpretations of these outputs, see Hendrickson et al. (2026) in review.

"mars_export.csv" is the IMA-processed input dataset from CheMin as indicated in Table 2 of Hendrickson et al. (2026) in review.

# References
Hendrickson, K., Yee, F., Prabhu, A., Sheppard, R., Hazen, R. M., Rampe, E. B., Bermanec, M., Jibrin, Z., Bristow, T. F., Yen, A. S., Thorpe, M. T., Tu, V. M., Downs, R. T., Blake, D. F., Tutolo, B. M., Vaniman, D. T., Des Marais, D., Morris, R. V., Ming, D. W., Meusburger, J. M., Simpson, S. L., Hausrath, E. M., Chipera, S. J., Craig, P. I., Castle, N., & Morrison, S. M. (2026). Expanded Mineralogy in Gale Crater: Predictions from Martian Mineral Association Analysis [Manuscript under review as of 10/2026]

Morrison, S. M., Prabhu, A., Eleish, A., Hazen, R. M., Golden, J. J., Downs, R. T., et al. (2023). Predicting new mineral occurrences and planetary analog environments via mineral association analysis. PNAS Nexus, 2(5), pgad110. https://doi.org/10.1093/pnasnexus/pgad110 

Prabhu, A., Morrison, S. M., Eleish, A., Fox, P., Golden, J. J., Downs, R. T., Perry, S., Burns, P. C., Ralph, J., & Hazen, R. M. (2022). Mineral association analysis—Rule bases to predict unknown mineral occurrences. Open Data Repository. https://doi.org/10.48484/1k4t-f534
