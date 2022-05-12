# Read Mapping
## Indexing
```
./pbmm2 index /mnt/batty-shared/species/human-9606/reference/hg38/full/ref.fa /home/alserm/Molecules2Variations/pbmm2-develop/ref-pbmm2.mmi```
## Mapping
```
./pbmm2 align /home/alserm/Molecules2Variations/pbmm2-develop/ref-pbmm2.mmi /home/alserm/Molecules2Variations/PBmixSequel729_1_A01_PBTH_30hours_19kbV2PD_70pM_HumanHG003.fastq /home/alserm/Molecules2Variations/pbmm2-develop/PBmixSequel729_pbmm2.bam --preset CCS```

## Variant Calling
```
docker run -v /mnt/panzer/alserm/Molecules2Variations/pbmm2-develop/:/input -v /mnt/batty-shared/species/human-9606/reference/hg38/full/:/refinput -v /mnt/batty/firtinac/Molecules2Variations/deepvariant/pb/output:/output google/deepvariant:1.3.0 /opt/deepvariant/bin/run_deepvariant --model_type=PACBIO --ref=/refinput/ref.fa --reads=/input/PBmixSequel729_pbmm2.bam --output_vcf=/output/output.vcf.gz --output_gvcf=/output/output.g.vcf.gz --intermediate_results_dir /output/intermediate_results_dir --num_shards=32
```
