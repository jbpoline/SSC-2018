---
title: Multivariate associations in imaging genetics and related reproducibility issues
shortitle:  Imaging Genetics Reproducibility
subtitle: A reproducibility perspective 
date:  June 25 2018
author: JB Poline \newline
institute: UC Berkeley, McGill	

header-include:
	- \usefonttheme{professionalfonts}
	- \usepackage{fontspec}
	- \setsansfont[BoldFont = {Fira Sans Medium}]{Fira Sans}
	- \setmonofont{Fira Mono}
        - \usepackage{amsmath}
---

Multivariate associations in imaging genetics and related reproducibility issues
=================================================================================
- Issues of reproducibility? 
<!--- 	- in general in science ?
	- in life science / psychology ? 
	- in imaging genetics (imaging, genetics, imaging genetics?)
-->
\pause
- Motivations for imaging genetics and multivariate methods
\pause
- An example 
\pause
- The issues
	- reproducibility 
	- interpretations
\pause
- Solutions and conclusion

Issues of reproducibility in sciences 
=================================================================================
![Stodden, 2014](./images/credibility-crisis.png){ height=270px }

Issues of reproducibility in *life sciences*
=================================================================================
![Potti versus Baggerley and Combes](./images/potti.png){ height=270px }


Motivations : why imaging genetics
====================================
- Geneticists: understand the genes 
\pause
- Neuroscientists: understand the brain
\pause
- Psychologists: understand the behaviour
\pause
- Clinicians: 
	- Personalized medicine
	- Predictive medicine
\pause
- No great model system for human brain!

Motivations: illustration
=============================

![Meyer-Lindenberg, 2006](./images/meyer-lindenberg-imag-genetic.png){ height=240px }

<!--
Motivations behind imaging genetics are also really important - what biological questions can we answer: mechanism of action for genes involved in neuropsychiatric diseases, genes influencing the expansion of the human brain as compared to other species, genes influencing function of the human brain (no great way to study this other than neuroimaging - model systems like mouse do not have human capabilities, humans not an easy experimental system)
-->


<!--
Example of MV methods in imaging genetics : X4 slides
=================================================================================
- Lefloch et al
- Vounou, Tom Nichols
- Giovani Montana
- Identification of gene pathways implicated in Alzheimer's disease using longitudinal imaging phenotypes with sparse regression (Silver et al., )
-->

Motivations: why multivariate methods 
=================================================================================
- Power issues and the curse of multiple testing 
\vspace{.3cm}
\pause
- Accounting for pleotropic effects 
\vspace{.3cm}
\pause
- In general - getting closer to the biology 

Multiple hypothesis: the curse of GWAS...
======================================================

![Shen et al., 2010](./images/gwas-right-hypo-GM-N=733-shen-2010.png){ height=200px }

- \small{Stein, 2010 (SNP X Voxel) 10\^ -13, Hibar, 2011, (Gene X Voxel) 10\^ -10 }


Multivariate approaches: example 1 
======================================================

* A popular technique: starts with dimension reduction 

![J. Liu et al, 2009](./images/multivariate-snp-fMRI.png){ height=170px }

* Review: Calhoun et al., 2009. Application to Schizophrenia.

<!-- J. Liu et al., ICA guided Schizophrenia -->

Multivariate approaches: example 2 
======================================================
<!-- $\vspace{-1.2cm}$ -->

![Vounou et al, 2010, LeFloch et al., 2012](./images/imaging-genetics-multivariate.png){ height=240px }


Multivariate approaches: cross-validation and permutations
===========================================================

![Computationally intensive](./images/cross-validation.png){ height=240px }

Multivariate approaches: example 2
======================================================
<!-- $\vspace{-1.2cm}$ -->

* 94 subjects, fMRI data (language asymmetry), 34 regions of interest, 600000 SNPs

![LeFloch et al., 2012](./images/mv-methods-table-results.png){ height=110px }

Multivariate approaches: example 2
======================================================
<!-- $\vspace{-1.2cm}$ -->

![LeFloch et al., 2012](./images/table-fsPLS-results.png){ height=110px }


Multivariate analyses: results 
======================================================

![Vounou et al, 2010, LeFloch et al., 2012](./images/lefloch_2012_sPLS_results.png){ height=240px }


The issue of reproducibility in imaging genetics
=================================================================================
* Are the imaging phenotypes reliable? 
\vspace{.3cm}
\pause
* Is there any issue with the genetic data? 
\vspace{.3cm}
\pause
* What happened with the classical imaging genetic studies?

Issues of reproducibility in *imaging* genetics  
=================================================================================
<!--  FSL / SPM / ... -->

![Kattuwal, 2016, f.in. Brain Imaging Methods](./images/imaging-reproducibility-SPM-FSL-FS.png){ height=240px }

Issues of reproducibility in *imaging* genetics  
=================================================================================

![J. Carp, 2016](./images/carp-flexible-analyses.png){ height=240px }

* > 8000 pipelines for fMRI preprocessing lead to variation of the localization of the most significant activity

<!-- - Nichols : method vibration 2 -->

Issues of reproducibility in imaging *genetics*
=================================================================================

![Capacity to justify](./images/genetic-just-so-stories.png){ height=240px }

