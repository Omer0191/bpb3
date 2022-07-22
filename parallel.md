# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [make_cluster4pwm](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md)  | [clean_tmp](clean_tmp.md)  


## parallel

<p>This program runs commands from the given file in parallel.</p>

### Required Paramters:
<ul>
  
  <li><code>commands_file: </code>file name with commands to run, one command per line </li>

</ul>

### Optional Paramters:
<ul>
  
<li><code>tmp_folder: </code>folder to put the temporary files (will be erased)</li>
  <li><code>name: </code> name tag for jobs</li>
 
</ul>

### Parallelization Paramters:
<ul>
  <li><code>use_cores: </code>number of cores to use on one machine </li>
<li><code>use_slurm: </code>use SLURM workload manager to distribute computations across nodes</li>
  <li><code>slurm_account: </code> SLURM account name</li>
<li><code>max_nodes: </code>maximum number of nodes to allocate when using SLURM</li>

</ul>
