## differential_expression
<p>This program determines which genes are differentially expressed based on RNA-seq data for two groups of samples. RPKM values arecomputed for each sample, optionally normalized, and Kolmogorov-Smirnov test/T-test is then applied to them to determine significant difference between distributions of values of the two groups. Order of optional normalizations: 
    
  </p>
<ol> 
  <li>quantile normalization</li> 
  <li>log transform</li> 
  <li>z-score transform. </li> 
</ol>

