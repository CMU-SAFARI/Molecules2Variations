# Read Mapping
## Indexing
```
./bwa-mem2 index -p prefix /mnt/batty-shared/species/human-9606/reference/hg38/full/ref.fa
```
## Mapping
```
./bwa-mem2 mem -t 1 prefix /mnt/batty-shared/species/human-9606/sample/na12878-SAMEA1573618/illumina/ERR194147-262997_1.fastq /mnt/batty-shared/species/human-9606/sample/na12878-SAMEA1573618/illumina/ERR194147-262997_2.fastq -o ERR194147-262997-40.sam
```

# Variant Calling
```
docker run -v /mnt/panzer/alserm/Molecules2Variations/:/input -v /mnt/batty-shared/species/human-9606/reference/hg38/full/:/refinput -v /mnt/batty-shared/species/human-9606/sample/na12878-SAMEA1573618/illumina/bwa/:/baminput -v /mnt/batty/firtinac/Molecules2Variations/deepvariant/illumina/output:/output google/deepvariant:1.3.0 /opt/deepvariant/bin/run_deepvariant --model_type=WGS --ref=/refinput/ref.fa --reads=/baminput/hg38_na12878_ERR194147-262997.bam --output_vcf=/output/output.vcf.gz --output_gvcf=/output/output.g.vcf.gz --intermediate_results_dir /output/intermediate_results_dir --num_shards=32
```
