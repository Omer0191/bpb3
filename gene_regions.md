# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [make_cluster4pwm](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md)  | [Run Pipeline](run_pipeline.md) | [clean_tmp](clean_tmp.md)  



## gene_regions
<p>This program extracts regions near transcription start site of selected genes based on gencode gtf file. </p>

### Required Parameters:
<ul>
  <li><code>gene_annotation: </code> Gene annotation in GTF format from genCode(e.g. https://www.gencodegenes.org/releases/19.html)</li>
 </ul>

### Optional Paramters:


<ul>
  <li><code>selected_genes: </code> File with gene names to use. The first column will be taken as the list of gene names. If not given, all genes from the annotation file will be used, default is None</li>
  <li><code>upstream_size: </code> Number of base pairs to take upstream of the TSS, default=1000</li>
<li><code>downstream_size: </code> Number of base pairs to take downstream of the TSS, default=1000</li>
  <li><code>transform_chrom: </code> Transform chromosome names between long (chr15) and short(15) formats, default is False</li>
<li><code>output_file: </code> Output file name in BED format, default is - . </li>
  
 </ul>
 
 
