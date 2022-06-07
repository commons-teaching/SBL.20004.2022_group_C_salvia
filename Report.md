# Metabolomics analysis report
SBL.20004 

18.05.2022

----
Group C
-  Christelle Brumann
-  Gloria Lampo
-  Alex Leytens
----


## Introduction

The metabolome is the collection of molecules produced by biological processes within a cell. The set of experimental and analytical techniques carried out to profiling these products is called Metabolomics.

Plants have always played a fundamental role in everyday life. With the advent of traditional medicine and scientific development as well as the need for renewable systems, metabolic analysis of these organisms has become essential.
Being sessile organisms, plants have developed over the years different and specific metabolism to counteract abiotics and biotic stress. This strong interdependence with their environment has resulted in the definition of metabolomic identities that can be shared between different phylums within similar ecosystems.
This is why we are interested in investigating whether the identification of the metabolic identity of plants can be used as an alternative technique to genetic sequencing to develop phylogenetic links.
For this reason, the choice of plants to be analysed is based on two criteria:

- Plants samples must belong to a single plant family, whose genetic sequence and correlation has already been established and described in the literature.
- This family must have a large number of representatives in the harvest region.

Therefore we performed a MS-metabolome analysis of several Salvia strains cultivated in the botanical garden of the University of Fribourg. The aim is to reconstruct a phylogenetic tree based on the metabolome’s analysis and compare it to databases and similar studies. Data collected will contribute to the molecular cartography of the botanical garden. This project is led by Dr. Emmanuel Defossez and Dr. Pierre-Marie Allard [^1]. 

Among the genus Salvia from the lamiaceae family, we collected 14 plants of 11 different species in the 15 section of the botanical garden. They represent 3 subgenus (Glutinaria, Salvia and Sclarea) of the 11 commonly accepted (1. Audibertia, 2. Calosphace, 3. Dorystaechas, 4. Glutinaria, 5. Heterosphace, 6. Meriandra, 7. Peroskia, 8. Rosmarinus, 9. Salvia, 10. Sclarea, 11. Zhumeria). Heterosphae is not clearly defined as a subgenus but its heritage differs as a result of geographical events. A genomic study using next-generation sequencing on which we base our comparison, defined Heterosphae as a subgenus [^2]. To simplify and do easier comparisons we will use the same nomenclature. 

**Salvia phylogeny based on nuclear gene study**

