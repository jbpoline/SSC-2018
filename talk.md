---
title: A Brief History of Imaging Genetics 
shortitle:  Imaging Genetics
subtitle: A reproducibility perspective 
date:  June 25 2017
author: JB Poline \newline
institute: UC Berkeley, McGill	

header-include:
	- \usefonttheme{professionalfonts}
	- \usepackage{fontspec}
	- \setsansfont[BoldFont = {Fira Sans Medium}]{Fira Sans}
	- \setmonofont{Fira Mono}
        - \usepackage{amsmath}
---
A short history of imaging genetics - the reproducibility view
======================================================

- Motivations
- Quick background on genetic variations
- An historical perspective
- Some practical examples : How do I compute ... ?
- What will we need in the future

Motivations
=============================
- Geneticists: understand the genes 
- Neuroscientists: understand the brain
- Psychologists: understand the behaviour
- Clinicians: 
	- Personalized medicine
	- Predictive medicine
- No great model system for human brain!

Motivations: illustration
=============================

![Meyer-Lindenberg, 2006](./images/meyer-lindenberg-imag-genetic.png){ height=240px }

<!--
Motivations behind imaging genetics are also really important - what biological questions can we answer: mechanism of action for genes involved in neuropsychiatric diseases, genes influencing the expansion of the human brain as compared to other species, genes influencing function of the human brain (no great way to study this other than neuroimaging - model systems like mouse do not have human capabilities, humans not an easy experimental system)
-->

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

* Example of Hariri 2002: In Fig 3, Authors report $m_1 = .28, m_2 = .03, \textrm{SDM}_1 = 0.08, \textrm{SDM}_2 = 0.05, N_1 = N_2 = 14$ $\vspace{-0.20cm}$
    - ![Hariri et al. Science, 2002](./images/hariri_fig3.pdf)
$\vspace{-0.10cm}$

* How do we compute the effect size ? 
    - we know: the means, the standard deviations, and the Ns. 

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

    - get $\sigma$ from $\textrm{SDM}$ : $\sigma = \sqrt{14-1}\textrm{SDM}$
    - Combine the $\sigma$ to have one estimation across the groups
        - formula easy to recompute or find
    - $\sigma = \sqrt(14-1)\textrm{SDM}$, $d = \frac{m_1 - m_2}{\sigma} = 1.05$ 
\pause
\vspace{.4cm}
    - What is the percentage of variance explained ? 
\pause
\vspace{.4cm}
    - Write the estimated model: $Y = [1 \ldots 1]^t [m_1-m_2] + \textrm{residual}$
    - Compute the total sum of square, then the proportion: 
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
   \item  What is the Z score for p =  6.63e-10 ? : n01.isf(6.63e-10) = 6.064
   \pause
   \item  From Z score to Cohen's d ?  6.064/sqrt(733) = 0.224
   \end{itemize}
\pause
\item Question: what is the power for p=5.e-8 and d=0.22, N=733? 
\end{itemize}


Effect size in imaging genetics
=================================

\begin{itemize}
    \item BDNF and hippocampal volume: genuine effect or winners curse? d=0.12, p=0.02, Molendijk (2012)
\pause
    \item Stein et al, 2012: marker is associated with 0.58\% of intracranial volume per risk allele 
\pause
    \item Flint 2014: Effect size of intermediate phenotype not much greater than others 
\pause
    \item For psychiatric diseases: mean OR is 1.15, QT: variance explained by 1 locus << 0.5\%, 0.1-0.3\% for protein or serum concentration 
\end{itemize}

Some example of SNP effect size
=================================

![Franke et al., 2015](./images/franke-2015-effect-size.png){ height=200px }

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

* See also Silver et al., 2012, Richiardi 2015

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

- Combinaison of imaging and of genetics issues (the "AND" problem) 
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




Conclusion 3: What's next   
======================================================

* Greater interpretability 
	- include pathways / biological information
	- heritable phenotypes
	- analyzing other existing databases / datasets (eg ABI) 
	- more complex methods (multivariate) 

