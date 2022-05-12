# Read Mapping
## Indexing
```
./minimap2 -t 1 -x map-ont -d /home/alserm/Molecules2Variations/minimap2-master/hg38-ont.mmi /mnt/batty-shared/species/human-9606/reference/hg38/full/ref.fa
```
## Mapping
```
./minimap2 -t 1 -a hg38-ont.mmi /home/alserm/Molecules2Variations/GM24149_1.fastq
```

## Variant Calling
```
docker run -v /mnt/panzer/alserm/Molecules2Variations/minimap2-master/:/input -v /mnt/batty-shared/species/human-9606/reference/hg38/full/:/refinput -v /mnt/batty/firtinac/Molecules2Variations/deepvariant/ont/output:/output kishwars/pepper_deepvariant:r0.8 run_pepper_margin_deepvariant call_variant -f /refinput/ref.fa -b /input/ONT-GM24149_1.bam -o /output/ -t 32 --ont_r9_guppy5_sup
```
