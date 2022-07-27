# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Secondary Functions

## filter_results_by_gene_expression
<p>This program will filter those TFs whose expression is too low (e.g., RPKM<0.03) from the results produced by affinity_change_significance_test.py.
Warning: it assumes a certain naming convention for PWM files. If you add your own PWM files that do not conform to it it will likely crash or filter them out. It is also incomplete and doesn't recognize many TFs. This is the reason it is not a part of the package, but rather a demo </p>
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