* More documented data needed for 
	- power
	- interpretability

* Move from p-values to prediction ?

Acknowledgements  
======================================================

* Berkeley: M. D'Esposito, M. Brett, S. Van der Walt, J.Millman
* Pasteur: R. Toro, G. Dumas, T. Bourgeron, A. Beggiato
* Neurospin: B. Thirion, G. Varauquaux, V. Frouin, others


Thank you for your attention - Questions ?
======================================================

More material
======================================================


What are the solutions: 
=========================

- Pre-register hypotheses 
    - More hypotheses 
    - Candidate versus GWAS: cf Flint & Mufano, 2012

> - Statistics: 
    - What is your likely effect size ?
    - Power analyses with the smallest expected effect size (cost does not enter in this calculation) 
    - Take robust statistical tools
    - Meta analysis - cf Enigma / Replication whenever possible 
    - Effect size variation estimation (bootstrapping)

The power issue
===================
What exactly is power ?
-----------------------
![Power: $\large{W = 1-\beta}$ Here W=77%](./images/what_is_pw.pdf)

Cohen's d and relation with n :
---------------------------------
$\hspace{3cm} d = \frac{\bar{x_1} - \bar{x_2}}{\sigma} = \frac{\mu}{\sigma} \hspace{2cm}$ \large{$Z = \frac{\mu\sqrt{n}}{\sigma} = d \sqrt{n}$}


The power issue
===================
- Studies of low power have low probability of detecting an effect (indeed!)
- Studies of low power have low positive predictive value: $PPV = P(H1 True | Detection)$
- Studies of low power are likely to show inflated effect size 

The power issue
===================

- $PPV = P(H1 True | Detection) = \frac{W \, P_1}{\alpha \, P_0 + W \, P_1}$

- If we have 4/5 that H0 is true, and 1/5 that H1 true, with 30% power: PPV = 60%.


-------------  ----------- ----------  --------
 P1/P0 =0.25   power=0.10,  alpha=0.05 PPV=0.33  
 P1/P0 =0.25   power=0.30,  alpha=0.05 PPV=0.60  
 P1/P0 =0.25   power=0.50,  alpha=0.05 PPV=0.71  
 P1/P0 =0.25   power=0.70,  alpha=0.05 PPV=0.78  
-------------  ----------- ----------  --------

The power issue
===================
What happens with more stringent $\alpha$?
-------------------------------------------------

![higher type I error threshold to account for MC](./images/pw_with_mc.pdf)

* effect on power: power goes down
* effect on PPV: PPV goes up 
* effect on estimated effect size: size bias: goes up

The power issue
===================

Studies of low power inflate the detected effect (2)
----------------------------------------------------

![Repeating experiments: estimated effects are above t05 line, leading to a biased estimation compared to true simulated effect.](./images/power_true.pdf)

The power issue
===================

Studies of low power inflate the detected effect (1)
-----------------------------------------------------

![Button et al. NRN, 2013](./images/butt_fig5.pdf)

The power issue
===================

What is the estimated power in common meta analyses? 
-----------------------------------------------------

![Button et al. NRN, 2013](./images/butt_fig2.pdf)

Power Calculator with 
======================

* Purcell et al. “Genetic Power Calculator” Bioinformatics (2003).

$\vspace{-0.5cm}$

![http://pngu.mgh.harvard.edu/~purcell/gpc/](./images/gene_pw_calc.pdf)

$\vspace{-0.5cm}$

> * http://www.sph.umich.edu/csg/abecasis/cats/

CaTS-text --additive --risk 1.3 --pisample .95 --pimarkers 1. --frequency .3 --case 1067 --control 1067 --alpha 0.00000001 : yields For a one-stage study 0.314.


Recall-by-Genotype and intermediate phenotype
===============================================

* Flint et al., Assessing the utility of intermediate phenotype, Trends in Neurosciences, 2014.

$\vspace{-0.5cm}$

![Recall by Genotype: Genotypic assignment vs randomisation assignment](./images/flint_2014_fig1_recall.pdf)


