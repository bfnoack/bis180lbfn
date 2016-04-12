Assignment 1
============

## Part 1

In *Introduction to Markdown* you were asked to create a brief
biography of your lab partner. Paste that below.

#Amanda Everitt
**BIotech**
*Junior*
  
* science
* Classic Rock

## Part 2

In *Just Enough Unix for Bioinformatics: Unix Exercise* you were asked
to create a directory structure that mimics the NCBI taxonomy structure
for a bunch of model organisms. Describe in detail (using a Markdown
list) the steps you used to do that task.

* copy the taxnomy list straight from the ncbi site with the following format 'name; name; name'
* in the terminal paste the list with the following command:
> echo 'Eukaryota; Alveolata; Apicomplexa; Aconoidasida; Haemosporida; Plasmodiidae; Plasmodium; Plasmodium'|tr ';' '/'| tr -d '[:space:]'
* again in the command line
>mkdir -p #copyaboveresult#

## Part 3

In *Just Enough Unix for Bioinformatics: Genome Composition Experiment*
you were asked to analyze the mono- and di-nucleotide compositions of 3
genomes. Input the data into the tables below (or an equally clear
format).
#####Commands:
* copy all genomes over
>cp #file# ~/filelocation
>cat *.fas.gz > ~/filelocation/filename
* remove all headers
>zless #oldfile#  |grep -v '>' > #newfile#

*  count all mono/di-nt
>grep '#onechar#' -o #filename# |wc -l
>grep 'ACTG' -o #filename# |wc -l
>echo (above results)/(total count) |bc -l

**Table 1:** Mono-nucleotide frequencies

| NT |  At  |  Ce  |  Dm  |
|:--:|:-----|:-----|:-----|
| A  |   0.32   |   0.323   |   0.29   |
| C  |   0.18   |   0.117   |   0.208   |
| G  |   0.18   |   0.117   |   0.208   |
| T  |   0.32   |   0.323   |   0.29   |

**Table 2:** Expected and observed di-nucleotide frequences

| NTs| At obs | At exp | Ce obs | Ce exp | Dm obs | De exp |
|:--:|:-------|:-------|:-------|:-------|:-------|:-------|
| AC |0. 0516|.0576        |        |        |        |        |
| AG | 0.0587       |    .0576    |        |        |        |        |
| AT | 0.0912       |     0.102   |        |        |        |        |
| CA | 0.0627    |    0.0576                |        |        |        |        |
| CC | 0.0289    |     0.0324        |        |        |        |        |
| CG |  0.0232     |     0.0324       |        |        |        |        |        |
| CT |        0.0587     |    0.0576         |        |        |        |        |
| GA |         0.0633    |    0.0576      |        |        |        |        |
| GC |        0.0296    |    0.0324       |        |        |        |        |
| GG |       0.0287    |    0.0324       |        |        |        |        |
| GT |        0.0516    |    0.0576       |        |        |        |        |
| TA |       0.0756    |    0.1024      |        |        |        |        |
| TC |       0.0632    |   0.0576       |        |        |        |        |
| TG |        0.0626     |    0.0576       |        |        |        |        |
| TT |        0.083     |    0.1024      |        |        |        |        |

Briefly discuss the results of your experiment below.
* The results of the di-duc cannot be be predicted from the mono results because the amino acids are not independently distributed from another

*The reulst supported the predictions. Where the Expected and Observed are very varied could be an indication of repeats.
