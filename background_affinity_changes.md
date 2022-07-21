# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.


[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) 


## background_affinity_changes
<p>This program is used to compute mutation backgrounds based on selected parameters.</p>


<ul>
  <li><code>block_size: </code> the size of the block to take for background. It should be similar to size of the actual patient block that will be tested against this background, default is None</li>
    <li><code>genome: </code> reference genome in FASTA format</li>
    <li><code>regions: </code>BED file with regions of interest from which to take the background samples. This should be similar to regions of interest that were used to filter the mutations</li>


<li><code>mutations_distribution: </code>a space-separated list of numbers that represent the distribution of the number of mutations to apply to each background block. It should be similar to distribution of mutation counts in actual patients in the blocks. mussd.py outputs these distributions in the last column of the block_summary.tsv file. Give one number to have a constant mutation count in each background block, default is None</li>
  <li><code>result_folder: </code> Folder to put the results (will be erased), default is result</li>
<li><code>block_resample_iterations: </code> Number of times to perform sampling of blocks from regions. On each iteration, a number of random block will be selected from regions, default=1</li>
  <li><code>block_samples_to_take: </code> Number of samples to take from regions on each resampling iteration. For each sample, a region is chosen randomly from the input regions without replacement, and then a block of specified size is chosen randomly from that region. If this number is not specified, it is equal to the number of regions, meaning that each region will be sampled once, default is None" </li>
    <li><code>mutation_signature: </code> File containing the mutation signature to apply when generating mutations. Tab-separated two-column file with a header. First column is a k-mer specification with a nucleotide replacement in square brackets, i.e. A[C>A]A specifies a 3-mer mutation ACA -> AAA. The second column is the probability of the given replacement. Reverse-complement replacement will have the same probability. Default is None</li>  
 <li><code>background_mutations: </code> File containing background mutations to use. Tab-separated file without a header with at least 4 columns: chromosome, position, reference nucleotide, alternate nucleotide. If given, only these mutations will be selected in background blocks, default is None </li>
<li><code>pwm_folder: </code> Folder containing TF binding models in BayesPI .mlp format</li>
<li><code>chemical_potentials: </code> List of chemical potentials to use </li>
<li><code>iterations: </code> Iteration count for background affinity distribution calculation, default=10000</li>
  <li><code>p_value_cutoff: </code> Maximum dbA p-value to consider protein-DNA binding significanti, default=0.1</li>
<li><code>max_rank: </code> Maximum rank of a PWM file in the rankings to add to the background model , default = 30</li>
<li><code>normalize_dba: </code> Divide each dbA value by its standard deviation in the background sequence set, default is False</li>
<li><code>integration: </code> Method to integrate delta-dbA values obtained from different chemical potentials, default = pca</li>
  <li><code>seed: </code> Random seed for background affinity sampling. 0 means time-based seed, default is 1</li>
<li><code>start_from_integration: </code>do not compute the random blocks and their delta-dbA values, assume they are already computed. Start from integration, default is False.</li>
  <li><code>reuse_output: </code> Do not recompute the random blocks and their dbA values if they are already present in the result folder. This mode can handle partially computed results from an interrupted computation. Only the missing or corrupted output will be recomputed, default is False.</li>
</ul>
