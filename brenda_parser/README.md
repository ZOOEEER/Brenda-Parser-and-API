One could download the *brenda_download.txt* from https://www.brenda-enzymes.org/download_brenda_without_registration.php

The correspondence between abbreviations using in *brenda_download.txt* and entry names is saved in *NAME.txt*.

## Dealing with entries
The entries could be grouped into 5 classes.
\# | Entry | Example | Description*
-|-|-|-
1|REFERENCE|<2> O'Connor, K.C.; Bailey, J.E.: Hydrolysis of emulsified tributyrin by porcine pancreatic lipase. Enzyme Microb. Technol. (1988) 10, 352-356. {Pubmed:} (c)| \<r\> c {a}
2|PROTEIN|#1# Meleagris gallopavo   (#1# isoform Xyl3A <315>) <315>| #p# c (a) \<r\>
3|SUBSTRATE_PRODUCT|#121# (R/S)-ibuprofen methoxyethyl ester + H2O = (R)-ibuprofen methoxyethyl ester + (S)-ibuprofen + 2-methoxyethanol {} <97>| #p# c (a) {a} \<r\>
4|CLONED|#200# (expression in Trichoderma reesei) <351>|#p# (a) \<r\>
5|SYSTEMATIC_NAME|triacylglycerol lipase| c

*p = protein, r = reference, c = content, a = annotation

Regular expressions are built for each class to extract information.
\# | Entries
-|-
1|'REFERENCE'
2|'PROTEIN'
3|'SYNONYMS',  'SOURCE_TISSUE',  'LOCALIZATION', 'NATURAL_SUBSTRATE_PRODUCT', 'SUBSTRATE_PRODUCT',                     'TURNOVER_NUMBER', 'KM_VALUE', 'PH_OPTIMUM', 'PH_RANGE', 'SPECIFIC_ACTIVITY',                      'TEMPERATURE_OPTIMUM', 'TEMPERATURE_RANGE', 'COFACTOR', 'ACTIVATING_COMPOUND', 'INHIBITORS', 'METALS_IONS',                     'MOLECULAR_WEIGHT', 'POSTTRANSLATIONAL_MODIFICATION', 'SUBUNITS', 'PI_VALUE',                     'APPLICATION', 'ENGINEERING', 'GENERAL_STABILITY', 'ORGANIC_SOLVENT_STABILITY',                     'OXIDATION_STABILITY', 'PH_STABILITY', 'STORAGE_STABILITY', 'TEMPERATURE_STABILITY', 'KI_VALUE',                     'IC50_VALUE', 'KCAT_KM_VALUE', 'EXPRESSION', 'GENERAL_INFORMATION'
4|'CLONED', 'CRYSTALLIZATION', 'PURIFICATION', 'RENATURED'
5|'RECOMMENDED_NAME', 'REACTION', 'SYSTEMATIC_NAME', 'REACTION_TYPE'
