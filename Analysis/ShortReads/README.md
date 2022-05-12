# Read Mapping
## Indexing
```
./bwa-mem2 index -p prefix /mnt/batty-shared/species/human-9606/reference/hg38/full/ref.fa
```
## Mapping
```
./bwa-mem2 mem -t 1 prefix /mnt/batty-shared/species/human-9606/sample/na12878-SAMEA1573618/illumina/ERR194147-262997_1.fastq /mnt/batty-shared/species/human-9606/sample/na12878-SAMEA1573618/illumina/ERR194147-262997_2.fastq -o ERR194147-262997-40.sam
```
