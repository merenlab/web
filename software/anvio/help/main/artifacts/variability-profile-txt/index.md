---
layout: page
title: variability-profile-txt [artifact]
categories: [anvio]
comments: false
image:
  featurerelative: ../../../images/header.png
  display: true
---


{% include _toc.html %}


<img src="../../images/icons/TXT.png" alt="TXT" style="width:100px; border:none" />

A TXT-type anvi'o artifact. This artifact can be generated, used, and/or exported **by anvi'o**. It can also be provided **by the user** for anvi'o to import into its databases, process, and/or use.

Back to the **[main page](../../)** of anvi'o programs and artifacts.

## Provided by


<p style="text-align: left" markdown="1"><span class="artifact-p">[anvi-gen-variability-profile](../../programs/anvi-gen-variability-profile)</span></p>


## Required or used by


<p style="text-align: left" markdown="1"><span class="artifact-r">[anvi-display-structure](../../programs/anvi-display-structure)</span> <span class="artifact-r">[anvi-gen-fixation-index-matrix](../../programs/anvi-gen-fixation-index-matrix)</span> <span class="artifact-r">[anvi-script-calculate-pn-ps-ratio](../../programs/anvi-script-calculate-pn-ps-ratio)</span> <span class="artifact-r">[anvi-script-snvs-to-interactive](../../programs/anvi-script-snvs-to-interactive)</span> <span class="artifact-r">[anvi-script-variability-to-vcf](../../programs/anvi-script-variability-to-vcf)</span></p>


## Description

This artifact contains various information about the SNVs, SCVs, and SAAVs across a <span class="artifact-n">[profile-db](/software/anvio/help/main/artifacts/profile-db)</span> that is thoroughly described [on this blogpost](http://merenlab.org/2015/07/20/analyzing-variability/#the-output-matrix).  

This was generated by <span class="artifact-n">[anvi-gen-variability-profile](/software/anvio/help/main/programs/anvi-gen-variability-profile)</span>, which is also described on [that blogpost](http://merenlab.org/2015/07/20/analyzing-variability/#the-anvio-way). 

{:.notice}
Unsure what SNV, SCV, and SAAVs are or looking for a refresher? You can find that information [on the same blogpost](http://merenlab.org/2015/07/20/analyzing-variability/#an-intro-to-single-nucleotidecodonamino-acid-variation). 

In summary, this contains output matrices for your SNVs, SCVs and SAAVs that annotate them with lots of additional infomration. This way, you can interact with that data by running <span class="artifact-n">[anvi-script-snvs-to-interactive](/software/anvio/help/main/programs/anvi-script-snvs-to-interactive)</span> or incorporate it into your structural analysis when running <span class="artifact-n">[anvi-display-structure](/software/anvio/help/main/programs/anvi-display-structure)</span>. 

### What kinds of information? 

#### SNVs

For each of your SNVs, this matrix include their position in the contig and gene, sample, coverage data, the A, C, G, and T counts, the reference and consensus nucleotides, entropy value, and more. 

#### SCVs 

This information will only appear if you requested it when running your earlier analysis. To do this, use the flag `--profile-SCVs` when you run <span class="artifact-n">[anvi-profile](/software/anvio/help/main/programs/anvi-profile)</span> or <span class="artifact-n">[anvi-merge](/software/anvio/help/main/programs/anvi-merge)</span>. Then, when running <span class="artifact-n">[anvi-gen-variability-profile](/software/anvio/help/main/programs/anvi-gen-variability-profile)</span> use the flag `--engine CDN`. 

For each SCVs, this matrix details the position, sample, coverage data, count for each of the 64 codons (AAA, AAC, ..., TTG, TTT), entropy, synonymity, etc. 

#### SAAVs

Like the information about SCVs, this information will only appear if you requested it when running your earlier analysis. To do this, use the flag `--profile-SCVs` when you run <span class="artifact-n">[anvi-profile](/software/anvio/help/main/programs/anvi-profile)</span> or <span class="artifact-n">[anvi-merge](/software/anvio/help/main/programs/anvi-merge)</span>. Then, when running <span class="artifact-n">[anvi-gen-variability-profile](/software/anvio/help/main/programs/anvi-gen-variability-profile)</span> use the flag `--engine AA`. 

For each SCVs, this matrix details the position, sample, coverage data, count for each of the 20 amino acids (as well as the stop codon), entropy, BLOSUM62, etc. 

#### Structural information

If you provided <span class="artifact-n">[anvi-gen-variability-profile](/software/anvio/help/main/programs/anvi-gen-variability-profile)</span> with a <span class="artifact-n">[structure-db](/software/anvio/help/main/artifacts/structure-db)</span>, then you'll also have some additional columns to your matrices. These include structural annotations, how the residue responds to water, information about bond angles, and a list of residues that are in physical contact with the residue you're looking at. 

For more information on any of this, check out [this page](http://merenlab.org/2015/07/20/analyzing-variability/#the-output-matrix), where every column in these matrices is not only listed, but explained. 


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/artifacts/variability-profile-txt.md) to update this information.
