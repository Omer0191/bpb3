![helsesorost](https://user-images.githubusercontent.com/79196757/116503417-50eaa000-a8b6-11eb-9925-382c86dc97c9.png) ![ous](https://user-images.githubusercontent.com/79196757/116503445-652e9d00-a8b6-11eb-8985-df71a9a4b9f2.png)

# BayesPI-BAR in Python3 - bpb3

bpb3 is a software tool for Bayesian method for proteinâ€“DNA interaction with binding affinity Ranking in Python3.

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
To install the package, go to the AffinityPropogation_Clustering directory and type: python setup.py install
For more detials, follow the readme file in the package
</div>
	
## Contents of the package:
<div class="container-fluid abstract_des">
		
<p>The package folder will contain following:
	</p>
<ul>
	<li><code>demo</code> : Contains demo data sets.</li>
	<li><code>abc4pwm</code> : Contains python soruce code of pipeline.</li>
	<li><code>readme.txt</code> : Instructions about usage of package.</li>
	<li><code>requirments.txt</code> :  List of requirments. Can be used for automatic installation from miniconda or pip.</li>
	<li><code>setup.py</code>: Setup file for package.</li>
	<li><code>data</code>: Contains in and out for demo.</li>


</ul>	


## Pipeline Tasks:
<div class="container-fluid abstract_des">
<p>The pipeline consists of follwoing tasks. To run a task, type abc4pwm <task> [<args>]. To see what are the options for each task of the pipeline, please run: abc4pwm -h </p>

<ul>
	<li><code>cleandatabase_for_classification</code> : Uniformly TF named database for associating pwms with DNA binding domain.</li>
	<li><code>classification</code> : Classification of input pwms into their DNA binding domains.</li>
	<li><code>clustering</code> : Clustering of similar looking position weight matrices.</li>
	<li><code>representative_motif</code> : This module makes a representative mofit of the cluster.</li>
	<li><code>quality_assessment</code>: This modules automatically asses the quality of clusters of pwms.</li>
	<li><code>visualize</code>: To visualize the clusters through boxplots etc.</li>
	<li><code>plot_cluster_motifs</code> : To plot the sequence motif of clusters' pws and representative motif.</li>
	<li><code>text_tfdb</code> : Obtaining a database in text formate with details of sources and names used in package.</li>
	<li><code>ensemble_learning</code> : A module to predict pwms using bayesPI with ensemble learning.</li>
	<li><code>ensemble_investigate</code>: A module to cluster and search the predicted pwms against a database.</li>
	<li><code>conversion</code>: Conversion of files from one (e.g., ab4pwm) to other (e.g., TRANSFAC, JASPAR).</li>
	<li><code>searching</code>: A module to search a TF pwm (motif) against the database..</li>



</ul>	

## Demo
<div class="container-fluid abstract_des">

<p>Test run is available on human pwms data, present in demo folder.
In folder abc4pwm/demo , there demos of all modules and study cases which can be run by entering: ./demo , in the command line to run the demo automatically.
In folder abc4pwm/demo , there demos of all modules and study cases. </p>

Having trouble with package? Contact us @ omerali.0191@gmail.com, junbai.wang@medisin.uio.no and we will be glad to help you.
