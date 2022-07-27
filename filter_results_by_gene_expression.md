# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Secondary Functions

## filter_results_by_gene_expression

### Requried Parameters:
<ul>
  <li><code>results_file: </code>the file containing
                        affinity_change_significance_test.py output </li>
<li><code>expression: </code>the file containing gene expression values. Two
                        columns: gene name and gene expression</li>

    
</ul>

### Optional Parameters:

<ul>
  <li><code>output_file: </code>output file name. It has the same format as input with
                        lowly expressed TFs removed </li>
<li><code>min_expression: </code> minimum TF gene expression value, default minimum RPKM
                        = 0.03</li>
  
    
</ul>  
[Home](index.md)
