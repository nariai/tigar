=====
TIGAR
=====

Transcript isoform abundance estimation method with gapped alignment of RNA-Seq data by Variational Bayesian inference

by Naoki Nariai, Osamu Hirose, Kaname Kojima and Masao Nagasaki

<pre>
Example: java -jar Tigar.jar FASTA SAM OUT --thread_num 1 --alpha_zero 0.1
 FASTA            : reference FASTA file
 SAM              : target SAM/BAM file (if the SAM file does not exist, then
                    create the SAM file)
 OUT              : output file
 --alpha_zero N   : tuning parameter alpha_zero
 --bowtiepath VAL : path of bowtie. default = undef
 --inputFastq VAL : input fastq
 --thread_num N   : number of thread
</pre>

This site is maintained by:
Naoki Nariai<br>
<br>
Contact:<br>
nariai [at] megabank.tohoku.ac.jp

