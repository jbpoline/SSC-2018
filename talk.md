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
\ 
======================================================

![\ ](./images/first-slide.png){ height=260px }

Multivariate associations in imaging genetics and related reproducibility issues
=================================================================================
- Motivations: why imaging genetics
\pause
- issues of reproducibility? 
	- in general (life science, epidemiology)
	- in imaging genetics (imaging, genetics, imaging genetics?)
\pause
- Motivations: why multivariate methods 
\pause
- The issues: 
	- curse of dimensionality with multiple testing 
	- interpretations
	- reproducibility 
\pause
- Solutions:
	- technical
	- social
\pause
- Conclusion

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

Issues of reproducibility in sciences 
=================================================================================
![Stodden, 2014](./images/credibility-crisis.png){ height=240px }

Issues of reproducibility in *life sciences*
=================================================================================
![Potti versus Baggerley and Combes](./images/potti.png){ height=240px }

Issues of reproducibility in *imaging* genetics  
=================================================================================
![Kattuwal, 2016, f.in. Brain Imaging Methods](./images/imaging-reproducibility-SPM-FSL-FS.png){ height=240px }

Issues of reproducibility in imaging *genetics*
=================================================================================
![Capacity to justify](./images/genetic-just-so-stories.png){ height=240px }

Issues of reproducibility in *imaging genetics*
=================================================================================

![Molendijk, 2012, BDNF and hippocampal volume](./images/molendijk_2012_f4.pdf) 

$\vspace{-1.2cm}$

![Mier, 2009, COMT & DLPFC](./images/mier_2009_f4.pdf)


<!--
- Hariri issue 
- sample size issue (Mufano, Ioannidis, ...)
- Jason Stein (1 slide : literature)
- False positives in neuroimaging genetics using voxel-based morphometry data (Silver et al., 2010) 
- Carp : method vibration workflow
- Nichols : method vibration 2
- FLS/FreeSurfer/SPM
-->

Effect size and reproducibility?
==========================================

\begin{itemize}
    \item HTTLPR and amygdala: Hariri 2002: p-value implies that locus explain > 40\% of phenotypic variance. d=1.05
    \item COMT and DLPFC: meta analysis : d = 0.55,  most studies N < 62 subjects (Meir, 2010) 
    \item KCTD8 / cortical area: Paus 2012: 21\% of phenotypic variance (250 subjects), d=1.03.
    \item Compare with effect size of APOE on hipocampal volume: Cohen's d=.22
\end{itemize}

Some example of SNP effect size
=================================

![Franke et al., 2015](./images/franke-2015-effect-size.png){ height=240px }

<!-- - \small{Franke et al., 2015 } -->

Motivations: why multivariate methods - some examples
=================================================================================
- Power issues and the curse of multiple testing 
- Better interpretability ? 
- Better inclusion of prior information?

<!--
Example of MV methods in imaging genetics : X4 slides
=================================================================================
- Lefloch et al
- Vounou, Tom Nichols
- Giovani Montana
- Identification of gene pathways implicated in Alzheimer's disease using longitudinal imaging phenotypes with sparse regression (Silver et al., )
-->

Multivariate approaches  
======================================================

* Effect of several genes - Effect on several regions

![J. Liu et al, 2009](./images/multivariate-snp-fMRI.png){ height=170px }

* Review: Calhoun et al., 2009. Application to Schizophrenia.

<!-- J. Liu et al., ICA guided Schizophrenia -->


Multivariate approaches: methods 
======================================================
<!-- $\vspace{-1.2cm}$ -->

![Vounou et al, 2010, LeFloch et al., 2012](./images/imaging-genetics-multivariate.png){ height=240px }



Multivariate approaches: cross-validation and permutations
===========================================================

![Computationally intensive](./images/cross-validation.png){ height=240px }

Multivariate approaches: methods 
======================================================
<!-- $\vspace{-1.2cm}$ -->

![LeFloch et al., 2012](./images/mv-methods-table-results.png){ height=120px }

$\vspace{-1.2cm}$

![LeFloch et al., 2012](./images/table-fsPLS-results.png){ height=120px }


Multivariate analyses: results 
======================================================

![Vounou et al, 2010, LeFloch et al., 2012](./images/lefloch_2012_sPLS_results.png){ height=240px }

* Then: issues of interpretation - and statistics needed to determine which region/voxel and which SNP/gene can be reported


Review and challenges in statistical methods for imaging genetics
=================================================================================

- Pluta et al, 2018
- issues are : 
	- dimensionality
	- ?

Issues / lack of reproductibility with MV methods (1)
=======================================================
- choice of methods still poorly justified
	- practitionners are selecting tools on the shelf rather than designing something for their question
	- Can also be influenced by the latest innovation read in NIPS/elsewhere
