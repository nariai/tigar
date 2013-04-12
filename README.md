=====
TIGAR
=====

Transcript isoform abundance estimation method with gapped alignment of RNA-Seq data by Variational Bayesian inference

by Naoki Nariai, Osamu Hirose, Kaname Kojima and Masao Nagasaki

<pre>
 Example: java -jar Tigar.jar <FASTA> <SAM> <OUT> --alpha_zero <DOUBLE> --is_paired <INT> --polyA <INT>
 FASTA          : reference FASTA file
 SAM            : target SAM/BAM file
 OUT            : output file
 --alpha_zero N : tuning parameter alpha_zero
 --is_paired N  : paired-end data. default = 0 (false). Please set 1, if sam
                  file was generated from paired-end reads.
 --polyA N      : polyA flag. default = 0 (false). Please set 1 if both read
                  and reference sequences contain polyA tails.
</pre>

This site is maintained by:
Naoki Nariai<br>
<br>
Contact:<br>
nariai [at] megabank.tohoku.ac.jp

