# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## make_cluster4pwm
<p>This function makes input PWMs files for bpb3 by using clustered PWMs from abc4pwm.</p>

### Required Parameters:
<ul>
  <li><code>foreground_folder: </code> Folder path for result of foreground</li>
<li><code>background_folder: </code> Folder path for result of background</li>
</ul>

### Optional Paramters:
</ul>
<li><code>sep_string_cluster4pwm: </code> String used to separate definitation of clustered PWMs such as quality_assessed~NAME~ or uncertain_pwms~NAME~, default is ~ </li>
<li><code>initial_string2clusteredPWMs: </code> Initial string for clustered PWMs such as quality_assessed~NAME~ default is quality_assessed.</li>
</ul>


## Modules:
[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [Clean temp](clean_tmp.md) 
