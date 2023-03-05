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

The overall quality of raw reads from RNA-Seq libraries was assesed with FastQC. Raw reads were filtered and quality trimmed using trimmomatic v0.33 with the following parameters: "ILLUMINACLIP:TruSeq2-PE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:35". Gene quantification reported as transcripts per million (TPM) was calculated using 'quant' fuction inside kallisto v0.46 and the version 5 of the reference line B73 downloaded from the maizeGDB webpage. Sumarized table with all TPM values was created with in-house python script 'Make_rna_ss.py' deposited here.