- choice of parameters such as number of dimensions, sparsity, etc makes for a large number of possible results. Validation is generally within a dataset 
- interpretation are done through "networks" but these may be artificial through mathematical constraints (eg PCA) which will depend on the signal to noise ratio
- imaging phenotypes are not always reliable
	- carp et al
	- FSL / SPM / ... 

Issues / lack of reproductibility with MV methods (2)
=======================================================
- true replication quasi inexistant datasets are very very sparse 
	- accessibility of datasets are poor - consortia are not dissiminating data
- populations even from the same ethnicity are not often comparable
	- change in age, gender ratio, SSE, ... all affecting phenotypes
- no consensus for the causes: See Bogdan et al, (2016 BPsy) 
- complexity issue
	- data suggest that subcortical volume abnormalities observed in schizophrenia may instead arise from rare mutations (e.g., de novo), schizophrenia itself (103), its treatment (104,105), associated risk factors, and potential gene 3 environment interactions (106). 
- Software availability : cf Stodden 2011 Nips experiment 

Solutions: What's next   
======================================================

* More documented data needed for 
	- power
	- interpretability

* Greater interpretability 
	- include pathways / biological information
	- heritable phenotypes
	- analyzing other existing databases / datasets (eg ABI) 
	- better adapted methods (multivariate) 

* Move from p-values to prediction ?


Conclusion: Ionanidis is very likely right   
======================================================


Acknowledgements  
======================================================

* Berkeley: M. D'Esposito, M. Brett, S. Van der Walt, J.Millman
* Pasteur: R. Toro, G. Dumas, T. Bourgeron, A. Beggiato
* Neurospin: B. Thirion, G. Varauquaux, V. Frouin, others






<!--
Genetic variations: 
===========================

![Scherer 2007, Credit S. Cichon](./images/genetic-variations.png){ height=240px }

Genetic variation: SNP
========================

![Credit S. Cichon](./images/SNP.png){ height=240px }

Genetic variation: CNV
========================

![Credit S. Cichon](./images/CNV.png){ height=240px }

The imaging genetic studies
===================================

- One variant, small Ns 
- GWAS, small then large Ns
- Genome-wide-Brain-wide
- Multivariate analyses
- [Heritability] 
- Networks
- Interpretation 

Some first studies: small Ns
==============================

![Hariri et al. Science, 2002](./images/hariri.png){ height=200px }
$\vspace{-0.10cm}$

* Authors report $m_1 = .28, m_2 = .03, \textrm{SDM}_1 = 0.08, \textrm{SDM}_2 = 0.05, N_1 = N_2 = 14$ 
* How do we compute the effect size ?  

Computing effect size
========================

What is the effect ?
---------------------

$\hspace{3cm}\mu = \bar{x_1} - \bar{x_2}$

