# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) 


## choose_background_parameters
<p>This program selects parameters (block size, mutation distribution, set of PWM files) for background computation based on selected mutation blocks obtained by mussd.py. It will create a shell script with the command to create the background model with selected parameters.</p>




 ## Required parameters:
<ul>
    <li><code>blocks_folder: </code> The folder containing mussd.py output.</li>
<li><code>block_ids: </code> The space-separated list of block IDs against which the background model is being made</li>
  <li><code>foreground_folder: </code> the folder containing bayespi_bar.py output for each selected block"</li>
<li><code>pwm_folder: </code>folder containing TF binding models in BayesPI .mlp format</li>
  <li><code>background_pwm_folder: </code> folder where to put PWM files selected for background"</li>
    <li><code>background_output_folder: </code> folder where to put the background model</li>
<li><code>regions: </code>BED file with regions of interest from which to take the background samples. This should be similar to regions of interest that were used to filter the mutations</li>
  <li><code>genome: </code> reference genome in FASTA format</li>


</ul>


## Optional parameters:
<ul>
  
  <li><code>output_file: </code> output file name. It will contain the command to create the background model, default is -</li>
<li><code>max_rank: </code>maximum rank of a PWM file in the rankings to add to the background model , default = 30</li>
  <li><code>block_resample_iterations: </code> umber of times to perform sampling of blocks from regions. On each iteration, a number of random blocks will be selected from regions, default =1</li>
<li><code>block_samples_to_take: </code>number of samples to take from regions on each resampling iteration. For each sample, a region is chosen randomly from the input regions without replacement, and then a block of specified size is chosen randomly from that region. If this number is not specified, it is equal to the number of regions, meaning that each region will be sampled once, default is None</li>
  <li><code>mutation_signature: </code> File containing the mutation signature to apply when generating mutations. Tab-separated two-column file with a header. First column is a k-mer specification with a nucleotide replacement in square brackets, i.e. A[C>A]A specifies a 3-mer mutation ACA -> AAA. The second column is the probability of the given replacement. Reverse-complement replacement will have the same probability. Default is None</li>  

 <li><code>background_mutations: </code>file containing background mutations to use. Tab-separated file without a header with at least 4 columns: chromosome, position, reference nucleotide, alternate nucleotide. If given, only these mutations will be selected in background blocks, default is None </li>
<li><code>isCluster4pwm: </code>whether input PWMs are clustered PWMs or not, default is False , original PWMs without cluster</li>
  <li><code>chemical_potentials: </code>list of chemical potentials to use </li>
<li><code>iterations: </code>iteration count for background affinity distribution calculation, default=10000</li>
  <li><code>p_value_cutoff: </code> aximum dbA p-value to consider protein-DNA binding significanti, default=0.1</li>
  <li><code>reuse_output: </code> do not recompute the random blocks and their dbA values if they are already present in the result folder. This mode can handle partially computed results from an interrupted computation. Only the missing or corrupted output will be recomputed, default is False</li>
<li><code>start_from_integration: </code>do not compute the random blocks and their delta-dbA values,assume they are already computed. Start from integration, default is False</li>
</ul>
