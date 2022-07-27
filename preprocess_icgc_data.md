# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Secondary Functions

## preprocess_icgc_data

This is a demo script for getting and preprocessing of ICGC data before running bpb3

### Required Parameters:



<ul>
  <li><code>out_data_folder : </code>Export data file folder </li>
<li><code>patient_data_folder : </code>patient data folder </li>
  <li><code> normal_rnaseq_folder: </code>normal sample RNA-seq data folder, where the file
                        namee shall be *.gene_counts.tsv if they will be
                        selected for analysis </li>
<li><code>source_data_folder : </code>source data folder for downloaed files from ICGC data
                        portal. </li>
  <li><code>genome_folder : </code> Genome folder that contains genome information such as
                        fasta fikle and gene annotation files et al</li>
     <li><code>genome_fasta_file : </code>Genome fasta file </li>
<li><code>gene_annotation_file : </code>Gene annotation file from genCode with gtf format </li>
  <li><code>rnaseq_file : </code> RNA-seq file name for tumor samples</li>
</ul>

### Optional Parammeters:
<ul>
  <li><code> genome_link: </code>Genome sequence link address, default is ftp://ftp.100
                        0genomes.ebi.ac.uk/vol1/ftp/technical/reference/phase2
                        _reference_assembly_sequence/hs37d5.fa.gz </li>
<li><code> annotation_link: </code>Gene annotation link address, default is ftp://ftp.ebi
                        .ac.uk/pub/databases/gencode/Gencode_human/release_19/
                        gencode.v19.annotation.gtf.gz </li>
  <li><code> skin_cancer_data_link: </code>Skin cancer data link address, default is
                        https://junbaiw.github.io/BayesPI-BAR2/"
                        "skin_cancer_icgc_and_normal_melanocytes_geo_data.tgz </li>

</ul>  

[Home](index.md)
