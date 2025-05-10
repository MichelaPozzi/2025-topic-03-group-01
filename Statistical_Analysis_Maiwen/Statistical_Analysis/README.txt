#### README.txt ####

This material contains the instructions for the installation and running of the mass spectrometry statistical analysis pipeline associated with the R-DeeP protocol.
The pipeline provided as "MS_Statistical_Analysis.R" in the Supplementary Data is written in "R" programmation language and can be run in RStudio.
Before using the pipeline, we recommend to install RStudio on the computer.


#### 1 - System requirements ####

According to the RStudio webpage, RStudio is available in an open source (as well as commercial) edition and runs on standard operating systems (Windows, Mac, and Linux).
See the "Installation" section below for detailled instructions on how to instal RStudio and run the pipeline.


#### 2 - Installation ####

1) RStudio requires R 2.11.1 (or higher) to run. R is a free software environment for statistical computing and graphics. If needed, please download R from the R project webpage: https://www.r-project.org  according to your operating system and follow the instructions to install R on your computer. In principle, R can be installed executing the installer (double click on it). Note that it will require password or login of an account with administrator privileges. The installation can be customized, but the default is suitable for most users. In case of difficulties, more help can be obtained from the operating system specific FAQ and HOWTO documents at https://cran.r-project.org/faqs.html.

2) Download the open source edition of RStudio from the download wegpage https://www.rstudio.com/products/rstudio/download/ according to your operating system.

3) Following download, execute the RStudio installer. A troubleshooting guide is available at https://support.rstudio.com/hc/en-us/articles/200488498-Troubleshooting-Guide-Using-RStudio.

4) We experienced error message at the start of RStudio due to language settings. If it is the case, refer to the support page: https://support.rstudio.com/hc/en-us/articles/200532197-Character-Encoding

5) The installation of both R and RStudio should not take longer than 30 min.


#### 3 - Use of the pipeline on the test dataset (Demo) ####

6) Once RStudio is running, it includes a console, a syntax-highlighting editor from which the code can be directly executed, and additional tools to access the workspace (files), the environment (new variables defined in the pipeline), but also windows to view plots, to manage packages (set of functions to be used) and a help tool.

7) Create a specific folder dedicated to the analysis of the mass spectrometry dataset.

8) Copy the pipeline "MS_Statistical_Analysis.R", and the test dataset "Mass_Spec_RawData_Sample.csv" in that folder. Create a new folder entitled "Examples" in that folder and copy the example files "MS_Analysis_Shifts.csv", "HNRPU_HUMAN_FIT.pdf" and "HNRPU_HUMAN_ALL.pdf" in the "Examples" folder.

9) Using the "File" window in RStudio (you will find it on the bottom right part of the RStudio programm), navigate to the folder created Step 7 of this file).

10) Click on the Menu "More" from the "File" window and select "Set As Working Directory". the line "setwd("....") should appear in the "Console" window (bottom left part).

11) In the "File" window, click on the pipeline file entitled "MS_Statistical_Analysis.R" to open the pipeline in the editor window (Upper left part, above the "Console").

12) R programming is simplified by a great number of ready-to-use functions, which are accessible via so-called "packages". Upon startup, a set of packages are loaded per defaults: "base", "datasets","utils","grDevices","graphics","stats" and "methods". You can verify that these packages are activated by looking into the "Packages" window, next to the "Files" window. The packages will appear ticked in the list. Additional packages can be installed via the "Installed" button on the top left corner of the Packages window.

13) To run the graphical functions defined at the end of the pipeline (see Step 17 of this file), it is necessary to intall the following packages:
"raster", "sp", graphics", "grid", "ggplot2", "gridExtra" and "lattice". The packages are then automatically loaded/activated in the pipeline.

14) In the pipeline file, the green lines (starting with #) are only comments. The pipeline can be executed either step-by-step by executing each line one after each other (copy and paste in the "Console" or click on the green "Run" arrow at the top right corner of the editor window); or by copying and pasting the whole pipeline in the "Console" (alternatively, you can also click on the "Source" button at the top right corner of the editor window). A set of selected lines of the pipeline can be automatically executed by using the combination "ctrl + enter" keys.

15) The pipeline produces at the end a CSV file, which is exported to the working directory as defined in step 7 of this file. This analysis summary table is named "MS_Analysis_Shifts.csv". The table is also accessible in RStudio under the variable name "MS_Analysis_table" and can bu further exploited as needed. You can compare the summary table exported by the pipeline with the export table provided in the Supplementary Data under the name "MS_Analysis_Shifts.csv".

16) The expected running time for the test dataset is about 5 to 10 min, depending on the computer processor.


#### 4 - Graphics ####

17) Along with the pipeline, two graphical functions are available to represent the mass spectrometry data on an individual protein basis.

18) The first function is called "curves_plot" and can be used as follow "curves_plot(pos)" where "pos" is a protein Entry name (UniProt). For example: curves_plot("HNRPU_HUMAN"). The function "curves_plot" returns the graphical representation of the mean control and RNase-treated samples including the Gaussian fits, where the x-axis is the fraction number and the y-axis the normalized protein amount. An example of this plot is provided in the Supplementary Data under the name "HNRPU_HUMAN_FIT.pdf". 

19) The second function is called "curves_all" and can be used as follow "curves_all(pos)" where "pos" is a protein Entry name (UniProt). For example: curves_all("HNRPU_HUMAN"). The function "curves_all" returns the graphical representation of each control and RNase-treated replicate, where the x-axis is the fraction number and the y-axis the normalized protein amount. An example of this plot is provided in the Supplementary Data under the name "HNRPU_HUMAN_ALL.pdf".

20) In RStudio, the plots can be exported to the working directory as an image or PDF file using the Menu "Export" in the "File" window.
 

#### 5 - Database ####

21) A searchable R-DeeP database for RNA-dependent proteins is available online for the analysis of the RNA-dependent proteins in HeLa cells at http://R-DeeP.dkfz.de.


