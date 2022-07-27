# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


## Parameter Configuration

<div class="container-fluid abstract_des">
This bpb3 parameter configure file will be directly loaded to bpb3 by run_pipeline module for running BayesPI-BAR2 analysis pipeline automatically with the predefined parameters.
</div>	

### Required libraries

<div class="container-fluid abstract_des">
		
<p>These are the required libraries for this file:
	</p>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> import os</span>
<span class="hljs-comment"> import glob</span>
<span class="hljs-comment"> import time</span>
<span class="hljs-comment"> from bpb3.script.script_high.other import common</span></code></pre>
	</div>	


## Setup main Paths and folders


### Project main Output path
<p> Use this paramter to set project main output path
	</p>

<div class="container-fluid abstract_des">

	<pre class="bash"><code class="hljs"><span class="hljs-comment"> out_data_folder = os.path.abspath("../../final_demo_data/demo4_fl_cohort_small_cluster4pwm/out") </span> </code></pre>
</div>

#### Project input path for patient mutation data and gene expression data

<p>Use following code to set up Project input path for patient mutation data and gene expression data
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> patient_data_folder = os.path.join(out_data_folder,'../', "patient_data")
  </span></code></pre>
</div>	


#### Project input path for gene expression data of normal control samples

<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> normal_rnaseq_folder = os.path.join(out_data_folder,'../', "normal_gcb_counts")
  </span></code></pre>
</div>



#### Project name in logo file
<p>Use following code to set up Project name in logo file
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> project_name='demo4_fl_cohort_smallcluster4pwm'</span></code></pre>
</div>

#### Input Genome path
<p>Use following code to set up Project name in logo file
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> genome_folder=os.path.abspath("../../final_demo_data/genome_data/hg19/")</span></code></pre>
</div>

##### Input human genome sequence
<p>Use following code to set up Input human genome sequence
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> genome_fasta_file= os.path.join(genome_folder, "human_g1k_v37_decoy.fasta")</span></code></pre>
</div>

####  Input gtf file of human genes from GenCode
<p>Use following code to set up Input gtf file of human genes from GenCode
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> gene_annotation_file= os.path.join(genome_folder, "gencode.v19.annotation.gtf")</span></code></pre>
</div>

#### Project output folders for foreground and background calculations
<p>Use following code to set up Project output folders for foreground and background calculations
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> foreground_folder = os.path.join(out_data_folder, "foreground")

  </span></code></pre>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_folder = os.path.join(out_data_folder, "background")</span></code></pre>
</div>

#### Background pwm folder 
<p>Use following code to set up Background pwm folder 
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_pwm_folder = os.path.join(out_data_folder, "pwm_for_background")</span></code></pre>
</div>

#### output folder of predicted muation blocks by MUSSD algorithm
<p>Use following code to set up output folder of predicted muation blocks by MUSSD algorithm
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> mussd_result_folder = os.path.join(out_data_folder, "mussd_blocks")</span></code></pre>
</div>

## Set up input file name postprefix 
#### Input gene expression folder is located in patient data folder postprefix of gene expression file name for normal control samples such as files in folder normal_rnaseq_folder
<p>Use following code to set up Input gene expression folder is located in patient data folder postprefix of gene expression file name for normal control samples such as files in folder normal_rnaseq_folder
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">normal_count_files_postprefix="*.only_counts.tsv"</span></code></pre>
</div>

#### gene length file name
<p>Use following code to set up gene length file name
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> gene_length_file = os.path.join(genome_folder, "gene_lengths.tsv")</span></code></pre>
</div>

#### postprefix of gene expression file name for patients such as files in folder patient_data_folder
<p>Use following code to set up postprefix of gene expression file name for patients such as files in folder patient_data_folder
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> donor_count_files_postprefix="D*/*_expression.tsv"</span></code></pre>
</div>

## 0. set up PWM file path for clustered PWMs or common PWMs 
<p> Here is the only difference if input PWMs are either clustered PWMs or common PWMs!  
 Generate tempary pwms based on clustered and uncertain clustered PWMs </p>
