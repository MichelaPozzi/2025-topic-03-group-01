# Proteome-wide Screen for RNA-dependent Proteins of non-synchronized HeLa cells

##### Baureis, J., Ferdin, J., Nicklas, B., Wintel, L.

##### Supervisors: Prof. Caudron-Heger, M., Pozzi, M.

------------------------------------------------------------------------

Welcome to our project in which we used mass-spectrometry data of non-synchronized HeLa cells in order to perform a proteome-wide screen to identify RNA-dependent proteins.

**Our dataset...**\
... contains 4,765 proteins and 150 columns, representing 25 density fractions for each condition, measured in triplicates.\
... was generated using the R-Deep approach.\
... is based on a cell lysate obtained from non-synchronized HeLa cells.

**R-Deep**\
A cell lysate was separated on a 25-step sucrose density gradient via ultracentrifugation. Two conditions were used: a control with intact ribonucleoprotein complexes, and an RNase-treated sample where RNA was degraded, leading to dissociation of RNA–protein interactions. In the control, RNA–protein complexes migrate to specific density fractions. Upon RNase treatment, proteins previously bound to RNA shift to other fractions due to the loss of complex formation. Peptide abundance in each fraction was quantified by mass spectrometry, and differences between conditions were used to identify RNA-dependent proteins - defined by a shift in peak fraction.

**Non-synchronized HeLa cells**\
Ribonucleoprotein (RNP) complexes - composed of RNA and RNA-binding proteins (RBPs) - are dynamic and can vary depending on the cell cycle stage. By using non-synchronized cells in different phases of the cell cycle, we achieve a broader picture and capture more proteins with an RNA dependence.

------------------------------------------------------------------------

## A Glimpse into Potential Results

Our approach enables the identification of RNA-dependent proteins based on their redistribution across the sucrose gradient upon RNase treatment. Specifically, we select proteins that exhibit a shift of at least three fractions in both their main peak fraction and center of mass between the control and RNase-treated conditions. Proteins displaying highly correlated abundance profiles (based on intensity across all 25 fractions) between both conditions are excluded, as such consistent profiles indicate minimal redistribution and are unlikely to be RNA-dependent. The robustness of our selection criteria was evaluated by comparison with external datasets in which RNA dependence has been previously annotated.

![***Fig. 1:** Plot of the NUCL_HUMAN protein showing a significant shift of the RNASE compared to the control.*](images/NUCL_HUMAN_plot.jpg){width="620"}

------------------------------------------------------------------------

### Content of github repository:

***Data_set:***

This document contains our project code. It is divided into the following sections:

> 1.  Load Dataset
> 2.  Data Cleanup
> 3.  Normalization
> 4.  Identification of local maxima as fit parameters
> 5.  Identification of shoulders
> 6.  Total count of maxima (peaks and shoulders) per protein
> 7.  Identification of proteins with different maxima amount in ctrl vs rnase
> 8.  Criteria for selecting rna-dependent proteins
> 9.  Wilcoxon rank-sum test
> 10. Principle Component Analysis
> 11. k-means clustering
> 12. Linear regression analysis

***Poster:***

This PowerPoint contains the poster for our final presentation.

***Excel table of original data:***

This table shows the original mass spectroscopy data we were given with adjusted delimiter.

***Images:***

This folder contains the plots we used in the poster and the README.

------------------------------------------------------------------------

### Sources:

-   [Sternburg *et al.*, Global Approaches in Studying RNA-Binding Protein Interaction Networks, 2020, Trends in Biochemical Sciences.pdf](https://github.com/user-attachments/files/19981693/Sternburg.et.al.Global.Approaches.in.Studying.RNA-Binding.Protein.Interaction.Networks.2020.Trends.in.Biochemical.Sciences.pdf)

-   [Corley *et al.*, How RNA-Binding Proteins Interact with RNA Molecules and Mechanisms, 2020, Molecular Cell.pdf](https://github.com/user-attachments/files/19981705/Corley.et.al.How.RNA-Binding.Proteins.Interact.with.RNA.Molecules.and.Mechanisms.2020.Molecular.Cell.pdf)

-   [Gebauer *et al*., RNA-binding proteins in human genetic disease, 2020, Nature Reviews Genetics.pdf](https://github.com/user-attachments/files/19981707/Gebauer.et.al.RNA-binding.proteins.in.human.genetic.disease.2020.Nature.Reviews.Genetics.pdf)

-   [Caudron-Herger *et al.*, R-DeeP Proteome-wide and Quantitative Identification of RNA-Dependent Proteins by Density Gradient Ultracentrifugation, 2019, Molecular Cell.pdf](https://github.com/user-attachments/files/19981712/Caudron-Herger.et.al.R-DeeP.Proteome-wide.and.Quantitative.Identification.of.RNA-Dependent.Proteins.by.Density.Gradient.Ultracentrifugation.2019.Molecular.Cell.pdf)

-   [Caudron-Herger *et al*., Identification, quantification and bioinformatic analysis of RNA-dependent proteins by RNase treatment and density gradient ultracentrifugation using R-DeeP-2020-Nature Protocols_1.pdf](https://github.com/user-attachments/files/19981715/Caudron-Herger-Identification.quantification.and.bioinformatic.analysis.of.RNA-dependent.proteins.by.RNase.treatment.and.density.gradient.ultracentrifugation.using.R-DeeP-2020-Nature.Protocols_1.pdf)

-   [Rajagopal-Proteome-Wide Identification of RNA-Dependent Proteins in Lung Cancer Cells-2022-Cancers.pdf](https://github.com/user-attachments/files/19981723/Rajagopal-Proteome-Wide.Identification.of.RNA-Dependent.Proteins.in.Lung.Cancer.Cells-2022-Cancers.pdf)

-   [Rajagopal *et al.*, An atlas of RNA-dependent proteins in cell division reveals the riboregulation of mitotic protein-protein interactions. Nat. Commun. 16, 2325 (2025).pdf](https://github.com/user-attachments/files/19981728/Rajagopal.et.al.An.atlas.of.RNA-dependent.proteins.in.cell.division.reveals.the.riboregulation.of.mitotic.protein-protein.interactions.Nat.Commun.16.2325.2025.pdf)
