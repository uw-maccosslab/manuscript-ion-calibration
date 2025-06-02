# manuscript-ion-calibration
[![DOI](https://zenodo.org/badge/649092539.svg)](https://doi.org/10.1101/2025.05.30.657132)

This repo contains most of the input files and the basic analyses used in the manuscript "Evaluation of an Orbitrap Astral Zoom mass spectrometer prototype for quantitative proteomics - beyond identification lists", which is currently located on bioRxiv under the DOI [10.1101/2025.05.30.657132](https://doi.org/10.1101/2025.05.30.657132). Any files not located here are freely and openly accessible on the [Ion calibration manuscript page of PanoramaWeb](https://panoramaweb.org/MacCoss_ModifiedOrbitrapAstralZoom.url).

Data was exported using the Skyline document grid. Many of the Skyline documents were created using pivot tables. Analyses were perfomed using Skyline and R Markdown files.

### Repository Layout

* **bin:** Contains scripts used to generate figures and preprocessing

* **data:** Contains csv, tsv, mzML, raw files used as input and output for the scripts in the bin folder. 
  
* **figures:** Contains the figure outputs from the scripts

Just a 

$~$

## Scripts

Scripts are located in the **bin** folder.

* **HeLa_IsoWindow_Figs2-5_FigS1_S4-5_TableS1-2.Rmd:** R markdown that generates Figures 2: Acquisition Rates and cycle times, Figure 3: Proteins and precursor identifications, Figure 4: Coefficient of variation (CV) plots, and Figure 5: Ion counting. It also includes Figure S1: ion injection time, Figure S4: Apex total spectrum ion counts, and Figure S5: LC peak peptide ion count log2 ratio as a density distribution. We also included Supplementary Tables 1 and 2, which are the protein and precursor values for Figure 3. All comparisons were between the Orbitrap Astral and the Orbitrap Astral Zoom (sometimes labeled as Actis).

* **EV_MMCC_Fig6_FigS6.Rmd:** R markdown that generates Figure 6: Human extracellular vesicle matrix-matched calibration curve assessing quantitative accuracy. This code also includes Figure S6: Protein/Precursor IDs and CVs, and it also includes the protein ion abundance ranked plot. All comparisons were between the Orbitrap Astral and the Orbitrap Astral Zoom (sometimes labeled as Actis).

* **Ion_Calibration_Table1_FigS2-3.Rmd:** R markdown that generates the ion calibration using Glu[1]-Fibrinopeptide B for various Thermo Scientific mass spectrometers, designated as Table 1 in the manuscript. Figure S2 is the fragmentation pattern for the three compounds (Glu[1]-Fibrinopeptide B, Flexmix with Ultramark 1122, and Flexmix with Ultramark 1822) that we tested for ion caliibration. Figure S3 shows the linear regression for the three compounds with the Orbitrap Astral and the Orbitrap Astral Zoom.



