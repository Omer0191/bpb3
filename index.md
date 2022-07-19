![helsesorost](https://user-images.githubusercontent.com/79196757/116503417-50eaa000-a8b6-11eb-9925-382c86dc97c9.png) ![ous](https://user-images.githubusercontent.com/79196757/116503445-652e9d00-a8b6-11eb-8985-df71a9a4b9f2.png)![uio_segl_a](https://user-images.githubusercontent.com/79196757/179632843-0bd8b826-7fe3-4d3e-81c0-cf53647375b6.png)


# BayesPI-BAR in Python3 - bpb3

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Authors:

  <p align="center"><strong>  Junbai Wang <sup>1*,2,5</sup>, Mingyi Yang <sup>3,4</sup>, Magnar Bjørås <sup>4,6</sup>  </strong></p>
  
  <p align="center">1. Department of Pathology, Oslo University Hospital - Norwegian Radium Hospital, Oslo, Norway </p>
  <p align="center">2. Department of Clinical Molecular Biology in University of Oslo, Norway </p>
  <p align="center">3. Department of Medical Biochemistry, Oslo University Hospital and University of Oslo, Oslo, Norway</p>
  <p align="center">4. Department of Microbiology, Oslo University Hospital and University of Oslo, Oslo, Norway. </p>
  <p align="center">5. Department of clinical molecular biology (EpiGen), Akershus University Hospital, Lørenskog, Norway </p>
  <p align="center">6. Department of Clinical and Molecular Medicine, Norwegian University of Science and Technology, Trondheim, Norway </p>
<p align="center">*To whom correspondence should be addressed.Email: junbai.wang@medisin.uio.no </p>

<head>
	

</head>


## Abstract
<div class="container-fluid abstract_des">

<div class="row"> 
	<p> 
	BayesPI-BAR3 (or bpb3) is Bayesian method for protein–DNA interaction with binding affinity Ranking in Python3. 
It is a command line tool, which not only includes all R functions of previous BayesPI-BAR [1] and Python2 modules of BayesPI-BAR2[2,3], 
but also add a number of new functions and modules in the new bpb3 package (e.g., preprocess of download data from ICGC data portal, 
generate heatmap for predicted significant TF binding affinity changes, estimate significant TF binding affinity changes by using 
either clustered PWMs [5] or a two levels approach, and clean temporary files et al.) Especially, the previous BayesPI-BAR programs 
were implemented in Python2 and scatted to various command line scripts, which may not be suited for users with limited knowledge in Python. 
Bpb3 is upgraded to Python3 and can be easily installed in either Linux or MAC OS system, which can be simply called by users as 
the other build-in commands in the operating system. In particular, bpb3 provides a precompiled input parameter configure file, 
in which user can modify various parameters associated with running bpb3 pipeline such as input/output file location and disable/enable certain steps in the pipeline. 
Then, the parameter configure file can be directly loaded into bpb3 package for running the user desired calculation automatically. 
It significantly simplifies the application of bpb3 in different tasks. Demos of these new functions and examples are provided in the package.
</p>
	
</div>

	
## How to start:
<div class="container-fluid abstract_des">
bpb3 is written in python. It can be installed and accessed from command line and is avalible for both linux and mac operating systems. The package can be downloaded <strong> here </strong> .

Prior to installing the package, dependencies must be fulfilled. List of dependencies is as follows:
<ul>
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
	<li>matlab.engine</li>
	<li>numba</li>
	<li>beautifulsoup4==4.9.3</li>
	<li>bs4==0.0.1</li>
	<li>fpdf==1.7.2</li>
	<li>joblib==1.0.1</li>
	<li>kiwisolver==1.3.1</li>
	<li>matplotlib==3.3.4</li>
	<li>Pillow==8.1.2</li>
	<li>scikit-learn==0.24.1</li>
	<li>sklearn==0.0</li>
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
		
	
## Contents of the package:
<div class="container-fluid abstract_des">
		
<p>The package folder will contain following:
	</p>
<ul>
	<li><code>final_demo</code> : Contains demo data sets.</li>
	<li><code>bpb3</code> : Contains python soruce code of pipeline.</li>
	<li><code>readme.txt</code> : Instructions about usage of package.</li>
	<li><code>requirments.txt</code> :  List of requirments. Can be used for automatic installation from miniconda or pip.</li>
	<li><code>setup.py</code>: Setup file for package.</li>
	<li><code>final_demo_data</code>: Contains demo data.</li>


</ul>	
	


	
## Pipeline Tasks:
	
<div class="container-fluid abstract_des">
<p>The pipeline consists of follwoing tasks. To run a task, type bpb3 task args. To see what are the options for each task of the pipeline, please run: bpb3 -h </p>

<ul>
<li><code> [differential_expression](differential_expression.md) </code> : Predict differentialy expressed genes (DEG) based on two group of samples.</li>
	<li><code> gene_regions </code> : Extracts regions near transcription start sites of selected genes based on genCode gtf. </li>
	<li><code>mussd</code> : Mutation filtering based on the Space and Sample Distribution - MuSSD.</li>
	<li><code>highly_mutated_blocks</code> : Find blocks with significantly more mutations than would be expected.</li>
	<li><code>bayespi_bar</code>: BayesPI-BAR delta-dbA ranking computation for TF binding affinity affected by DNA mutation.</li>
	<li><code>choose_background_parameters</code>: Selects parameters for mutation background computation.</li>
	<li><code>background_affinity_changes</code> : Mutation background computation.</li>
	<li><code>affinity_change_significance_test</code> : Significant test of TF binding affinity changes between foreground and background affinity changes.</li>
	<li><code>parallel</code> : Run commands from the given file in parallel.</li>
	<li><code>make_cluster4pwm</code>: Make input PWM files for bpb3 based on clustered PWMs.</li>
	<li><code>bpb3selectedPWM</code>: The second level analysis of bpb3 by using the top PWMs in TF ranking after the first level analysis of bpb3 based on the clustered PWMs.</li>
	<li><code>run_pipeline</code>: Run full bpb3 pipeline (e.g., the first level analysis of bpb3 if clustered PWMs are used in the calculation).</li>
	<li><code>clean_tmp</code>: Clean temporary files from output folders.</li>

</ul>	
 
Click on the module for more details:
[differential_expression](differential_expression.md)
[gene_regions](gene_regions.md)  
[mussd](mussd.md)
[highly_mutated_blocks](highly_mutated_blocks.md)
[bayespi_bar](bayespi_bar.md)
[choose_background_parameters](choose_background_parameters.md)
[background_affinity_changes](background_affinity_changes.md)
[affinity_change_significance_test](affinity_change_significance_test.md)
	
## Demo
<div class="container-fluid abstract_des">

<p>Test run is available in final_demo folder.
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
	

	
	
          		 
         	
         		
         		
         			
         	
         		
         		
         	
Having trouble with package? Contact us @ junbai.wang@medisin.uio.no and we will be glad to help you.
