# BayesPI-BAR in Python3 - bpb3 Documentation

bpb3 is a software tool for Bayesian method for protein-DNA interaction with binding affinity Ranking in Python3.

## Secondary Functions

## make_plots_cluster4pwm

This is a demo script to generate heatmaps for all significant mutation blocks that affect TF binding based on calculation of clustered PWMs

### Required Parameters:

<ul>
  <li><code>foreground_folder: </code> Folder path for result of foreground</li>
<li><code>background_folder: </code> Folder path for result of background</li>
  <li><code>mussd_result_folder: </code> Folder path for result of mussd </li>

</ul>
  
  ### Optional Parameters:
<ul>
  <li><code>sep_string_cluster4pwm: </code> string used to separate definitation of clustered PWMs
                        such asquality_assessed~NAME~ or uncertain_pwms~NAME~,
                        default is ~</li>
<li><code>initial_string2clusteredPWMs: </code>initial string for clustered PWMs such as
                        quality_assessed~NAME~default is quality_assessed</li>

    
</ul>  

[Home](index.md)
