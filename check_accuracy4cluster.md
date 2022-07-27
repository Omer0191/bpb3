# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Secondary Functions

## check_accuracy4cluster

### Required Parameters:
<ul>
  <li><code> in_cluster_out_path: </code> File path contains all clustered PWMs and uncertain
                        PWMs, such as '../data/out/sep8_run1</li>
<li><code> in_bpb3_ranking_path: </code> File path for bpb3 ranking results, such as ../data/ou
                        t/sep8_run1/test_67snps/foreground/test_seq/rankings/</li>
  <li><code> in_fileString4clustered_pwm: </code> File string or file folder/name used/contained for
                        clustered PWMs such as quality_assessed_out_seed3</li>

    
</ul>


### Optional Parameters:
<ul>
  <li><code>in_separateString4file : </code>string separation for joined new file name, default= ~ </li>
<li><code>in_topRank_cutoff : </code>Top rank cutof value for selected TFs for comparison,
                        default=10 </li>
  <li><code> in_fileString4uncertain_pwm: </code> File strin or file folder/name used/contained for
                        untertain PWMs such as uncertain_pwms</li>

    
</ul>  

[Home](index.md)
