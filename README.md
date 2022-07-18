# bpb3
bpb3 --help
usage:  bpb3 <task> [<args>]

     Tasks available for using:
         differential_expression        Predict differentialy expressed genes (DEG) based on 
                                        two group of samples.
         gene_regions           Extracts regions near transcription start sites of selected 
                                genes based on genCode gtf. 
         mussd                  Mutation filtering based on the Space and Sample Distribution 
                                - MuSSD. 
         highly_mutated_blocks  Find blocks with significantly more mutations than would be expected.
         bayespi_bar            BayesPI-BAR delta-dbA ranking computation for TF binding affinity 
                                affected by DNA mutation.
         choose_background_parameters   Selects parameters for mutation background computation.
         background_affinity_changes    Mutation background computation.
         affinity_change_significance_test      Significant test of TF binding affinity changes 
                                                between foreground and background affinity changes.
         parallel               Run commands from the given file in parallel.
         make_cluster4pwm       Make input PWM files for bpb3 based on clustered PWMs.
         bpb3selectedPWM        The second level analysis of bpb3 by using the top PWMs in TF ranking 
                                after the first level analysis of bpb3 based on the clustered PWMs. 
         run_pipeline           Run full bpb3 pipeline (e.g., the first level analysis of bpb3 if 
                                clustered PWMs are used in the calculation).
         clean_tmp              Clean temporary files from output folders.

     Tasks available for demo purpose:
         plot_result            Generate heatmaps for selected mutation blocks. (demo) 
         filter_results_by_gene_expression_cluster4pwm  Filter those TF whose expression is too 
                                                        low in clustered PWMs. (demo)
         filter_results_by_gene_expression              Filter those TFs whose expression is too 
                                                        low (e.g., RPKM<0.03). (demo)
         make_plots_cluster4pwm         Make heatmap plots for all significant mutation blocks 
                                        that affecting clustered PWMs. (demo)
         make_plots                     Make heatmap plots for all significant mutation blocks 
                                        that affecting PWMs. (demo)
         check_accuracy4cluster Check accuracy for 67 SNPs that based on clustered PWMs. (demo)
         check_accuracy         Check accuracy for 67 SNPs that based on original PWMs. (demo)
         filterDEG4bpb3         Filter bpb3 exported differential expression gene list by rratios. (demo)
         preprocess_icgc_data   Preprocess of ICGC data such as a folder contains files donor_*, 
                                specimen, simple_somatic*, exp_seq.tsv et al. (demo)
     
 BayesPI-BAR in Python3 - bpb3

 positional arguments:
  task        Pipeline task to run

 optional arguments:
  -h, --help  show this help message and exit
