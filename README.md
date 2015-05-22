### KisSplice description ###

KisSplice is a software that enables to analyse RNA-seq data with or without a reference genome. It is an exact local transcriptome assembler that allows to identify SNPs, indels and alternative splicing events. It can deal with an arbitrary number of biological conditions, and will quantify each variant in each condition. It has been tested on Illumina datasets of up to 1G reads. Its memory consumption is around 5Gb for 100M reads.

KisSplice is not a full-length transcriptome assembler. This means that it will output the variable regions of the transcripts, not reconstruct them entirely.

KisSplice comes as a workflow, with several possible post-treatments meant to facilitate the analysis of the results. The choice of the post-treatment depends on the availability of a reference genome/transcriptome and on the need to perform a differential analysis, as summarised in the following table. 

### Import the dockerfile ###

git clone https://github.com/cmonjeau/docker-kissplice.git

### Build the dockerfile ###

docker build -t cmonjeau/kissplice .

### Print Kissplice programs help ###

docker run -it --rm cmonjeau/kissplice

### Run Kissplice program with data (inside /home/user/Kissplice directory)

docker run -it --rm cmonjeau/kissplice

docker run -it --rm -v /home/user/Kissplice:/data cmonjeau/kissplice -r /data/reads1.fa -r /data/reads2.fa -o /data