Issues of reproducibility in *imaging genetics*
=================================================================================

![Molendijk, 2012, BDNF and hippocampal volume](./images/molendijk_2012_f4.pdf) 

$\vspace{-1.2cm}$

![Mier, 2009, COMT & DLPFC](./images/mier_2009_f4.pdf)

Some example of SNP effect size
=================================================================================

![Franke et al., 2015](./images/franke-2015-effect-size.png){ height=240px }

<!-- - \small{Franke et al., 2015 } -->

Review and challenges in statistical methods for imaging genetics
=================================================================================

    "False positives, spurious results, and underpowered studies 
    are serious issues when considering the reliability and 
    reproducibility of imaging genetics results." 

\small{Pluta et al, 2018, Stat. challenge in connectome genetics}

\pause

- issues are : 
	- high dimensionality
	- "sample sizes for these studies are typically around 1000 subjects"


Issues / lack of reproductibility with MV methods
=======================================================
* "Networks" are extracted but these may be artificial through mathematical constraints (eg PCA): biological interpretation issue 
\pause
* A p-value on the MV association but how to report region/voxel and SNP/gene:
  interpretation (partial overlap with pathways/networks) and statistical issues
\pause
* "Networks" variation with SNR / QC / sample size / methods vibration?
\pause
* Choice of parameters such as number of dimensions, sparsity, etc makes for a
  large number of possible results
	- **within** a dataset optimization
\pause
* Choice of methods 
	- selecting tools on the shelf rather than design for a question
	- influenced by the latest innovation 

Issues / lack of reproductibility with MV methods (3)
=======================================================
* Replication very rare 
	- accessibility of datasets is poor 
	- most consortia are not disseminating data
\pause
* Populations even from the same ethnicity are often not comparable
	- change in age, gender ratio, SSE, ... are all affecting phenotypes
\pause
* "Concerns [of irreproducibility] are "heighten" with MV (Bogdan et al, Bio. Psy. 2017)
\pause
* Complexity issue: Carter, Bio-Psy, 2017
	- data suggest that subcortical volume abnormalities observed in
	  schizophrenia may instead arise from rare mutations (e.g., de novo),
	  schizophrenia itself (103), its treatment (104,105), associated risk factors,
	  and potential gene by environment interactions (106). 

Beware of cross validation failure !
=======================================================

![Varoquaux, 2017](./images/accuracy-prediction-sample-size.png){ height=240px }

Cross validation failure
=======================================================

![Varoquaux, 2017](./images/accuracy-prediction-methods.png){ height=170px }

* SVM or logistic regression, optionally with feature selection of 100, 200,
  500, 1 000, or 2 000 voxels and smoothing at 2, 4, or 6 mm

* Haxby dataset, inverted face and house labels in 50% of the sessions

Issues / lack of reproductibility with MV methods 
=======================================================
* Many points of variability 
	- starting dataset 
	- preprocessing steps
	- feature selection methods 
	- algorithm choice 
	- tuning of algorithm 
	- tuning of parameters: CV choice

Solutions: What's next (1) 
======================================================

* More **documented data** needed for 
	- power 
	- interpretability
	- generalizability
\pause
* More information on the algorithms is needed:
	- Clairebout's "advertisement versus scholarship"
	- **software availability**: cf 2011 Nips experiment 
	- software testing to be improved
\pause
* More biological constraints ? 
	- heritable phenotypes
	- when/how to include pathways, brain networks, or other biological information?

Solutions: What's next (2) 
======================================================

* More vibration studies
	- on the imaging phenotype measurement 
	- on the methods parameter choices
	- on the models 
\pause
* Find ways to accumulate confirmation results obtained with MV analyses?
	- release "image networks" in "FAIR" datasets 
	- release "gene sets" and weights in "FAIR" datasets 
	- make meta analyses possible across these objects?

Solutions (3): publish data and code 
======================================================

- _Increased transparency of methods and enhanced data sharing will further
  enhance replicability_ Carter, Bio. Psy., 2017

![Publishing code and data](./images/stodden-data-code-worflow-publish.png){ height=180px }


Conclusion: Ionanidis is very likely right   
======================================================

* Recent fields tend to have less stringent criteria 
\pause

* Ioannidis 2005: When are results more likely to be false? 
    - The smaller the studies ...
    - The smaller the effect size ...
    - The larger the number of tests ...
    - The more flexibility in the analyses
    - The more trendy ...
    - The more financial interest ...

Acknowledgements  
======================================================

* Pingzaho Hu for his invite
* McGill: A. Evans, C. Greenwood, B. Misic, S. Das, S. Brown 
* Berkeley: M. D'Esposito, M. Brett, S. Van der Walt, J.Millman
* Pasteur: R. Toro, G. Dumas, T. Bourgeron, A. Beggiato
* Neurospin: B. Thirion, G. Varauquaux, V. Frouin, others


Questions
======================================================

* Questions

Issues with / lack of reproductibility of MV methods 
=======================================================
* Analysis of the Acute Leukemia Dataset in "Molecular Classification of Cancer: Class Discovery and Class Prediction by Gene Expression Monitoring” (1999)

![Stodden, Golub dataset study](./images/stodden-golub-classif-method-variation.png){ height=120px }


