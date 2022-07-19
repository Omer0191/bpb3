## differential_expression
<p>This program determines which genes are differentially expressed based on RNA-seq data for two groups of samples. RPKM values arecomputed for each sample, optionally normalized, and Kolmogorov-Smirnov test/T-test is then applied to them to determine significant difference between distributions of values of the two groups. Order of optional normalizations: 
    
  </p>
<ol> 
  <li>quantile normalization</li> 
  <li>log transform</li> 
  <li>z-score transform. </li> 
</ol>

### Required Parameters:
<ul>
  <li><code>group_1_count_files: </code>list of files with read counts for group 1 (e.g., tumor group). Each file must have at least two columns: gene name and count. </li>
  <li><code>group_2_count_files: </code>List of files with read counts for group 2 (e.g., normal group).Each file must have at least two columns: gene name and count.</li>
  <li><code>gene_lengths: </code>File with two columns: gene name and its length. Only genes listed in this file will be considered in the computation. Note that RPKM computation is affected by the set of considered genes".</li>
  
  </ul>
<ul>    
    
    <li><code>: </code>Folder containing TF binding models in BayesPI .mlp format, default is None.</li>
  <li><code>: (int) </code>Iteration count for background affinity distribution calculation, default =10000 </li>
  <li><code>: (float) </code>maximum dbA p-value to consider protein-DNA binding, default = 0.1.</li>
  <li><code>: </code>divide each dbA value by its standard deviation in the background sequence set, default is False,</li>
  <li><code>: </code>Do not compute delta-dbA values, assume they are already computed. Start from integration. default is False.</li>
  <li><code>: </code>Do not recompute dbA values if they are already present in the result folder. This mode can handle partially computed results from an interrupted computation. Only the missing or corrupted output will be recomputed. default is False.</li>
  <li><code>integration: (str) </code> Method to integrate delta-dbA values obtained from different chemical potentials, default is pca. choices=["pca", "mean_ddba", "med_ddba"] </li>
  <li><code>: (str path) </code>Folder to put the results (will be erased), default=result"</li>
  <li><code>: (int) </code>Random seed for background affinity sampling. 0 means time-based seed, default =1 </li>
  <li><code>: (float) </code> A threshold on \"median delta-dbA P-value\",default is None "</li>
  <li><code>: (int)</code> Maximum number of PWMs to write in each side of the rankings, default =10</li>
 
  </ul>

Optional Parameters



    

   

    optional.add_argument("--output_file", help="output file name. Two columns will be written: "
                                                "gene name and the corresponding KS test P-value. Only genes with "
                                                "P-values smaller than the threshold given by --p_value parameter will "
                                                "be written, default is -", type=argparse.FileType('w'),
                          metavar="FILE", default="-")

    optional.add_argument("--output_group_1_rpkm", help="output file name for gene expression in group 1. Two "
                                                        "columns "
                                                        "will be written: gene name and the corresponding median "
                                                        "RPKM "
                                                        "(quantile-normalized if --quantile_normalization is "
                                                        "specified) "
                                                        "across group 1 counts. default is None",
                          type=argparse.FileType('w'),
                          metavar="FILE")

    #added wang march 2021
    optional.add_argument("--output_group_2_rpkm", help="output file name for gene expression in group 2. Tow "
                                                        "columns "
                                                        "will be written: gene name and the corresponding median "
                                                        "RPKM "
                                                        "(quantile-normalized if --quantile_normalization is "
                                                        "specified ) "
                                                        "across group 2 counts. default is None", 
                           type=argparse.FileType('w'),
                            metavar="FILE")


    optional.add_argument("--p_value", help="P-value cutoff for the KS test or T-test, default= 0.05", type=float,
                          metavar="NUMBER", default=0.05)

    optional.add_argument("--quantile_normalization", help="apply quantile normalization to RPKM values of all "
                                                           "experiments, default is False",
                          action="store_true")

    optional.add_argument("--log_transform", help="apply log-transformation (ln(1 + x)) to all values, default is False",
                          action="store_true")

    optional.add_argument("--z_score", help="apply z-score transformation values of each experiment separately, default is False",
                          action="store_true")

    optional.add_argument("--min_fold_change", help="in addition to the KS-test or T-test, check that the minimum fold change in "
                                                    "median RPKM between the two groups is above the specified number. "
                                                    "If quantile normalization is "
                                                    "activated, the quantile normalized values are compared, default is None",
                          metavar="NUMBER", type=float)
    #addded by wang
    optional.add_argument("--min_medianRPKM", help ="check the median of RPKM in each group,"
                                                " and only keep genes with RPKM greater than the minimum value in bith groups."
                                               "If quantile normalization is activated, then the quantile normalized values are checked, default is None",
                          metavar="NUMBER", type=float)

    optional.add_argument("--output_all_values", help="put values (RPKM or their z-scores) for all input datasets as "
                                                      "additional columns in the output file, default is False",
                          action="store_true")
    #added by wang march 2021
    optional.add_argument("--test_method", help="Differential expression test methods: 0 for KS-test, 1 for T-test, default is 0 for KS-test",
                          metavar="NUMBER", type=int,default=0)

## Modules:
[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [Clean temp](clean_tmp.md) 
