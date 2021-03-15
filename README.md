# Miscellaneous bioinformatics

Navigating common challenges in microbial ecology.

### ./Cutadapt
How to trim primer sequences from reads generated by Illumina. We currently have code for prokaryotic V3-V4, V4, and V4-V5 16S rRNA gene regions; and eukaryotic 18S rRNA gene regions.


### ./DADA2
<b>1. filterAndTrim_bigData.R</b>. At the [filter and trim](https://benjjneb.github.io/dada2/tutorial.html) step, process groups of samples one at a time instead of all samples simultaneously. Saves time and computer power and crashes and headaches.


### catFASTQ.sh
Concatenate FASTQ files with identical names. Its original purpose was to combine files from two sequencing runs (on full and nano Illumina flow cells) on the same samples. 


### demultiplexFASTQ.sh
Trim primers and sort reads according to their unique barcodes. [Mothur](https://mothur.org/wiki/make.contigs/) has this ability, however it also merges paired-end reads in the process. This script's original purpose was to sort reads from mutiple isolate 16S rRNA genes, sequenced simultaneously, based on unique oligos on the 5' ends of primers. This will be updated so it will take a list of file names as input.


### downloadMultipleSRA_series.sh
Download multiple files from NCBI [Sequence Read Archive](https://www.ncbi.nlm.nih.gov/sra). Use when you're interested in runs that are named as a series of numbers, which is typical for BioProjects (e.g., runs in project PRJNA597057 range from SRR10755563 to SRR10755886).


### downloadMultipleSRA_text.sh
Download multiple files from NCBI [Sequence Read Archive](https://www.ncbi.nlm.nih.gov/sra). Use when you're interested in runs that are not named in a series. Create a text file called "runs.txt" at the end of the name. For example...

```
lou$ head runs.txt
ERR2129782
ERR2129783
ERR2129800
ERR2129801
ERR2129803
ERR2129872
ERR2129873
ERR2129875
ERR2129891
ERR2129909
````


### rgiFASTA.sh
Align all FASTAs in a directory with CARD's resistance gene identifier ([RGI](https://card.mcmaster.ca/analyze/rgi)).
