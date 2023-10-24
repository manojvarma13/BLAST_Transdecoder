# Blast and TransDecoder
## Sai Manoj Tekumalla
# Methods
## BLAST & BLAST Programs:
The Basic Local Alignment Search Tool (BLAST) finds regions of local similarity between sequences. The program compares nucleotide or protein sequences to sequence databases and calculates the statistical significance of matches. BLAST can be used to infer functional and evolutionary relationships between sequences as well as help identify members of gene families.[1]

Different types of BLAST programs include, blastp, blastn, blastx whose target sequence types are protein, nucleotide, protein respectively. Their query sequence types include, protein, nucleotide, translated nucleotide respectively. 

## Building a custom BLAST database:
makeblastdb command can be used to create the BLAST database from any .fasta file. 

## Transcriptome annotation:
Transcriptome annotation provides insight into the function and biological process of transcripts and the proteins they encode. Transcriptome analysis involves the measurement of all or a subset of transcripts, including all mRNA in a cell. Two general approaches exist for transcriptome analysis: Mapping sequence reads onto a reference genome and de novo transcriptome assembly using software to infer transcripts from short next generation sequencing reads. Once reads have been mapped, expressed genes and isoforms (transcriptome reconstruction) can be identified. Finally, estimations of genes and isoform abundance as well as differential expression analysis can be performed. Many current RNA-Seq methods are not suitable for annotating 5’ and 3’ ends of transcripts. Using specialized libraries designed to identify transcript ends, annotation can be significantly improved.[2]

## Running BLAST:
BLAST can be run from NCBI or UniProt web pages, from the command-line on a bioinformatics server, via a web API to NCBI, or using a BLAST+ in a Docker image (Links to an external site.) so that you can conveniently use it on the cloud (has been tested on the Google Cloud Platform (GCP) and Amazon Web Services (AWS), however by using open and de facto standards such as Docker and Linux commands, it should be easy to port to other cloud platforms and operating environments). 

The sequence in question is an mRNA (nucleotide) sequence, and to align it to SwissProt, which is a protein database. To align nucleotides to protein sequences, blastx is used.  

## Running TransDecoder:
TransDecoder is a utility developed and included with Trinity (Links to an external site.), and it is intended to assist in the identification of potential coding regions within reconstructed transcripts.

## Find the longest ORFs:
TransDecoder.LogOrfs command will help generate the results. 

## Align Protein (from the ORFs) to SwissProt:
Since many sequences are being used, all the runds will be compared to the swissprot database. 

## Run hmmscan to find protein domains:
hmmscan is a tool, used to search protein sequences against collections of protein profiles. For each sequence in the input file, use that query sequence to search the target database of profiles in hmm_db, and output ranked lists of the profiles with the most significant matches to the sequence.

## Predict proteins:
Transdecoder.LongOrfs command can be used to predict the coding regions from the ORFs.

# Citations
[1] BLAST: Basic Local Alignment Search Tool
https://blast.ncbi.nlm.nih.gov/Blast.cgi

[2] https://genohub.com/bioinformatics/7/transcriptome-annotation#:~:text=Transcriptome%20annotation%20provides%20insight%20into,all%20mRNA%20in%20a%20cell. 
