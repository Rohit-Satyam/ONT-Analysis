# ONT-Analysis
Resources related to ONT analysis
1. [Introduction to Long-Read Data Analysis](https://timkahlke.github.io/LongRead_tutorials/)


## Steps
1. ONT doesn't produce Paired end data like illumina. It produces multiple fastq files per sample (barcode) that needs to be concatenated before downstream analysis using the command:

```bash
ls -1 -d * | while read p; do zcat $p/*.gz | gzip > $p.fastq.gz; done
```
