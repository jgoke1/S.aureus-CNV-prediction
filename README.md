# S.aureus-CNV-prediction
Identifying borderline oxacillin-resistant Staphylococcus aureus via CNV prediction using Contol-FREEC

### INTRODUCTION
Staphylococcus aureus is a major global pathogen, with methicillin resistance posing significant challenges. Borderline oxacillin-resistant S. aureus (BORSA) are mecA-negative, yet methicillin-resistant and often misclassified as methicillin susceptible S. aureus (MSSA). Suggestions that the BORSA phenotype may arise from elevated expression levels of blaZ gene, as reported by many studies.

This study aims to develop and validate whole-genome sequence-based methods to identify BORSA, using copy number variation of the blaZ gene.

We used the Control-freec4 algorithm for the detection of copy number in 145 known methicilin resistant lacking mec (MRLM) and 166 known MSSA, all with known mic values from studies1,2,3. As well in comparison to mutations of the MRLM in the gdpP and PBPs genes.

### METHOD
Quality check was used to sort the aligned files and to generate the depth of sequence. 

Control-freec was then configured to generate copy numbers for S. aureus, with varying bin, seq was done using fastqc and trimmomatics on short reads sequence, mapping of the genome to a reference genome was done using Bowtie, Samtools uence data with higher mapping depth, we used 250 bin while those with lower mapping depth we used 1000 bin, in other conceal some sequencing noise that may cause discrepancies in output.

 Phylogenetic tree was reconstructed using Iqtree after variant was called with Snippy and tree visualisation was done ITOL. Statistical analysis and visualisation was done using  R.

### RESULT
Of the 311 MRLM/MSSA tested, 47 MRLM were true positives (had a copy number higher than the baseline of 1), 98 MRLM were false negatives (had a copy number less than the baseline), 97 MSSA were true negatives (had a copy number lower or equal to the baseline), and 69 MSSA were false positives (had a copy number higher than the baseline).

ST7 phenotype was observed to have a high copy number, and the same was true for ST188, which is majorly MRLM. These STs are reportedly less susceptible to oxacillin due to the overexpression of the blaZ gene and mutations in gdpP and PBPs genes.  Among ST7, elevated copy number was not associated with MLRM but gdpP SNPS showed strong association (p=0).

Of the 145 MRLM, 20 known to harbour truncated gdpP genes had copy numbers of less than 6, except for the 3 MRLM of ST7 with higher copy numbers.