#### Input path of clustered PWMs
<p>Use following code to set up Input path of clustered PWMs
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> in_clustered_pwms_path=os.path.join(out_data_folder,'../')</span></code></pre>
</div>

#### file folder of clustered PWMs passed quality control in abc4pwm package 
<p>Use following code to set up file folder of clustered PWMs passed quality control in abc4pwm package 
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> in_clustered_pwms_folder_name='abc4pwm_quality_assessed_out_seed5'</span></code></pre>
</div>

#### file folder of PWMs which do not pass quality control in abc4pwm
<p>Use following code to set up file folder of PWMs which do not pass quality control in abc4pwm
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> in_uncertain_pwms_folder_name='abc4pwm_uncertain_pwms'
</span></code></pre>
</div>

#### new input folder of clustered PWMs 
<p> when reorganizing PWMs file names based on the two aforementioned folders. These renamed PWMs will be used as input PWMs for applying clustered  PWMs in bpb3. Use following code to set up new input folder of clustered PWMs 
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> out_tmp_pwms_folder_name='tmp_pwm'</span></code></pre>
</div>

#### final pwm folder path for TF binding affinity calculation.
<p> If we do not use clustered PWMs as input, then this can be simply replaced by a folder path of common PWMs such as the folder contains 1772 PWMs in bpb3. Use following code to set up final pwm folder path for TF binding affinity calculation.
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> pwm_folder=os.path.join(in_clustered_pwms_path,out_tmp_pwms_folder_name)</span></code></pre>
</div>

# Setup Pipeline parameters from step 1 to step 8 before running bpb3 

## 1. Differential gene expression options
<p>Use following code to set up export file name for differentially expressed genes
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differentially_expressed_genes_file = os.path.join(out_data_folder, "differentially_expressed_genes.txt")</span></code></pre>
</div>

#### group name for tumor and normal samples
<p>Use following code to set up group name for tumor and normal samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> group1_str='tumor'</span></code></pre>
  <pre class="bash"><code class="hljs"><span class="hljs-comment"> group2_str='normal'</span></code></pre>
</div>


#### Export gene expression files path

<p>Use following code to set up Export gene expression files path
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> group1_median_rpkm_file = os.path.join(out_data_folder, group1_str + "_median_patient_rpkm.tsv")</span></code></pre>
  <pre class="bash"><code class="hljs"><span class="hljs-comment"> group2_median_rpkm_file = os.path.join(out_data_folder, group2_str +"_median_patient_rpkm.tsv")</span></code></pre>
</div>

#### maximum Kolmogorov-Smirnov test or other statistic test P value to consider genes as differentially expressed
<p>Use following code to set up maximum Kolmogorov-Smirnov test or other statistic test P value to consider genes as differentially expressed
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_p = 0.05</span></code></pre>
</div>


####  Quantile normalization of RPKM values, True or False
<p> Whether to do quantile normalization of RPKM values, True or False. Use following code to set up 
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_quantile_normalization = True</span></code></pre>
</div>


####  log transformation of RPKM values, True or False
<p> Whether to do log transformation of RPKM values, True or False. Use following code to set up log transformation of RPKM values, True or False
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_log_transform = True</span></code></pre>
</div>


####  z-score transformation of RPKM values, True or False
<p> Whether to do z-score transformation of RPKM values, True or False. Use following code to set up whether to do z-score transformation of RPKM values, True or False
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">differential_expression_z_score_transform = False</span></code></pre>
</div>


####  minimum fold change of quantile normalized RPKM to consider genes as differentially expressed. 
<p>Use following code to set up minimum fold change of quantile normalized RPKM to consider genes as differentially expressed. None to disable
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_min_fold_change = None</span></code></pre>
</div>


#### export full expression data , True or False
<p>Use following code to set up export full expression data , True or False
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> isExportAll = True</span></code></pre>
</div>


#### select test method:  1 for T-test, 0 for KS-test
<p>Use following code to set up select test method:  1 for T-test, 0 for KS-test
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> test_method=1</span></code></pre>
</div>


