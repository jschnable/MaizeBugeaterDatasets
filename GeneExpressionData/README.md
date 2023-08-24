# Sample Collection

## Nebraska 2020

Samples were collected from the "1000s" replicate of the 2020 Nebraska Bugeater field experiment between 9 AM and 11 AM on July 8th, 2020. In each plot, a single representative plant was selected and five leaf discs were sampled from a fully expanded/mature leaf.

## Nebraska 2021

Samples were collected from the "XXXXs" replicate of the 2021 Nebraska Bugeater field experiment between 9 AM and 11 AM on July 8th, 2021. In each plot, a single representative plant was selected and five leaf discs were sampled from a fully expanded/mature leaf.

## Michigan 2021

...get details from Addie. 

# Sample Preparation

## Nebraska 2020

RNA extraction was performed on 50mg leaf tissue stored in 2mL microcentrifuge tubes (Fisher Scientific; 05-408-138) containing a single, 3/16" stainless steel precision ball (Grainger; 4RJF7). Samples had remained frozen at or below -60*C since collection.

Using a TissueLyzer II (Qiagen; 85300) that oscillated at 25Hz in 30 second increments, the frozen leaf samples were ground to a fine powder. If additional grindings were required, samples were chilled on dry ice for one minute before resuming.

Total RNA was extracted from the grounded frozen leaf samples using the MagMax Plant RNA Isolation Kit (ThermoFisher Scientific; A47157). The standard procedure affiliated with this product was followed. It should be noted the extraction was performed with the optional use of dithiothreitol in the lysis buffer and the aid of a Kingfisher Flex Purification System (ThermoFisher Scientific; 5400630).

Total RNA extracts had their concentration quantified using the Quant-IT Broad Range RNA Assay Kit (ThermoFisher Scientific; Q10213) and a CLARIOstar Plus plate reader (BMG LabTech)

## Nebraska 2021 and Michigan 2021

Samples were extracted largely as described for Nebraska 2020, but extractions were conducted externally (at Psomagen). RNA concentration with a TapeStation 4200 (Agilent) rather than with dye and plate reader. 

# Sequencing

For each RNA sample a single stranded mRNA TruSeq library was constructed. Samples were sequenced on a NovaSeq6000 S4 with 2x150 base pair reads, and a target average of 40M reads per sample. Sequencing was conducted by Psomagen.

# Raw Sequence Data

Each RNA sample has been or will be deposited into the NCBI SRA. Details to be added when this occurs.

# Expression Quantification

(Genome version. Software. Settings. This work was conducted by Vladimir Torres Rodriguez.)

The overall quality of raw reads from RNA-Seq libraries was assessed with FastQC. Raw reads were filtered and quality trimmed using Trimmomatic v0.33 (Bolger et al., 2014) with the following parameters: "ILLUMINACLIP:TruSeq3-PE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:35". Gene quantification reported as transcripts per million (TPM) was calculated using the 'quant' function inside Kallisto v0.46 (Bray et al., 2016) and the version 5 of the reference line B73 downloaded from the maizeGDB webpage. Summarized table with all TPM values was created with in-house python script. 

# Transcriptome-wide association studies 
Genes with TPM > 0.1 in at least 50% of the samples were kept for down-stream analysis. Methodology to prepare data for the association analysis was as described in Li D. et al (Li D. et al., 2021), briefly, TPM data was normalized in a range from 0 to 2. Extreme values were converted to 0 (TPM values smaller than quantile 5) or 2 (TPM values larger than quantile 95), the remaining values were linearly transformed into values between 0 and 2.

TWAS was performed using the R package GAPIT under the Compressed Mixed Linear Model (Zhang et al., 2010; Lipka et al., 2012). The first three principal components derived from gene expression were included. Genes described as associated were those with a p-value lower than the threshold calculated as Bonferroni correction of 0.05 

# Bibliography 
(Expression Quantification & Transcriptome-wide association studies)

Zhang, Zhiwu, Elhan Ersoz, Chao-Qiang Lai, Rory J. Todhunter, Hemant K. Tiwari, Michael A. Gore, Peter J. Bradbury et al. "Mixed linear model approach adapted for genome-wide association studies." Nature genetics 42, no. 4 (2010): 355-360.

Lipka, Alexander E., Feng Tian, Qishan Wang, Jason Peiffer, Meng Li, Peter J. Bradbury, Michael A. Gore, Edward S. Buckler, and Zhiwu Zhang. "GAPIT: genome association and prediction integrated tool." Bioinformatics 28, no. 18 (2012): 2397-2399.

Bolger, Anthony M., Marc Lohse, and Bjoern Usadel. "Trimmomatic: a flexible trimmer for Illumina sequence data." Bioinformatics 30, no. 15 (2014): 2114-2120.

Bray, Nicolas L., Harold Pimentel, Páll Melsted, and Lior Pachter. "Near-optimal probabilistic RNA-seq quantification." Nature biotechnology 34, no. 5 (2016): 525-527.

Li, Delin, Qiang Liu, and Patrick S. Schnable. "TWAS results are complementary to and less affected by linkage disequilibrium than GWAS." Plant physiology 186, no. 4 (2021): 1800-1811.


