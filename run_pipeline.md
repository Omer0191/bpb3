# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [Clean temp](clean_tmp.md) 



## Run_pipeline

<p> Run BayeaPI-BAR3 full pipeline with a proper bpb3 configure file. If clustered PWMs are used in the calcuation then it is the first level analysis of bpb3. The second level analysis of bpb3, which evaluates the top N PWMs from the ranking test of the first analysis, can be achieved by function bpb3selectedPWM. </p>

### Required Parameters:

<ul>
  <li><code>import_bpb3_config: </code>File for import bpb3 configure file , and the name shall be bpb3_config.py.</li>
</ul>
Download the config file [here](https://github.com/Omer0191/bpb3-Documentation/blob/main/bpb3_clusterPWM_config_fl.py.gz)  
