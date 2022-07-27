# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Secondary Functions

## plot_result
<p> This demoe script produces heatmaps like the one in the package paper. For general use, you may need to edit the layout, font sizes etc. so that everything is visible.</p>
<ul>
  <li><code>background_folder: </code>folder containing the computed background model
                        produced by background_affinity_changes.py </li>
<li><code>foreground_folder: </code>folder containing the computed delta-dba values for
                        patient data produced by bayespi_bar.py</li>
  <li><code>significant_pwms: </code> file containing the table of PWMs which have
                        significant affinity changes, produced by
                        affinity_change_significance_test.py
</li>

  
</ul>

### Optional Parameters:

<ul>
  <li><code>output_file: </code>output file name. If not specified, the plot will be
                        displayed on the screen </li>
<li><code>title: </code>plot title</li>
  <li><code>show: </code> show the plot on the screen (this may not look exactly
                        the same as the saved picture)</li>
<li><code>use_tags: </code>use the last column of the --significant_pwms file
                        instead of PWM file names (the second column) for plot
                        labels</li>
  
</ul>  

[Home](index.md)
