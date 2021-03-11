## King Crab Genome Assembly

### PacBio CLR data, downsampled to 75% ZMWs, assembled with wtdbg2

*Derrik Gratz, Jonas Grove, Chris Chua, Susan Collins, Cameron Watson*

### Downsampling the ZMWs

Down sampling was performed with the objective of sampling in a stochastic way, such that a particular subset of reads are not sampled with bias. To achieve this, the data files were shuffled before taking the first 75% of reads. The data percentage was calculated using the bit size of the file, such that the downsampled dataset encompassed 75% of the total starting sequence data.

See DownSamplingReport.MD for more info. 

### Setting Up the Conda Environment

conda create --name redbean  
conda activate redbean  
conda config --add channels bioconda  
conda config --add channels conda-forge  
conda install -c bioconda wtdbg  

### Running wtdbg2 (redbean)

**Usage:** wtdbg2 [options] -i <reads.fa> -o <prefix> [reads.fa ...]  
  
**Options Used:**  

| short | type    | description                                                                                |
| ----- | ------- | -------------------------------------------------------------------------------------------|
| -i    | string  | Long reads sequences file (REQUIRED; can be multiple)                                      |
| -o    | string  | Prefix of output files (REQUIRED)                                                          |
| -t    | int     | Number of threads, 0 for all cores                                                         |
| -f    |         | Force to overwrite output files                                                            |
| -x    | string  | Presets, comma delimited; (genome size >= 1G: preset3) -p 19 -AS 2 -s 0.05 -L 5000         |
| -g    | number  | Approximate genome size (k/m/g suffix allowed)                                             |
| -L    | int     | Choose the longest subread and drop reads shorter than <int> (5000 recommended for PacBio) |
| -p    | int     | Kmer psize, 0 <= p <= 23                                                                   |
| -S    | float   | Subsampling kmers, 1/(<-S>) kmers are indexed                                              |
| -A    |         | Keep contained reads during alignment                                                      |
| -s    | float   | Min similarity, calculated by kmer matched length / aligned length                         |
