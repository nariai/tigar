=====
TIGAR
=====

Transcript isoform abundance estimation method with gapped alignment of RNA-Seq data by variational Bayesian inference

by Naoki Nariai, Osamu Hirose, Kaname Kojima and Masao Nagasaki

<pre>
 Example: java -jar Tigar.jar FASTA SAM OUT --alpha_zero DOUBLE --is_paired INT --polyA INT
 FASTA          : reference FASTA file
 SAM            : target SAM/BAM file
 OUT            : output file
 --alpha_zero N : tuning parameter alpha_zero
 --is_paired N  : paired-end data. default = 0 (false). Please set 1, if sam
                  file was generated from paired-end reads.
 --polyA N      : polyA flag. default = 0 (false). Please set 1 if both read
                  and reference sequences contain polyA tails.
</pre>

## Recommended pipeline to run TIGAR

Prepare cDNA reference sequences in FASTA format.

<pre>
e.g.)
http://hgdownload.soe.ucsc.edu/goldenPath/hg19/bigZips/refMrna.fa.gz
</pre>

Build bowtie2 index

<pre>
bowtie2-build refMrna.fa ./ref/refMrna
</pre>

Run bowtie2

<pre>
bowtie2 -p 8 -k 1000 --very-sensitive ./ref/refMrna sample.fa > sample.sam
</pre>

Run TIGAR

<pre>
java -jar Tigar.jar refMrna.fa sample.sam --alpha_zero 0.1 ./out/sample_out.txt
</pre>

Please note that the current implementation of TIGAR requires large memory size for large sam/bam files.
We will keep posted the latest version of the software for improving memory usage and
running speed.




This site is maintained by:
Naoki Nariai<br>
<br>
Contact:<br>
nariai [at] megabank.tohoku.ac.jp

Last updated on 2013/05/10