#### minimum median RPKM allowed in each group, input 0 to disable this option
<p>Use following code to set up minimum median RPKM allowed in each group, input 0 to disable this option
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> minimum_median_RPKM=0  #1.0</span></code></pre>
</div>



## 2. Region of interest selection options
####  number of base pairs to take upstream of TSS
<p>Use following code to set up number of base pairs to take upstream of TSS
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> upstream_size = 1000</span></code></pre>
</div>


#### number of base pairs to take downstream of TSS
<p>Use following code to set up number of base pairs to take downstream of TSS
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> downstream_size = 1000</span></code></pre>
</div>


#### Export file path for extracted regions
<p>Use following code to set up Export file path for extracted regions
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> regions_file = os.path.join(out_data_folder, "regions.bed")</span></code></pre>
</div>

<p> If we do not use bpb3 function to extract a specified TSS regions, then manually input a bed format region file
for example, using enhancer regions overlapping with Differential Methylation Regions for DNA muatation enrichment and the TF binding affinity change significance test 
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> regions_file='../demo7_mr_enhancers/in/dmr_intersect_enhancer_regions_chr18noChr_5kb_flank.tsv'</span></code></pre>
</div>

## 3. MuSSD options
####  minimum number of patients in a hot mutation region

<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> min_patients_in_block = 3</span></code></pre>
</div>


####  minimum number of mutations in a hot mutation region

<p>Use following code to set up minimum number of mutations in a hot mutation region
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> min_block_size = 3 </span></code></pre>
</div>


####  maximum distance between mutations in a hot mutation region
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> cluster_distance = 30</span></code></pre>
</div>


#### maximum distance between two adjacent mutaiton blocks
<p>Use following code to set up maximum distance between two adjacent mutaiton blocks
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> block_distance=500</span></code></pre>
</div>


####  number of base pairs to add to the left and right side of a mutation block when extracting sequences
<p>Use following code to set up number of base pairs to add to the left and right side of a mutation block when extracting sequences
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> block_flank = 25</span></code></pre>
</div>

## 4. P values for significant muation blocks
<p>Use following code to set up P values for significant muation blocks
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> p_value_for_significant_blocks=0.001</span></code></pre>
</div>


#### commamnd line file name for running mussd
<p>Use following code to set up commamnd line file name for running mussd
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> mussd_command_file=os.path.join(out_data_folder, 'run_mussd.sh')</span></code></pre>
</div>


#### bonferroni corrected p value, True or False
<p>Use following code to set up whether to use bonferroni corrected p value, True or False
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> pval_correction=True</span></code></pre>
</div>

#### patient mutation file names under folder patient_data_folder
<p>Use following code to set up patient mutation file names under folder patient_data_folder
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> patient_mut_files_postprefix="DO*/icgc_mutations*.tsv"</span></code></pre>
</div>

#### Export file path of significant mutation blocks
<p>Use following code to set up Export file path of significant mutation blocks
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> significant_blocks_file = os.path.join(out_data_folder, "significant_blocks.txt")</span></code></pre>
</div>

## 5. BayesPI-BAR options
####  a range of chemical potentials to use
<p>Use following code to set up a range of chemical potentials to use
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> chemical_potentials = "none -10 -13 -15 -18 -20"</span></code></pre>
</div>


####  sequence shuffling iterations for dbA calculation
<p>Use following code to set up sequence shuffling iterations for dbA calculation
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> shuffling_iterations = 10000</span></code></pre>
</div>


#### Parallel option path
<p>Use following code to set up Parallel option path
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> parallel_options_file = os.path.abspath(os.path.join(os.path.dirname(__file__), "parallel_options.txt"))</span></code></pre>
</div>


#### maximum number of TFs will be ranked in foreground calculation
<p>Use following code to set up maximum number of TFs will be ranked in foreground calculation
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> max_ranking_for_foreground=30</span></code></pre>
</div>


#### Forground and background ddba already exists? True or False
<p>Use following code to set up whether both forground and background ddba are already exists, True or False
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> start_from_integration=False</span></code></pre>
</div>

