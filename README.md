# manuscript-ion-calibration
[![DOI](https://zenodo.org/badge/649092539.svg)](https://doi.org/10.1101/2025.05.30.657132)

This repo contains most of the input files and the basic analyses used in the manuscript "Evaluation of an Orbitrap Astral Zoom mass spectrometer prototype for quantitative proteomics - beyond identification lists", which is currently located on bioRxiv under the DOI [10.1101/2025.05.30.657132](https://doi.org/10.1101/2025.05.30.657132). Any files not located here are freely and openly accessible on the [Ion calibration manuscript page of PanoramaWeb](https://panoramaweb.org/MacCoss_ModifiedOrbitrapAstralZoom.url).

Data was exported using the Skyline document grid. Many of the Skyline documents were created using pivot tables. Analyses were perfomed using Skyline and R Markdown files.

### Repository Layout

* **bin:** Contains scripts used to generate figures and preprocessing

* **data:** Contains csv, tsv, mzML, raw files used as input and output for the scripts in the bin folder. 
  
* **figures:** Contains the figure outputs from the scripts


$~$

## Scripts

Scripts are located in the **bin** folder.

* **HeLa_IsoWindow_Figs2-5_FigS1-2_S6-7_TableS1-2.Rmd:** R markdown that generates Figures 2: Acquisition Rates and cycle times, Figure 3: Proteins and precursor identifications, Figure 4: Coefficient of variation (CV) plots, and Figure 5: Ion counting. It also includes Figure S1: ion injection time, Figure S2: Peptides and proteins gained from higher input, Figure S6: Apex total spectrum ion counts, and Figure S7: LC peak peptide ion count log2 ratio as a density distribution. We also included Supplementary Tables 1 and 2, which are the protein and precursor values for Figure 3. All comparisons were between the Orbitrap Astral and the Orbitrap Astral Zoom (sometimes labeled as Actis). 

* **EV_MMCC_Fig6_FigS8.Rmd:** R markdown that generates Figure 6: Human extracellular vesicle matrix-matched calibration curve assessing quantitative accuracy. This code also includes Figure S8: Protein/Precursor IDs and CVs, and it also includes the protein ion abundance ranked plot. All comparisons were between the Orbitrap Astral and the Orbitrap Astral Zoom (sometimes labeled as Actis).

* **Ion_Calibration_Table1_FigS3-5.Rmd:** R markdown that generates the ion calibration using Glu[1]-Fibrinopeptide B for various Thermo Scientific mass spectrometers, designated as Table 1 in the manuscript. Figure S3 is the fragmentation pattern for the three compounds (Glu[1]-Fibrinopeptide B, Flexmix with Ultramark 1122, and Flexmix with Ultramark 1822) that we tested for ion caliibration. Figure S4 demonstrates the different parts of the ion calibration. Figure S5 shows the linear regression for the three compounds with the Orbitrap Astral and the Orbitrap Astral Zoom. **Quick note: the glu1-fib-Astral-Astral.mzML.zip and glu1-fib-Actis-Astral.mzML.zip are ZIPPED files because of the file size limitations on Gitub! Remember to unzip them before running the ion calibration code. 

## Ion Calibration (misc. notes)

Since the ion calibration calculates ratio between two ion intensity peaks, we wanted to assess how that would change with using different reference ions. The resulting csv output from running the ion calibration will give you the R^2, slope (or the alpha correction factor), y-intercept (non-poisson noise), the standard error (SE) for the linear regression, and compound _m/z_ for all fragments used. From our experience, the use of different fragments as the reference did not change the calculated slope or alpha by very much, so we ended up only reporting the alpha value from a single reference ion. 

If there are any questions or comments, please feel free to contact maccoss@uw.edu or chrhsu@uw.edu.



