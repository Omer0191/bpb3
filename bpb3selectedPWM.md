# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## bpb3selectedPWM
<p>This is the second level analysis of bpb3, to evaluate PWMs of the selected top N clustered PWMs from the first level analysis of bpb3 by using the clustered PWMs.</p>

### Required Parameters:
<ul>
  <li><code>cluster_out_path: </code> File path for clustered PWMs results</li>
<li><code>bpb3_out_path: </code> File path of bpb3 ranking based on clustered PWMs</li>
  <li><code>in_fileString4clustered_pwm: </code> File string or file folder/name used/contained for clustered PWMs such as quality_assessed_out_seed3</li>
<li><code>project_name: </code> Project name for the current calculation</li>
  <li><code>output_folder: </code> Output folder name for the current calculation </li>
  <li><code>in_seq_ref_file: </code> File name of reference genome sequence file</li>
  <li><code>in_seq_alt_file: </code> File name of alternative genome sequence file </li>

  
</ul>
  
### Optional Paramaters:


 <ul>
 <li><code>in_fileString4uncertain_pwm: </code> File string or file folder/name used/contained for untertain PWMs, default is uncertain_pwms </li>
<li><code>in_separateString4file: </code> String separation for joined new file name</li>
  <li><code>in_topRank_cutoff: </code> The cutoff value of top ranked results from the first level analysis of clustered PWMs , default=10</li>
<li><code>skip_dba_calculation: </code> Skip dba calculation in bbp3 if the results are already exist, default is False</li>
  <li><code>clean_tmp: </code> Clean temporary files in snp calculations default = false</li>
 <li><code>export_selected_pwms: </code> Export all selected pwms from cluster4pwm to a folder: selected_pwm default =false </li>
<li><code>export_pwm_to_different_folder: </code> Export folder path for pwms that are selected from cluster4pwm , default=false and all pwms will be exported to the folder: selected_pwm</li>
  <li><code>change_pwm_name: </code> Change pwm names for results of cluster4pwm by removing the first few labels of clustering information in each PWM, default =False</li>   
</ul>


## 
[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [Clean temp](clean_tmp.md) 
