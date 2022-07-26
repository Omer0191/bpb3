# Parameter Configuration

<div class="container-fluid abstract_des">
This bpb3 parameter configure is for demo purpose
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

#### Project main Output path

<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> out_data_folder = os.path.abspath("../../final_demo_data/demo4_fl_cohort_small_cluster4pwm/out")</span>
	</div>	

#### Project input path for patient mutation data and gene expression data
<p>Use following code to set up Project input path for patient mutation data and gene expression data
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> patient_data_folder = os.path.join(out_data_folder,'../', "patient_data")
  </span>
</div>	


#### Project input path for gene expression data of normal control samples
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> normal_rnaseq_folder = os.path.join(out_data_folder,'../', "normal_gcb_counts")
  </span>
</div>



#### Project name in logo file
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> project_name='demo4_fl_cohort_smallcluster4pwm'

  </span>
</div>

#### Input Genome path
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> genome_folder=os.path.abspath("../../final_demo_data/genome_data/hg19/")

  </span>
</div>

#Input human genome sequence
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> genome_fasta_file= os.path.join(genome_folder, "human_g1k_v37_decoy.fasta")

  </span>
</div>

#Input gtf file of human genes from GenCode
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> gene_annotation_file= os.path.join(genome_folder, "gencode.v19.annotation.gtf")

  </span>
</div>

#Project output folders for foreground and background calculations
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> foreground_folder = os.path.join(out_data_folder, "foreground")

  </span>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_folder = os.path.join(out_data_folder, "background")

  </span>
</div>

#Background pwm folder 
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_pwm_folder = os.path.join(out_data_folder, "pwm_for_background")

  </span>
</div>

#output folder of predicted muation blocks by MUSSD algorithm
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> mussd_result_folder = os.path.join(out_data_folder, "mussd_blocks")

  </span>
</div>

##### Set up input file name postprefix #########
#Input gene expression folder is located in patient data folder
#postprefix of gene expression file name for normal control samples such as files in folder normal_rnaseq_folder
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">normal_count_files_postprefix="*.only_counts.tsv"

  </span>
</div>

#gene length file name
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> gene_length_file = os.path.join(genome_folder, "gene_lengths.tsv")

  </span>
</div>

#postprefix of gene expression file name for patients such as files in folder patient_data_folder
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> donor_count_files_postprefix="D*/*_expression.tsv"

  </span>
</div>

#### 0. set up PWM file path for clustered PWMs or common PWMs 
##################Here is the only difference if input PWMs are either clustered PWMs or common PWMs! ################ 
################# Generate tempary pwms based on clustered and uncertain clustered PWMs ############
#Input path of clustered PWMs
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> in_clustered_pwms_path=os.path.join(out_data_folder,'../')

  </span>
</div>

# file folder of clustered PWMs passed quality control in abc4pwm package 
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> in_clustered_pwms_folder_name='abc4pwm_quality_assessed_out_seed5'

  </span>
</div>

# file folder of PWMs do not pass quality control in abc4pwm
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> in_uncertain_pwms_folder_name='abc4pwm_uncertain_pwms'

  </span>
</div>

# new input folder of clustered PWMs when reorganizing PWMs file names based on the two aforementioned folders.
# these renamed PWMs will be used as input PWMs for applying clustered  PWMs in bpb3 
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> out_tmp_pwms_folder_name='tmp_pwm'

  </span>
</div>

# final pwm folder path for TF binding affinity calculation.
# if we do not use clustered PWMs as input, then this can be simply replaced by a folder path of common PWMs such as the folder contains 1772 PWMs in bpb3
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> pwm_folder=os.path.join(in_clustered_pwms_path,out_tmp_pwms_folder_name)

  </span>
</div>

###########Setup Pipeline parameters from step 1 to step 8 before running bpb3 #########
#### 1. Differential gene expression options
#export file name for differentially expressed genes
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differentially_expressed_genes_file = os.path.join(out_data_folder, "differentially_expressed_genes.txt")

  </span>
</div>

#group name for tumor and normal samples
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> group1_str='tumor'

  </span>
  <pre class="bash"><code class="hljs"><span class="hljs-comment"> group2_str='normal'

  </span>
</div>


#Export gene expression files path
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> group1_median_rpkm_file = os.path.join(out_data_folder, group1_str + "_median_patient_rpkm.tsv")

  </span>
  <pre class="bash"><code class="hljs"><span class="hljs-comment"> group2_median_rpkm_file = os.path.join(out_data_folder, group2_str +"_median_patient_rpkm.tsv")


  </span>
</div>

# maximum Kolmogorov-Smirnov test or other statistic test P value to consider genes as differentially expressed
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_p = 0.05

  </span>
</div>


# whether to do quantile normalization of RPKM values, True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_quantile_normalization = True

  </span>
</div>


# whether to do log transformation of RPKM values, True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_log_transform = True

  </span>
</div>


# whether to do z-score transformation of RPKM values, True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">differential_expression_z_score_transform = False

  </span>
</div>


# minimum fold change of [quantile normalized] RPKM to consider genes as differentially expressed. None to disable
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> differential_expression_min_fold_change = None

  </span>
</div>


#export full expression data , True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> isExportAll = True

  </span>
</div>


#select test method:  1 for T-test, 0 for KS-test
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> test_method=1

  </span>
</div>


#minimum median RPKM allowed in each group, input 0 to disable this option
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> minimum_median_RPKM=0  #1.0

  </span>
</div>



