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
![Solution](URL_or_relative_path_to_image)
