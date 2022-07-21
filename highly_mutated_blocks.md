# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md)  



## highly_mutated_blocks
<p>This program finds which blocks produced by mussd.py have significantly more mutations than would be expected if all mutations were uniformly distributed across regions of interest. </p>

### Required Parameters
<ul>

  <li><code>blocks_folder: </code> The folder containing mussd.py output</li>

</ul>

### Optional Paramters:
<ul>
  <li><code>output_file: </code> Output file name. Each line will contain an ID of a significantly "
                                                "mutated block, default is - </li>
<li><code>p_value: </code>P-value cutoff for the binomial test, default=0.05</li>
  <li><code>correctPval: </code> Whether adjust P-values by bonferroni correction, default is True, if use False then this option will be turned off for correction </li>

</ul>

