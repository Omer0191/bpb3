
 
<img align="center" src="https://user-images.githubusercontent.com/79196757/180248926-efd6e216-0683-4549-99f0-e6783224a2c7.png">
<img align="right" src="https://user-images.githubusercontent.com/79196757/180251608-da859f67-aa58-49e8-bea8-a0258be93635.png"><img align="left" src="https://user-images.githubusercontent.com/79196757/180251606-8e257ad0-86d5-4cb7-b549-ed5e5c0aa9eb.jpg">  



# BayesPI-BAR in Python3 
## bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.




## Modules:
[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [make_cluster4pwm](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [clean_tmp](clean_tmp.md)  
## How to start:
<div class="container-fluid abstract_des">
bpb3 is written in python. It can be installed and accessed from command line and is avalible for both linux and mac operating systems. The package can be downloaded <strong> here </strong> .

Prior to installing the package, dependencies must be fulfilled. List of dependencies is as follows:
<ul>
	<li>bedtools</li>
	<li>setuptools</li>
	<li>itertools</li>
	<li>pandas</li>
	<li>numpy</li>
	<li>argparse</li>
	<li>os</li>
	<li>shutil</li>
	<li>multiprocessing</li>
	<li>matplotlib</li>
	<li>seaborn</li>
	<li>datetime</li>
	<li>scipy</li>
	<li>tempfile</li>
	<li>time</li>
	<li>numba</li>

</ul>
It is advised to install dependencies using miniconda.
Package contains a file requirments.txt which can be used for automatic installation of dependencies from conda or pip.
To install the package, go to the bpb3_git directory and type: python setup.py install
For more details, follow the readme file in the package.
</div>
	
	
## Installation:
<div class="container-fluid abstract_des">
		
<p>You can download and install the package by follwing steps:
	</p>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> tar -zxf bpb3_git.tgz</span>
<span class="hljs-comment"> cd bpb3</span>
<span class="hljs-comment"> python setup.py install</span></code></pre>
	</div>	
	
## Contents of the package:
<div class="container-fluid abstract_des">
		
<p>The package folder will contain following:
	</p>
<ul>
	<li><code>final_demo</code> : Contains seondary functions scripts.</li>
	<li><code>bpb3</code> : Contains python soruce code of pipeline.</li>
	<li><code>readme.txt</code> : Instructions about usage of package.</li>
	<li><code>requirments.txt</code> :  List of requirements. Can be used for automatic installation from miniconda or pip.</li>
	<li><code>setup.py</code>: Setup file for package.</li>
	<li><code>final_demo_data</code>: Contains data in and out for the secondary functions.</li>


</ul>	
	
</div>

	
## Pipeline Tasks:
	
<p>The pipeline consists of follwoing tasks. To run a task, type bpb3 task args. To see what are the options for each task of the pipeline, please run: bpb3 -h </p>

<ul>
<li><code>differential_expression </code> : Predict differentialy expressed genes (DEG) based on two group of samples.</li>
	<li><code>gene_regions </code> : Extracts regions near transcription start sites of selected genes based on genCode gtf. </li>
	<li><code>mussd</code> : Mutation filtering based on the Space and Sample Distribution - MuSSD.</li>
	<li><code>highly_mutated_blocks</code> : Find blocks with significantly more mutations than would be expected.</li>
	<li><code>bayespi_bar</code> : BayesPI-BAR delta-dbA ranking computation for TF binding affinity affected by DNA mutation.</li>
	<li><code>choose_background_parameters</code> : Selects parameters for mutation background computation.</li>
	<li><code>background_affinity_changes</code> : Mutation background computation.</li>
	<li><code>affinity_change_significance_test</code> : Significant test of TF binding affinity changes between foreground and background affinity changes.</li>
	<li><code>parallel</code> : Run commands from the given file in parallel.</li>
	<li><code>make_cluster4pwm</code>:  Make input PWM files for bpb3 based on clustered PWMs.</li>
	<li><code>bpb3selectedPWM</code> : The second level analysis of bpb3 by using the top PWMs in TF ranking after the first level analysis of bpb3 based on the clustered PWMs.</li>
	<li><code>run_pipeline</code> : Run full bpb3 pipeline (e.g., the first level analysis of bpb3 if clustered PWMs are used in the calculation).</li>
	<li><code>clean_tmp</code>: Clean temporary files from output folders.</li>

</ul>
	
## Module details:

For more details of individual module and parameters, please go to repsective module page.

[differential_expression](differential_expression.md)  
[gene_regions](gene_regions.md)  
[mussd](mussd.md)  
[highly_mutated_blocks](highly_mutated_blocks.md)  
[bayespi_bar](bayespi_bar.md)  
[choose_background_parameters](choose_background_parameters.md)  
[background_affinity_changes](background_affinity_changes.md)  
[affinity_change_significance_test](affinity_change_significance_test.md)  
[parallel](parallel.md)  
[make_cluster4pwm](make_cluster4pwm.md)  
[bpb3selectedPWM](bpb3selectedPWM.md)  
  

	
## Secondary Funtions:
<div class="container-fluid abstract_des">

<p>Test run for use of secondary functions are available in final_demo folder.
In folder bpb3/final_demo , there demos of following modules: </p>

<ul>
	<li><code>plot_result</code> : Generate heatmaps for selected mutation blocks. (demo)</li>
	<li><code>filter_results_by_gene_expression_cluster4pwm</code> : Filter those TF whose expression is too low in clustered PWMs. (demo)</li>
	<li><code>filter_results_by_gene_expression</code> : Filter those TFs whose expression is too low (e.g., RPKM<0.03). (demo)</li>
	<li><code>make_plots_cluster4pwm</code> : Make heatmap plots for all significant mutation blocks that affecting clustered PWMs. (demo)</li>
	<li><code>make_plots</code>: Make heatmap plots for all significant mutation blocks that affecting PWMs. (demo)</li>
	<li><code>check_accuracy4cluster</code>: Check accuracy for 67 SNPs that based on clustered PWMs. (demo)</li>
	<li><code>check_accuracy</code> : Check accuracy for 67 SNPs that based on original PWMs. (demo)</li>
	<li><code>filterDEG4bpb3</code> : Filter bpb3 exported differential expression gene list by rratios. (demo)</li>
	<li><code>preprocess_icgc_data</code> : Preprocess of ICGC data such as a folder contains files donor_*, specimen, simple_somatic*, exp_seq.tsv et al. (demo)</li>
	
</ul>
</div>

## Details of Secondary Funtions:

For more details of individual function and parameters, please go to repsective page.
 [plot_result](plot_result.md)  
 [filter_results_by_gene_expression_cluster4pwm](filter_results_by_gene_expression_cluster4pwm.md)  
 [filter_results_by_gene_expression](filter_results_by_gene_expression.md)  
 [make_plots_cluster4pwm](make_plots_cluster4pwm.md)  
 [make_plots](make_plots.md)  
 [check_accuracy4cluster](check_accuracy4cluster.md)  
 [check_accuracy](check_accuracy.md)  
 [filterDEG4bpb3](filterDEG4bpb3.md)  
 [preprocess_icgc_data](preprocess_icgc_data.md)  
 
          		 
         	
           			
         	
         		
         		
         	
Having trouble with package? Contact us @ junbai.wang@medisin.uio.no and we will be glad to help you.
You can also go to <a href="https://bpb3.github.io/bpb3/">https://bpb3.github.io/bpb3/</a> for more information on demos and installation.
