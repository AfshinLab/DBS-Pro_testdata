# DBS-Pro testdata version 0.4 generation

Copied `ABC-sequences.fasta` from DBS-Pro-testdata-0.3.

Subsampled original PrEST FASTA files from /proj/uppstore2018173/private/rawdata/190407.MiSeq.DBSpro.new_read_structure/ 
on rackham to 20,000 reads each. Used three different dataset to have the ability to test and compare 
running multiple samples. 

```
seqtk sample -s 1000 /proj/uppstore2018173/private/rawdata/190407.MiSeq.DBSpro.new_read_structure/1_PrEST01_L001/1-PrEST01_S10_L001_R1_001.fastq 20000 | pigz > sample1.fastq.gz
seqtk sample -s 1000 /proj/uppstore2018173/private/rawdata/190407.MiSeq.DBSpro.new_read_structure/2_PrEST02_L001/2-PrEST02_S11_L001_R1_001.fastq 20000 | pigz > sample2.fastq.gz
seqtk sample -s 1000 /proj/uppstore2018173/private/rawdata/190407.MiSeq.DBSpro.new_read_structure/3_PrEST03_L001/3-PrEST_S12_L001_R1_001.fastq 20000 | pigz > sample3.fastq.gz
```

Additional info about the samples:

- sample1: Generated using beads coated in ABC1 antigen
- sample2: Generated using beads coated in ABC2 antigen
- sample3: Generated using beads coated in ABC3 antigen

//Pontus, 2021-07-07