![Salvia_phylogeny based on nuclear gene study](https://user-images.githubusercontent.com/103578333/172018211-3c37814d-f1e2-4c87-bcb9-5ed3ab0a7255.jpg)

Mass spectrometry is a powerful analytical system defined by three components: 

- Ion source: Convert the analytes into ions in the gaseous state.
- Mass analyzer: It separates the different ions according to their mass charge ratio (m/z).
- Detector: It defines for each individual ion the corresponding abundance.

The output is an informative spectro of ion peaks, which associate an intensity value of relative abundance to the corresponding ion molecule.
Depending on the type of omics-study, the sample preparation may vary, while still keeping some common features. Due to the metabolomic cell complexity, a fractionation of the sample before loading is necessary. For this reason, different chromatography techniques can be performed, each specific to the scientific question to be answered. In our case, HPLC was used with a polar stationary phase and elution with apolar solvent, the non-polarity of which is gradually increased over time.

The dry lab has the function to organize, sort and annotate data. Depend on the software used, raw files has to be convert in open source format but this modification can introduce errors.

The data treatment required 10 following steps:
1. Data import
2. MS peak detection
3. Chromatogram building
4. Chromatogram deconvolution
5. Isotope grouping
6. Feature alignment
7. MS row filter
8. Isotope filter (min.n isotope peaks) and normalisation (TIC or Standard)
9. Gap filling (reanalyse raw data)
10. Feature csv export

Based on the clean data it's then possible to identify moleculs with database comparison using tools such as GNPS (Global Natural Products Social Molecular Networking).


## Material & Methods


### Sample collection

The Salvias were harvest in the 15 section of the botanical garden the 13th April 2022 at 15.8°C [^3]. We then assume that plants have been subjected to identical stress reducing the variability between samples. The leaves of each plant were harvest and directly stored in liquide nitrogen to prevent any biochemical-stress reaction that can lead to misleading results. After 24h of lyophilization, the samples were stored at -80°C.
Plants observations geo-localisation are avalable on the INaturalist website (DBGI project) [^4].

[Salvia entries of the DBGI project on inaturalist](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/GroupC%20-%20Salvia%20-%20DBGI%20project%20on%20Inaturalist.csv)

##### 1.  Glutinaria:

![Glutinaria](https://user-images.githubusercontent.com/103578333/169149050-c9872802-53aa-484a-8532-9ade79ffd77e.png)


##### 2. Heterosphace:

![Heterosphace](https://user-images.githubusercontent.com/103578333/172025317-1d2961d5-25dd-4a08-bbbc-8d0d3f45d70e.png)


##### 3. Salvia:     

![Salvia](https://user-images.githubusercontent.com/103578333/172025107-53eb0a63-1289-47c0-a074-af76881859c2.png)


##### 4. Sclarea:   

![Sclarea](https://user-images.githubusercontent.com/103578333/169152368-3339366b-4021-40a1-8408-57b84b92f232.png)

##### 5. Non defined in Network n°1 (without filled gaps) but assigned in Salvia clade in Network n°2 (filled gaps)

![Salvia Candelabrum](https://user-images.githubusercontent.com/103578333/169149876-5933a88f-a539-476c-aefc-121d39db55ca.png)


### Sample preparation for qualitative and quantitative analysis

50 g  ± 0.5 g of lyophilized plant material was extracted with 170 µL MeOH/H2O/formic acid (80:20:0.1) with a Mixer mill MM 400 (Manufacturer Retsch) 30 Hz for 3 min at RT°. The supernatant was collected in to vials and stored at -80° prior MS-loading.


### Liquid chromatogrphy-Mass spectrometry Analysis

Chromatographic separation was performed on a VANQUISH HORIZON UPLC system (Thermo Scientific, Bremen, Germany) interfaced to a Q-Exactive Plus mass spectrometer (Thermo Scientific, Bremen, Germany), using a heated electrospray ionization (HESI-II) source. Thermo Scientific Xcalibur 3.1 software was used for instrument control. The LC conditions were as follows: column, Waters BEH C18 100 × 2.1 mm, 1.7 μm; mobile phase, (A) water with 0.1% formic acid; (B) acetonitrile with 0.1% formic acid; flow rate, 600 μl·min−1; injection volume, 6 μl; gradient, linear gradient of 5–100% B over 8 min and isocratic at 100% B for 1 min. The optimized HESI-II parameters were as follows: source voltage, 3.5 kV (pos); sheath gas flow rate (N2), 55 units; auxiliary gas flow rate, 15 units; spare gas flow rate, 3.0; capillary temperature, 350.00°C, S-Lens RF Level, 45. The mass analyzer was calibrated using a mixture of caffeine, methionine–arginine–phenylalanine–alanine–acetate (MRFA), sodium dodecyl sulfate, sodium taurocholate, and Ultramark 1,621 in an acetonitrile/methanol/water solution containing 1% formic acid by direct injection. The data-dependent MS/MS events were performed on the three most intense ions detected in full scan MS (Top3 experiment). The MS/MS isolation window width was 1 Da, and the stepped normalized collision energy (NCE) was set to 15, 30 and 45 units. In data-dependent MS/MS experiments, full scans were acquired at a resolution of 35,000 FWHM (at m/z 200) and MS/MS scans at 17,500 FWHM both with an automatically determined maximum injection time. After being acquired in a MS/MS scan, precursor ions were placed in a dynamic exclusion list for 2.0 s.


### Data analysis

The [Proteowizard ](https://proteowizard.sourceforge.io/) software was used to convert data raw files in mzML extension file and [MzMine 2.53](https://github.com/mzmine/mzmine2/releases) software was used to preprocess the raw HPLC-QORB-MS data for filtering peaks and get rid off contamination such as plastic coming from laboratory tools. After centroiding and isotopes groupping of the picks, GNPS was used to developpe a feature networking (advance analysis tools) to quantify molecules and reduced molecule redundancy.

The following GNPS setting were used: **Molecular Networking and Spectral Library Search**

A molecular network was created with the Feature-Based Molecular Networking (FBMN) workflow (Nothias L-F, Petras D, Schmid R et al. Nature Methods 17, 905–908 (2020)) on GNPS (https://gnps.ucsd.edu, Wang M et al. Nat. Biotech. 2016). The mass spectrometry data were first processed with MZMINE2 (cite accordingly, see below in the Citations section) and the results were exported to GNPS for FBMN analysis. The precursor ion mass tolerance was set to 0.02 Da and the MS/MS fragment ion tolerance to 0.02 Da. A molecular network was then created where edges were filtered to have a cosine score above 0.7 and more than 6 matched peaks. Further, edges between two nodes were kept in the network if and only if each of the nodes appeared in each others respective top 10 most similar nodes. Finally, the maximum size of a molecular family was set to 100, and the lowest scoring edges were removed from molecular families until the molecular family size was below this threshold. The spectra in the network were then searched against GNPS spectral libraries (Cite Wang M, et al. Nature Biotech. 2016 and Horai, H. et al. J. Mass Spectrom. 45, 703-714 2010). The library spectra were filtered in the same manner as the input data. All matches kept between network spectra and library spectra were required to have a score above 0.7 and at least 6 matched peaks. The DEREPLICATOR was used to annotate MS/MS spectra (Mohimani, H. et al. Nat. Commun. 9, 4035 (2018)). The molecular networks were visualised using Cytoscape software (Shannon, P. et al. Genome Res. 13, 2498-2504 (2003)).

#### Data Deposition and Job Accessibility
The mass spectrometry data were deposited on public repository (provide the deposition accession number), such as MassIVE or MetaboLights. The molecular networking job can be publicly accessed [here](https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=d9eb8151a9f5459dad892bb449ccc95a) (we recommend sharing this link in your manuscript).

1. [group_C_metadata.txt](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/GroupC_Metadata.txt) 
2. [group_C_quant.csv](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/group_C_quant.csv) 
3. [group_C.mgf](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/group_C.mgf) 

The output files were visualise using [cytoscape](https://cytoscape.org/) software.

## Results

### MS

The barplot below shows the effects of data treatment with MZmind on the number of peaks. 

![MZmind_treated_data](https://user-images.githubusercontent.com/103578333/172430700-65edce29-a4c9-4c0b-bd42-0b013745d736.png)

### Molecular Network
Molecular networks generated by GNPS were visualized with cytoscape. Node labels correspond to parent ion masses, nodes are represented as pie charts depicting the intensities of each feature in the different clades studied. Nodes with red borders indicate features annotated in GNPS. If labels are present on edges, labels represent mass differences.

Molecular network performed by GNPS:
- [GNPS job](https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=10d92d779bd741d09af035b2e89d7bad)

Link to the GNPS identification table:
- [Table list job](https://gnps.ucsd.edu/ProteoSAFe/result.jsp?task=10d92d779bd741d09af035b2e89d7bad&view=view_all_annotations_DB)

![Network](https://user-images.githubusercontent.com/103578179/172425883-1ce00612-1896-4d17-9f14-bdea81af399e.png)
![Legend complete](https://user-images.githubusercontent.com/103578333/172071591-e52f83c3-e529-486c-b62c-b02fa89e90bf.png)
![Legend of molecular Network](https://user-images.githubusercontent.com/103578333/172025698-53ab47b8-47dd-4c04-b0f4-ea09f2f9ed78.png)

The two subnetworks correspond to features mostly found amongst the Salvia clade, which also appeared to cluster well in the hierchical clustering. 

At left, the 1<sup>st</sup> subnetwork comprises 2 different annotated compounds, both correspnding to triterpens namely Sumaresinolic acid and Asiatic acid. Although other nodes from the graph were not annotated, the small differences in parent masses could suggest that this network comprises of other triterpens with a minimum of 30 carbon atoms.

At the right side, the 2<sup>nd</sup>  cluster belongs to sumaresinolic acid. It seems to be interesting because this compound is positionned in the hierarchical clustering at the position of Salvia clustering. 

![Carnosol_Cluster and Terpene Cluster](https://user-images.githubusercontent.com/103578333/172474393-12c6d3c0-8411-4530-8618-0b837da44d12.png)

![Carnosol_ inside_Salvia](https://user-images.githubusercontent.com/103578333/172431088-6b0ab448-54d6-4db8-8828-43766c45f9a5.png)

To do this piechart, we have extracted data table from cytoscape and looked precisely at a interesting compound such as Carnosol inside Salvia subgenus. We observed that we get several hits for same compound_name because several features are associated to one compound_name for each plant. So we take into account the higher one and we compare each plants inside subgenus Salvia. We can conclude that Carnosol is more specific to Salvia officinalis than to Salvia subgenus. 

### Samples clustering based on all features:
Gapfilled data was used to perform hierchical clustering. Generated dendrograms were compared to the phylogenetic analyses reported in the already mentionned study [2].

![Image Hierchical clustering](https://user-images.githubusercontent.com/103578179/172424154-a70e4c41-2713-49a7-bc7c-ada24e2a32fe.png)

The PCA is another way to analysis the distance and relation between subgenus. Here we can see that Salvia and Sclarea are separated from each other. Compared to the study it's suprizing but we have not enougth evidence to explain it.  

![PCA](https://user-images.githubusercontent.com/103578179/172426464-65f8f503-32cd-4a2d-a1f1-bfbad107a09b.png)


## Conclusion

The analysis of the metabolom was difficult because a few features were linked to a compound (1666 features in total, more or less 430 identified and named based on GNPS database, and more or less 215 features depend on the plant, after remove duplicates compound name associated). We can see similarities between our work and the study used as comparison but we cannot pointed out specific clusters explaining the phylogeny. 

# References

[^1]: Kozlowski Gregor, Defossez Emmanuel, & Allard Pierre-Marie. (2021). Molecular cartography of the Botanical Garden of the University of Fribourg (1.1). Zenodo. https://doi.org/10.5281/zenodo.5726749

[^2]: Rose Jeffrey P., Kriebel Ricardo, Kahan Larissa, DiNicola Alexa, GonzÃ¡lez-Gallegos JesÃºs G., Celep Ferhat, Lemmon Emily M., Lemmon Alan R., Sytsma Kenneth J. & Drew Bryan T. (2021). Sage Insights Into the Phylogeny of Salvia: Dealing With Sources of Discordance Within and Across Genomes, Frontiers in Plant Science, Vol..12	
https://doi.org/10.3389/fpls.2021.767478   

[^3]: Etat de Fribourg, Energy, agriculture et environnement: Degrés-jours et température moyenne, relevés hebdomadaires, website visited on 27 April 2022 
https://www.fr.ch/energie-agriculture-et-environnement/energie/degres-jours-et-temperature-moyenne-releves-hebdomadaires

[^4]: INaturalist, website visited on 13 April 2022
DBGI project https://www.inaturalist.org/projects/digital-botanical-gardens-initiative