What is the standardized effect ? (eg Cohen's d)
-------------------------------------------------

$\hspace{3cm}d = \frac{\bar{x_1} - \bar{x_2}}{\sigma} = \frac{\mu}{\sigma}$

"Z" : Effect accounting for the sample size 
--------------------------------------------------

$\hspace{3cm}Z = \frac{\mu}{\sigma / \sqrt{n}}$

Computing Effect size: practice
================================

* First, compute the standard deviation of the data from the $\textrm{SDM}$ 

    - get $\sigma$ from $\textrm{SDM}$ : $\sigma = \sqrt{14-1}\times\textrm{SDM}$
    - Combine the $\sigma$ to have one estimation across the groups
        - formula easy to recompute or find
    - $\sigma = \sqrt{14-1}\times\textrm{SDM}$, $d = \frac{m_1 - m_2}{\sigma} = 1.05$ 
\pause
\vspace{.4cm}
    - What is the percentage of variance explained ? 
\pause
\vspace{.4cm}
    - Write the estimated model: $Y = [1 \ldots 1]^t [m_1-m_2] + \textrm{residual}$
    - Compute the total sum of square $Y^t Y$, then the proportion: 
\pause
\vspace{.2cm}
    - \Large{$V_e = \frac{(n_1 + n_2)(m_1-m_2)^2}{n_1 s_1^2 + n_2 s_2^2 + (n_1 + n_2)(m_1-m_2)^2} > 40\%$}

Multiple hypothesis: the curse of GWAS--wise...
======================================================

![Shen et al., 2010](./images/gwas-right-hypo-GM-N=733-shen-2010.png){ height=200px }

- \small{See also Stein et al., 2010 (SNP X Voxel), Hibar et al., 2011, (Gene X Voxel) }

Computing effect size in imaging genetics (2)
===============================================

\begin{itemize}
\item Example of Shen et al using the ADNI cohort: Association of SNPs and the amount of GM in the hippocampus.
\pause
\item N = 733 subjects,  considered a large study for imaging, but a very small one for genome wide association. 
\pause
\item only APOE gene confirmed, p =  6.63e-10: reaches GWAS significance level of 5.e-8
\pause
\item Question: How would you compute the effect size for APOE ? 
   \begin{itemize}
   \pause
   \item  What is the Z score for p =  6.63e-10 ? : p-to-Z(6.63e-10) = 6.064
   \pause
   \item  From Z score to Cohen's d ?  6.064/sqrt(733) = 0.224
   \end{itemize}
\pause
\item Question: what is the power for p=5.e-8 and d=0.22, N=733? 
\end{itemize}


Effect size in imaging genetics
=================================

\begin{itemize}
    \item BDNF val/met and hippocampal volume: genuine effect or winners curse? d=0.13, p=0.02, Molendijk (2012)
\pause
    \item Stein et al, 2012: marker is associated with 0.58\% of intracranial volume per risk allele
\pause
    \item Flint 2014: Effect size of intermediate phenotype not much greater than others !
\pause
    \item For psychiatric diseases: mean OR is 1.15, QT: variance explained by 1 locus << 0.5\% and 0.1-0.3\% for protein or serum concentration 
\pause
    \item Franke et al., 2015: volume of hippocampus: -23 mm3 per SNP allele (~0.7\%) and OR=0.94 for schizophrenia vs control.
\end{itemize}

Some example of SNP effect size
=================================

![Franke et al., 2015](./images/franke-2015-effect-size.png){ height=230px }

<!-- - \small{Franke et al., 2015 } -->

Effect size and reproducibility?
==========================================

\begin{itemize}
    \item HTTLPR and amygdala: Hariri 2002: p-value implies that locus explain > 40\% of phenotypic variance. d=1.05
    \item COMT and DLPFC: meta analysis : d = 0.55,  most studies N < 62 subjects (Meir, 2010) 
    \item KCTD8 / cortical area: Paus 2012: 21\% of phenotypic variance (250 subjects), d=1.03.
\end{itemize}

Multivariate approaches 1 
======================================================

* Why ? Effect of several genes - Effect on several regions

![J. Liu et al, 2009](./images/multivariate-snp-fMRI.png){ height=170px }

* Review: Calhoun et al., 2009. Application to Schizophrenia.

<!-- J. Liu et al., ICA guided Schizophrenia -->

Multivariate approaches 2
======================================================
<!-- $\vspace{-1.2cm}$ -->

![Vounou et al, 2010, LeFloch et al., 2012](./images/imaging-genetics-multivariate.png){ height=200px }


Multivariate analyses: what do you get 
======================================================

![Vounou et al, 2010, LeFloch et al., 2012](./images/lefloch_2012_sPLS_results.png){ height=200px }

* Then: issues of interpretation - and statistics needed to determine which region/voxel and which SNP/gene can be reported

Heritability : more constraints - more interpretable
======================================================

* Definition (simple): percentage of variance due to genetic

![Toro et al, 2014](./images/toro-gcta-heritability.png){ height=200px }


Networks
======================================================

![Network SNP/Diffusion Chiang et al 2012](./images/network-diffusion-chiang-2012.png){ height=200px }

* See also Silver et al., 2012: Pathways, Richiardi 2015

<!--
Interpretation / Validation
======================================================

![Richiardi et al, 2015](./images/richiardi-2015-connectivity.png){ height=150px }

* Resting state networks in fMRI related to Allen Brain 
	- "Validation" on SNP / fMRI  
	- "Validation" on the mouse data

-->

A few specificities of Imaging Genetics
========================================

- Combinaison of imaging and of genetics potential pre-processing issues  
- Large number of subjects is necessary for GWAS and but too costly to scan  
- The multiple comparison issues
- The flexibility of analyses / exploration
- The "trendiness" of the field
- The capacity to "rationalize findings" 
    - noise in brain images is always interpretable
    - genes are always interpretable

Conclusion 1: Ioannidis again
======================================================

* Young fields tend to have less stringent criteria 
* Ioannidis 2005: When are results more likely to be false? 
    - The smaller the studies ...
    - The smaller the effect size ...
    - The larger the number of tests ...
    - The more flexibility in the analyses
    - The more trendy ...
    - The more financial interest ...

Conclusion 2: Effect-size = f(years, sample, ...)  
======================================================

![Molendijk, 2012, BDNF and hippocampal volume](./images/molendijk_2012_f4.pdf) 

$\vspace{-1.2cm}$

![Mier, 2009, COMT & DLPFC](./images/mier_2009_f4.pdf)






Thank you for your attention - Questions ?
======================================================

-->
