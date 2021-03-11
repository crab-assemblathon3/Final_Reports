# Downsampling PacBio King Crab Sequence Data

## Method

Down sampling was performed with the objective of sampling in a stochastic way, such that a particular subset of reads are not sampled with bias. To achieve this, the data files were shuffled before taking the first 75% of reads. The data percentage was calculated using the bit size of the file, such that the downsampled dataset encompassed 75% of the total starting sequence data.

## Results

| Sample File Name                    | Initial Size | Downsampled Size | Percentage Retained |
|-------------------------------------|--------------|------------------|---------------------|
| m64047_190827_175934.subreads.fastq | 143G         | 109G             | 0.7622377622377622  |
| m64047_201204_214048.subreads.fastq | 273G         | 212G             | 0.7765567765567766  |
| m64047_201206_040637.subreads.fastq | 298G         | 228G             | 0.7651006711409396  |
| m64047_201207_104522.subreads.fastq | 203G         | 154G             | 0.7586206896551724  |
| m64047_201208_172424.subreads.fastq | 257G         | 196G             | 0.7626459143968871  |