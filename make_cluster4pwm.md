# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [make_cluster4pwm](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [clean_tmp](clean_tmp.md)  



## make_cluster4pwm
<p>This function makes input PWMs files for bpb3 by using clustered PWMs from abc4pwm.</p>

### Required Parameters:


<ul>
  <li><code>in_pwm_path: </code>File path contains all clustered PWMs and uncertain
                        PWMs </li>
<li><code>in_clustered_pwm_folder: </code>File folder has all clustered PWMs, such as clustered_
                        pwm_folder/DBD_name/out/cluster_number/repres/cluster_
                        number_rep.mlp
</li>

</ul>


### Optional Parameters


<ul>
  <li><code>out_file_folder: </code>output file folder for renamed pwm files,default=tmp_pwm </li>
<li><code>in_file_postfix: </code>post prefix by file extension , default=*.mlp</li>
  <li><code>in_uncertain_pwm_folder: </code>File folder has uncertain pwms or pwms are not assigned to clusters, default=uncertain_pwms </li>
<li><code>in_separateString4file: </code>string separation for joined new file name, default= ~</li>
  <li><code>in_folder_depth4clustered_pwm: </code> folder depth for clustered pwms that will be used as new file name, default =-6</li>
  <li><code>in_folder_depth4uncertain_pwm: </code> folder depth for uncertain pwms that will be used as new file name, default = -2</li>

</ul>