## 6. Background model options
####  max rank of a PWM file in the foreground results to include in the background model
<p>Use following code to set up max rank of a PWM file in the foreground results to include in the background model
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> max_ranking_for_background = 20</span></code></pre>
</div>


####  number of random resampling
<p>Use following code to set up number of random resampling
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">resampling_iterations = 10</span></code></pre>
</div>


####  number of genes will be sampled
<p>Use following code to set up number of genes will be sampled
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">gene_samples = 8</span></code></pre>
</div>


####  number of random shuffling in backgroun calculation
<p>Use following code to set up number of random shuffling in backgroun calculation
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_shuffling_iterations = 1000</span></code></pre>
</div>

#### command line file for running background calculation
<p>Use following code to set up command line file for running background calculation
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_command_file = os.path.join(out_data_folder, "make_background.sh")</span></code></pre>
</div>

## 7. mutation signature definition for generating background mutations, set to None to disable
<p>Use following code to set up mutation signature definition for generating background mutations, set to None to disable
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> mutation_signature_file = None  # "../../data/signature_7.tsv"</span></code></pre>
</div>

####  set to True to use tumor mutations from patients as background mutations, False otherwise.


<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> # This and the mutation signature are mutually exclusive.</span></code></pre>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> # In both are disabled, uniform mutations will be generated</span></code></pre>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> tumor_mutations_as_background = True</span></code></pre>
</div>

###  Results selection options for significant affinity changes
#### P value for ranksum test in the output
<p>Use following code to set up P value for ranksum test in the output
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> affinity_change_p_value = 0.05</span></code></pre>
</div>


#### whether to use bonferroni corrected p value, True or False
<p>Use following code to set up whether to use bonferroni corrected p value, True or False
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> pval_correction4affinity=True</span></code></pre>
</div>


#### signifcant block parameters, maximum number of top ranked PWMs
<p>Use following code to set up signifcant block parameters, maximum number of top ranked PWMs
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">max_ranking_for_significant_blocks= 30</span></code></pre>
</div>

## End of Parameter setup, below options for running each of the analysis pipeline in bpb3 
## 8. Use True or False to either enable or disable the corresponding analysis step when running bpb3 #####

#### step 1. differential expression analysis
<p>Use following code to set up differential expression analysis
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runDiffExp= True</span></code></pre>
</div>

#### step 2: region extraction
<p>Use following code to set up region extraction
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">runRegionsFile= True</span></code></pre>
</div>

#### step 3: mussd mutation block detection
<p>Use following code to set up mussd mutation block detection
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runMussd= True</span></code></pre>
</div>

#### step 4: highly mutated mutation block test
<p>Use following code to set up highly mutated mutation block test
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runHighMutBlocks= True</span></code></pre>
</div>

#### step 5: do foreground bayespi-bar calculation
<p>Use following code to set up to do foreground bayespi-bar calculation
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runBayesPiBAR= True</span></code></pre>
</div>

#### step 6: do background bayespi-bar calcuation
<p>Use following code to set up to do background bayespi-bar calcuation
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">runBackgroundModel= True</span></code></pre>
</div>

#### step 7: do TF affinity change significance test
<p>Use following code to set up to do TF affinity change significance test
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runBlockSignificance= True</span></code></pre>
</div>

#### step 8: filter TF by gene expression level
<p>Use following code to set up to filter TF by gene expression level
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">filterTFbyGene=True</span></code></pre>
</div>

#### step 9: plot heatmap for TFs with significaly changed binding affinity
<p>Use following code to set up the plot heatmap for TFs with significaly changed binding affinity
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> isPlot=True  </span></code></pre>
</div>

#### step 10: remove temporary files in both foreground and background calculations
<p>Use following code to set up to remove temporary files in both foreground and background calculations
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runRemoveTempFile= True </span></code></pre>
</div>

#### option step: if the input PWMs are clustered PWMs from abc4pwm, then this option shall be True, otherwise it is False.
<p>Use following code to set up 
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runCluster4PWM=True  </span></code></pre>
</div>

[Home](index.md)
		

	