#### 2. Region of interest selection options
# number of base pairs to take upstream of TSS
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> upstream_size = 1000

  </span>
</div>


# number of base pairs to take downstream of TSS
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> downstream_size = 1000

  </span>
</div>


#Export file path for extracted regions
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> regions_file = os.path.join(out_data_folder, "regions.bed")

  </span>
</div>

# If we do not use bpb3 function to extract a specified TSS regions, then manually input a bed format region file
# for example, using enhancer regions overlapping with Differential Methylation Regions for DNA muatation enrichment and the TF binding affinity change significance test 
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> regions_file='../demo7_mr_enhancers/in/dmr_intersect_enhancer_regions_chr18noChr_5kb_flank.tsv'

  </span>
</div>

#### 3. MuSSD options
# minimum number of patients in a hot mutation region
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> min_patients_in_block = 3

  </span>
</div>


# minimum number of mutations in a hot mutation region

<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> min_block_size = 3 

  </span>
</div>


# maximum distance between mutations in a hot mutation region
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> cluster_distance = 30

  </span>
</div>


# maximum distance between two adjacent mutaiton blocks
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> block_distance=500

  </span>
</div>


# number of base pairs to add to the left and right side of a mutation block when extracting sequences
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> block_flank = 25

  </span>
</div>

#### 4. P values for significant muation blocks
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> p_value_for_significant_blocks=0.001

  </span>
</div>


#commamnd line file name for running mussd
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> mussd_command_file=os.path.join(out_data_folder, 'run_mussd.sh')

  </span>
</div>


#whether to use bonferroni corrected p value, True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> pval_correction=True

  </span>
</div>

#patient mutation file names under folder patient_data_folder
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> patient_mut_files_postprefix="DO*/icgc_mutations*.tsv"

  </span>
</div>

#Export file path of significant mutation blocks
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> significant_blocks_file = os.path.join(out_data_folder, "significant_blocks.txt")

  </span>
</div>

#### 5. BayesPI-BAR options
# a range of chemical potentials to use
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> chemical_potentials = "none -10 -13 -15 -18 -20"

  </span>
</div>


# sequence shuffling iterations for dbA calculation
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> shuffling_iterations = 10000

  </span>
</div>


#Parallel option path
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> parallel_options_file = os.path.abspath(os.path.join(os.path.dirname(__file__), "parallel_options.txt"))

  </span>
</div>


#maximum number of TFs will be ranked in foreground calculation
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> max_ranking_for_foreground=30

  </span>
</div>


#whether both forground and background ddba are already exists, True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> start_from_integration=False

  </span>
</div>

#### 6. Background model options
# max rank of a PWM file in the foreground results to include in the background model
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> max_ranking_for_background = 20

  </span>
</div>


# number of random resampling
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">resampling_iterations = 10

  </span>
</div>


# number of genes will be sampled
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">gene_samples = 8

  </span>
</div>


# number of random shuffling in backgroun calculation<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_shuffling_iterations = 1000

  </span>
</div>

# command line file for running background calculation
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> background_command_file = os.path.join(out_data_folder, "make_background.sh")

  </span>
</div>

#### 7. mutation signature definition for generating background mutations, set to None to disable
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> mutation_signature_file = None  # "../../data/signature_7.tsv"

  </span>
</div>

# set to True to use tumor mutations from patients as background mutations, False otherwise.


<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> # This and the mutation signature are mutually exclusive.
<pre class="bash"><code class="hljs"><span class="hljs-comment"> # In both are disabled, uniform mutations will be generated
<pre class="bash"><code class="hljs"><span class="hljs-comment"> tumor_mutations_as_background = True

  </span>
</div>

# Results selection options for significant affinity changes
# P value for ranksum test in the output
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> affinity_change_p_value = 0.05

  </span>
</div>


# whether to use bonferroni corrected p value, True or False
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> pval_correction4affinity=True

  </span>
</div>


#signifcant block parameters, maximum number of top ranked PWMs
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">max_ranking_for_significant_blocks= 30

  </span>
</div>

## End of Parameter setup, below options for running each of the analysis pipeline in bpb3 ############
#### 8. Use True or False to either enable or disable the corresponding analysis step when running bpb3 #####

#step 1. differential expression analysis
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runDiffExp= True</span>
</div>

#step 2: region extraction
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">runRegionsFile= True
</span>
</div>

#step 3: mussd mutation block detection
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runMussd= True
</span>
</div>

#step 4: highly mutated mutation block test
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runHighMutBlocks= True
</span>
</div>

#step 5: do foreground bayespi-bar calculation
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runBayesPiBAR= True
</span>
</div>

#step 6: do background bayespi-bar calcuation
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">runBackgroundModel= True
</span>
</div>

#step 7: do TF affinity change significance test
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runBlockSignificance= True
</span>
</div>

#step 8: filter TF by gene expression level
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment">filterTFbyGene=True
 </span>
</div>

#step 9: plot heatmap for TFs with significaly changed binding affinity
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> isPlot=True  </span>
</div>

#step 10: remove temporary files in both foreground and background calculations
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runRemoveTempFile= True </span>
</div>

#option step: if the input PWMs are clustered PWMs from abc4pwm, then this option shall be True, otherwise it is False.
<p>Use following code to set up Project input path for gene expression data of normal control samples
	</p>
<div class="container-fluid abstract_des">
<pre class="bash"><code class="hljs"><span class="hljs-comment"> runCluster4PWM=True  </span>
</div>


		

	
