## mussd
<p>Mutation filtering based on the Space and Sample Distribution - MuSSD.</p>

### Required Parameters:

<ul>
  <li><code>patient_mutations: </code> List of VCF files with somatic mutations, one per patient </li>
  <li><code>genome: </code> Reference genome in FASTA format </li>
  
</ul>



### Optional Paramaters:

  
<ul>
  <li><code>regions: </code> BED file with regions of interest. All mutations outside of these "
                                            "regions will be discarded, default is None"</li>
<li><code>result_folder: </code>folder to put the results (will be erased), default is result",</li>
  <li><code>cluster_distance: </code> maximum distance between mutations in a hot region, default=30"</li>
<li><code>block_distance: </code>aximum distance between hot regions in a block, default=1000"</li>
  <li><code>min_block_size: </code> minimum number of mutations in a hot region, default=2</li>
<li><code>min_patients_in_block: </code>minimum number of different patients' mutations in a hot region, can be an integer or a float between 0 and 1, meaning the fraction of total number of patients, default=2</li>
  <li><code>block_flank: </code> number of base pairs to add to each side of the block when extracting sequence, default=25</li>
  <li><code>take_blocks_from: </code> do not compute mutation blocks, take them from the specified file instead. The file format is the same as blocks_summary.tsv in the output"</li>
<li><code>patient_germline_mutations: </code>list of VCF files with germline mutations, one per patient. The order of files must correspond to theorder of --patient_mutations list. The reference sequences for patients will contain these mutations. default is None</li>
</ul>


## Modules:
[Home](index.md) | [Differential Expression](differential_expression.md) | [Gene Regions](gene_regions.md) | [Mussd](mussd.md) | [Highly Mutated Blocks](highly_mutated_blocks.md) | [BayesPiBar](bayespi_bar.md) | [Choose Background Parameters](choose_background_parameters.md) | [Background Affinity Changes](background_affinity_changes.md) | [Affinity Change Significance](affinity_change_significance_test.md) | [Parallel](parallel.md) | [Cluster for PWMs](make_cluster4pwm.md) | [bpb3 SelectedPWM](bpb3selectedPWM.md) | [Run Pipeline](run_pipeline.md) | [Clean temp](clean_tmp.md) 
