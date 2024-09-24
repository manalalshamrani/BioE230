# BioE230 Week 3 Assignment

# Q2
## Copy the downloaded files to your home directory on IBEX. 
```bash
scp ncbi_dataset.zip alshammm@ilogin.ibex.kaust.edu.sa:/home/alshammm
```


## Uncompress the zip file on IBEX.
```bash unzip ncbi_dataset.zip
Archive:  ncbi_dataset.zip
replace README.md? [y]es, [n]o, [A]ll, [N]one, [r]ename: y

```

# Q3 
## Write a command to output the line with the largest genome.
```bash 
[alshammm@login509-02-l data_summary]$ tail -n +2 data_summary_new.tsv | sort -t$'\t' -k2 -n | tail -n 1
```

## Write a command to output the line with the smallest genome.
```bash
[alshammm@login509-02-l data_summary]$ tail -n +2 data_summary_new.tsv | sort -t$'\t' -k2 -n | head -n 1
```
![Output](https://github.com/manalalshamrani/BioE230/blob/main/Screen%20Shot%202024-09-24%20at%204.33.23%20PM.png?raw=true)

# Q4
## Find the number of genomes that contain at least two "c" in the species name.

```bash
[alshammm@login509-02-l data_summary]$ tail -n +2 data_summary_new.tsv | cut -f 1 | grep -i "c.*c" | sort | uniq | wc -l
```
### answer: 7
## Find the number of genomes that contain at least two "c" but do not contain the word "coccus."

```bash
[alshammm@login509-02-l data_summary]$ tail -n +2 data_summary_new.tsv | cut -f 1 | grep -i "c.*c" | grep -vi "coccus" | sort | uniq | wc -l
```
### answer: 5
![Output](https://github.com/manalalshamrani/BioE230/blob/main/Screen%20Shot%202024-09-24%20at%205.23.16%20PM.png?raw=true)
# Q5

## Write a command to output how many genome files (FASTA) are larger than 3 megabytes.

```bash
[alshammm@login509-02-l data]$ find . -name "*.fna" -size +3M | wc -l
```

### answer: 6
![Output](https://github.com/manalalshamrani/BioE230/blob/main/Screen%20Shot%202024-09-24%20at%205.22.21%20PM.png?raw=true)
