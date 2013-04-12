=====
TIGAR
=====

Transcript isoform abundance estimation method with gapped alignment of RNA-Seq data by Variational Bayesian inference

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

## 1. Prepare cDNA reference sequences in FASTA format.
refMrna.fasta

## 2. Build bowtie2 index (otherwise, please use below already constructed)
bowtie2-build refMrna.fasta ./ref/refMrna

## 3. Run bowtie2
bowtie2 -p 8 -k 1000 --very-sensitive ./ref/refMrna sample.fastq > sample.sam

## 4. Run TIGAR
java -jar Tigar.jar  refMrna.fasta  sample.sam --alpha_zero 0.1 ./out/sample_out.txt







This site is maintained by:
Naoki Nariai<br>
<br>
Contact:<br>
nariai [at] megabank.tohoku.ac.jp

