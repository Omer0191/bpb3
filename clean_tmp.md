# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [make_cluster4pwm](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [clean_tmp](clean_tmp.md)  



## clean_tmp
<p>Clean temporary files in output folders, default only clean temporary files in background output. This function will remove intermediate result files that are not used anywhere so that it will reduce the result file size. </p>

### Required Parameters:
<ul>
   <li><code>background_out_file: </code> Background calculation output file folder</li>
<li><code>foreground_out_file: </code> Foreground calculation output file folder</li>
  <li><code>background_pwm_file: </code> Background PWM file folder</li>
<li><code>chemical_potentials: </code>A list of chemical potentials used in the calculations, space separeted string</li>

</ul>

### Optional Parameters:

<ul>
   <li><code>clean_both: </code> whether clean both foreground and background temporary files, default 0 for cleaning background, or 1 for foreground, or 2 for cleaning both foreground and background</li>

</ul>
