# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md)  | [Run Pipeline](run_pipeline.md) 

## bayespi_bar
<p>BayesPI-BAR delta-dbA ranking computation for TFs binding affinity changes affected by DNA mutations. This program computes rankings of given PWMs/clustered PWMs according to predicted effects of given sequence variants. This module needs following paramters. Details are given as under: </p>

<ul>
  <li><code>chemical_potentials: (str) </code>list of chemical potentials to use (e.g.,none -10 -13 -15 .. ), default is None </li>
  <li><code>reference_sequences: </code>FASTA file with reference sequences, default is None.</li>
  <li><code>alternate_sequences: </code>FASTA file with alternate sequences, default is None.</li>
  <li><code>pwm_folder: </code>Folder containing TF binding models in BayesPI .mlp format, default is None.</li>
  <li><code>iterations: (int) </code>Iteration count for background affinity distribution calculation, default =10000 </li>
  <li><code>p_value_cutoff: (float) </code>maximum dbA p-value to consider protein-DNA binding, default = 0.1.</li>
  <li><code>normalize_dba: </code>divide each dbA value by its standard deviation in the background sequence set, default is False,</li>
  <li><code>start_from_integration: </code>Do not compute delta-dbA values, assume they are already computed. Start from integration. default is False.</li>
  <li><code>reuse_output: </code>Do not recompute dbA values if they are already present in the result folder. This mode can handle partially computed results from an interrupted computation. Only the missing or corrupted output will be recomputed. default is False.</li>
  <li><code>integration: (str) </code> Method to integrate delta-dbA values obtained from different chemical potentials, default is pca. choices=["pca", "mean_ddba", "med_ddba"] </li>
  <li><code>result_folder: (str path) </code>Folder to put the results (will be erased), default=result"</li>
  <li><code>seed: (int) </code>Random seed for background affinity sampling. 0 means time-based seed, default =1 </li>
  <li><code>med_ddba_p_value: (float) </code> A threshold on \"median delta-dbA P-value\",default is None "</li>
  <li><code>max_rank: (int)</code> Maximum number of PWMs to write in each side of the rankings, default =10</li>
 
  </ul>
  
