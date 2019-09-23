### Set file paths of inputs
```
seq_f=
seq_r=
index_file=TruSeq3-PE-2_G.fa
output_base=
```

### Run Trimmomatic to just trim Illumina adapters and polyG stretches at the ends.
```
trimmomatic PE \
-phred33 \
"$seq_f" "$seq_r" \
"$output_base"_paired_f.fastq \
"$output_base"_single_f.fastq \
"$output_base"_paired_r.fastq \
"$output_base"_single_r.fastq \
ILLUMINACLIP:"$index_file":2:30:7
```
