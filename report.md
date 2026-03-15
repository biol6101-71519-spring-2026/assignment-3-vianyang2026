# Homework 3 Rna seq analysis Report 

## Quality Control & Trimming

Raw sequencing data quality was assessed using FastQC, and the results showed high-quality reads across all samples with quality scores above Q30, indicating very reliable data. Trim Galore was then used to remove adapter sequences and poor quality sections from the reads. The trimmed reads were then quality checked to verify that the trimming process had successfully improved read quality.  A notable observation was that the AGA samples (control group) were much larger files (5-8GB each) compared to the LWR samples (4-5GB each), indicating different amounts of sequencing data between the two groups. After trimming, MultiQC confirmed that all samples maintained good quality.

## Alignment

Alignment of cleaned reads to the reference genome yielded excellent results, with every sample achieving 100% alignment rate. The difference in data volume became even more apparent during alignment: AGA control samples contained substantially more reads (105-122 million mapped reads each), while LWR treatment samples had considerably fewer (206,000 to 2.4 million reads each). The difference in sequencing depth between the two groups was significant.

## Exploratory Analysis

The PCA analysis reveals clear separation between the two experimental groups. PC1 explains 95.2% of the variance and effectively separates the AGA control samples (AGA01, AGA02, AGA03) on the right side from the LWR treatment samples (LWR05, LWR06, LWR07) on the left side. PC2 accounts for only 3.2% of the variance, indicating that the primary source of variation in the dataset is the difference between conditions rather than technical factors or batch effects.

The correlation heatmap reinforces these findings, showing strong within group correlations and clear between group differences. AGA control samples show high correlations with each other (0.871-0.898), while LWR treatment samples also correlate well within their group (0.540-0.787). In contrast, correlations between AGA and LWR samples are much lower (0.260-0.451), confirming the distinct gene expression profiles between the two conditions.
