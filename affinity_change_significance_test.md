# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [make_cluster4pwm](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md)  | [Run Pipeline](run_pipeline.md) | [clean_tmp](clean_tmp.md)  



## Affinity_change_significance_test

Significant test of TF binding affinity changes between the foreground and the background calculations

## Required Paramters
<ul>
  <li><code>background_folder: </code> Folder containing the computed background model "
                                                                "produced by background_affinity_changes.py",</li>
<li><code>foreground_folder: </code> Folder containing the computed delta-dba values for "
                                                                "patient data produced by bayespi_bar.py"</li>
 
  
</ul>

## Optional Parameters

<ul>
  <li><code>output_file: </code> Output file name, default is - </li>
<li><code>p_value: </code> P-value cutoff for the Wilcoxon test, default=0.05</li>
  <li><code>max_rank: </code> Maximum rank of PWM to consider in the patient results, default=15 </li>
<li><code>exact_test: </code> Use exact Wilcoxon rank-sum test from R. R needs to be installed, default is False"</li>
  <li><code>pval_correction: </code> Whether adjust P-values by bonferroni correction, default is False"</li>
<li><code>: </code></li>
  
</ul>
