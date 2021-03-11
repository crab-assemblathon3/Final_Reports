## King Crab genome assembly

### PacBio CLR data, downsampled to 75% ZMWs, assembled with wtdbg2

*Derrik Gratz, Jonas Grove, Chris Chua, Susan Collins, Cameron Watson*

### Downsampling the ZMWs

### Setting Up The Conda Environment

conda create --name redbean  
conda activate redbean  
conda config --add channels bioconda  
conda config --add channels conda-forge  
conda install -c bioconda wtdbg  

### Running wtdbg2 (redbean)
