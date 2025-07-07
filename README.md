---
---
---

# Proteome-wide Screen for RNA-dependent Proteins of non-synchronized HeLa cells

##### Baureis, J., Ferdin, J., Nicklas, B., Wintel, L.

##### Supervisors: Caudron-Heger, M., Pozzi, M.

------------------------------------------------------------------------

Welcome to our project in which we used mass-spectrometry data of non-synchronized HeLa cells in order to perform a proteome-wide screen to identify RNA-dependent proteins.

**Our dataset ...**\
... contains 4,765 proteins and 150 columns, representing 25 density fractions for each condition, measured in triplicates.\
... was generated using the R-Deep approach.\
... is based on a cell lysate obtained from non-synchronized HeLa cells.

**R-Deep**\
A cell lysate was separated on a 25-step sucrose density gradient via ultracentrifugation. Two conditions were used: a control with intact ribonucleoprotein complexes, and an RNase-treated sample where RNA was degraded, leading to dissociation of RNA–protein interactions. In the control, RNA–protein complexes migrate to specific density fractions. Upon RNase treatment, proteins previously bound to RNA shift to other fractions due to the loss of complex formation. Peptide abundance in each fraction was quantified by mass spectrometry, and differences between conditions were used to identify RNA-dependent proteins - defined by a shift in peak fraction.

**Non-synchronized HeLa cells**\
Ribonucleoprotein (RNP) complexes - composed of RNA and RNA-binding proteins (RBPs) - are dynamic and can vary depending on the cell cycle stage. By using non-synchronized cells in different phases of the cell cycle, we achieve a broader picture and capture more proteins with an RNA dependence.

------------------------------------------------------------------------

## A Glimpse into Potential Results

Our approach enables the identification of RNA-dependent proteins based on their redistribution across the sucrose gradient upon RNase treatment. To classify proteins with respect to RNA-dependency, we defined two categories based on quantitative changes in their distribution profiles:

Selected (RNA-dependent): Proteins were classified as RNA-dependent\
- if they exhibited a center of mass (COM) shift of ≥ 2 fractions,\
- or — in the absence of a COM shift — if they showed a main peak shift of ≥ 3 fractions combined with a Pearson correlation \< 0.7 between control and RNase conditions.

Not selected (RNA-independent): Proteins were considered RNA-independent\
- if they showed no COM shift ≥ 2 and no main peak shift ≥ 3,\
- or if a peak shift occurred without a COM shift, but the profile correlation remained ≥ 0.7.

![Fig. 1: Protein intensity profiles across 25 fractions. DDX21_HUMAN shows a clear shift in its intensity distribution upon RNase treatment (blue), suggesting RNA-dependency. In contrast, SPTN1_HUMAN displays no noticeable change compared to the control condition (red), indicating RNA-independent behavior.](Images/Plot%20of%20SPTN1_HUMAN%20and%20DDX21_HUMAN.png){width="734"}

------------------------------------------------------------------------

### Content of github repository:

***Data_set:***

This document contains our project code. It is divided into the following sections:

> 1.  sub-project 1: HeLa_NS = non-synchronized HeLa cells\
> 2.  sub-project 2: HeLa_Mitosis = HeLa cells synchonized in mitosis\
> 3.  sub-project 3: HeLa_Interphase = HeLa cells synchonized in interphase

> 1.  Load dataset
> 2.  Data cleanup
> 3.  Normalization
> 4.  Identification of local maxima as fit parameters
> 5.  Identification of shoulders
> 6.  Total count of maxima (peaks and shoulders) per protein
> 7.  Identification of proteins with different maxima amount in ctrl vs rnase
> 8.  Add center of mass values
> 9.  Correlation functions
> 10. First criterion for data set purification
> 11. Second criterion for data set purification
> 12. Combining purified data sets
> 13. t-test
> 14. Further visualization/interpretation of purified data
> 15. Evaluation of selection criteria
> 16. Principle Component Analysis
> 17. k-means clustering
> 18. Linear regression analysis

***Poster:***

This PowerPoint contains the poster for our final presentation.

***Data:***

This folder contains the following documents:

> 1.  Excel table of original data: Original mass spectroscopy data with adjusted delimiter
> 2.  RBP2GO Table Non-RBPs: Data base of non RNA-binding proteins
> 3.  RBP2GO Table RBPs: Data base of RNA-binding proteins

***Images:***

This folder contains the plots we used in the poster and the README.

------------------------------------------------------------------------

### Sources:

-   [Sternburg *et al.*, Global Approaches in Studying RNA-Binding Protein Interaction Networks, 2020, Trends in Biochemical Sciences](https://github.com/user-attachments/files/19981693/Sternburg.et.al.Global.Approaches.in.Studying.RNA-Binding.Protein.Interaction.Networks.2020.Trends.in.Biochemical.Sciences.pdf)

-   [Corley *et al.*, How RNA-Binding Proteins Interact with RNA Molecules and Mechanisms, 2020, Molecular Cell](https://github.com/user-attachments/files/19981705/Corley.et.al.How.RNA-Binding.Proteins.Interact.with.RNA.Molecules.and.Mechanisms.2020.Molecular.Cell.pdf)

-   [Gebauer *et al*., RNA-binding proteins in human genetic disease, 2020, Nature Reviews Genetics](https://github.com/user-attachments/files/19981707/Gebauer.et.al.RNA-binding.proteins.in.human.genetic.disease.2020.Nature.Reviews.Genetics.pdf)

-   [Caudron-Herger *et al.*, R-DeeP Proteome-wide and Quantitative Identification of RNA-Dependent Proteins by Density Gradient Ultracentrifugation, 2019, Molecular Cell](https://github.com/user-attachments/files/19981712/Caudron-Herger.et.al.R-DeeP.Proteome-wide.and.Quantitative.Identification.of.RNA-Dependent.Proteins.by.Density.Gradient.Ultracentrifugation.2019.Molecular.Cell.pdf)

-   [Caudron-Herger *et al*., Identification, quantification and bioinformatic analysis of RNA-dependent proteins by RNase treatment and density gradient ultracentrifugation using R-DeeP-2020-Nature Protocols](https://github.com/user-attachments/files/19981715/Caudron-Herger-Identification.quantification.and.bioinformatic.analysis.of.RNA-dependent.proteins.by.RNase.treatment.and.density.gradient.ultracentrifugation.using.R-DeeP-2020-Nature.Protocols_1.pdf)

-   [Rajagopal-Proteome-Wide Identification of RNA-Dependent Proteins in Lung Cancer Cells-2022-Cancers](https://github.com/user-attachments/files/19981723/Rajagopal-Proteome-Wide.Identification.of.RNA-Dependent.Proteins.in.Lung.Cancer.Cells-2022-Cancers.pdf)

-   [Rajagopal *et al.*, An atlas of RNA-dependent proteins in cell division reveals the riboregulation of mitotic protein-protein interactions. Nat. Commun. 16, 2325 (2025)](https://github.com/user-attachments/files/19981728/Rajagopal.et.al.An.atlas.of.RNA-dependent.proteins.in.cell.division.reveals.the.riboregulation.of.mitotic.protein-protein.interactions.Nat.Commun.16.2325.2025.pdf)

-   [Caudron‑Herger *et al.*, RBP2GO: a comprehensive pan-species database on RNA-binding proteins, their interactions and functions, 2020, Nucleic Acids Research](https://doi.org/10.1093/nar/gkaa1040)
