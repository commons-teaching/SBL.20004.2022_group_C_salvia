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

Among the genus Salvia from the lamiaceae family, we collected 14 plants of 11 different species in the 15 section of the botanical garden. They represent 3 clades subgenus (Glutinaria, Salvia and Sclarea) of the 11 commonly accepted (1. Audibertia, 2. Calosphace, 3. Dorystaechas, 4. Glutinaria, 5. Heterosphace, 6. Meriandra, 7. Peroskia, 8. Rosmarinus, 9. Salvia, 10. Sclarea, 11. Zhumeria). Heterosphae is not clearly defined as a clade but its heritage differs as a result of geographical events. A genomic study using next-generation sequencing on which we base our comparison, defined Heterosphae as a clade [^2]. To simplify and do easier comparisons we will use the same nomenclature. 

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

![Clade Glutinaria](https://user-images.githubusercontent.com/103578333/169149050-c9872802-53aa-484a-8532-9ade79ffd77e.png)


##### 2. Heterosphace:

![Clade Heterosphace](https://user-images.githubusercontent.com/103578333/169702091-f4a67aa5-dca6-4ab3-b42a-f43e68c9739a.png)


##### 3. Salvia:     

![Clade Salvia](https://user-images.githubusercontent.com/103578333/169148133-80c1a659-db9d-4324-b917-2b1bf742079c.png)


##### 4. Sclarea:   

![Clade Sclarea](https://user-images.githubusercontent.com/103578333/169152368-3339366b-4021-40a1-8408-57b84b92f232.png)

##### 5. Non defined

![Salvia Candelabrum](https://user-images.githubusercontent.com/103578333/169149876-5933a88f-a539-476c-aefc-121d39db55ca.png)


### Sample preparation for qualitative and quantitative analysis

50 g  ± 0.5 g of lyophilized plant material was extracted with 170 µL MeOH/H2O/formic acid (80:20:0.1) in a (------------) 30 Hz at RT° for 3min. The supernatant was collected in to vials and stored at -80° prior MS-loading.


### Liquid chromatogrphy-Mass spectrometry Analysis

High performance liquid chromatography quadrupole orbitrap mass spectrometry (HPLC-QORB-MS) estimation of metabolite contents was carried out on a Thermo Ultimate 3000 RS (Thermo Fischer Scientific, Waltham, MA, USA)coupled to a Thermo (----) Qorbitrap mass spectrometer. Separations were performed on a C18 column, , with mobile phase A consisting of 0.1% (v/v) FA in water and mobile phase B consisting of 0.1% (v/v) FA in acetonitrile (MUST BE CHECKED). . The samples (2 µL) were injected, and a linear gradient from 15% to 70% phase B in phase A was used for 8 min to separate all main compounds. The flow rate was 0.3 mL/min, and the column was held at 30 ◦C. Mass spectra were acquired in positive-ion mode over a mass range from m/z 100 to 1500 with 5 Hz frequency Ultrapure nitrogen was used as drying and nebulizer gas and argon was used as collision gas. The collision energy was set automatically from 15 to 75 eV, depending on the m/z of the fragmented ion. Operating parameters of the ESI ion source were as follows: capillary voltage 3 kV, dry gas flow 6 L/min, dry gas temperature 200 ◦C, nebulizer pressure 0.7 bar, collision radio frequency 700.0 V, transfer time 100.0 µs, and pre pulse storage 7.0 µs.


### Data analysis

The [Proteowizard ](https://proteowizard.sourceforge.io/) software was used to convert data raw files in mzML extension file and [MzMine 2.53](https://github.com/mzmine/mzmine2/releases) software was used to preprocess the raw HPLC-QORB-MS data for filtering peaks and get rid off contamination such as plastic coming from laboratory tools. After centroiding and isotopes groupping of the picks, GNPS was used to developpe a feature networking (advance analysis tools) to quantify molecules and reduced molecule redundancy.
The following GNPS setting were used:

#### Molecular Networking and Spectral Library Search
A molecular network was created with the Feature-Based Molecular Networking (FBMN) workflow (Nothias L-F, Petras D, Schmid R et al. Nature Methods 17, 905–908 (2020)) on GNPS (https://gnps.ucsd.edu, Wang M et al. Nat. Biotech. 2016). The mass spectrometry data were first processed with MZMINE2 (cite accordingly, see below in the Citations section) and the results were exported to GNPS for FBMN analysis. The precursor ion mass tolerance was set to 0.02 Da and the MS/MS fragment ion tolerance to 0.02 Da. A molecular network was then created where edges were filtered to have a cosine score above 0.7 and more than 6 matched peaks. Further, edges between two nodes were kept in the network if and only if each of the nodes appeared in each others respective top 10 most similar nodes. Finally, the maximum size of a molecular family was set to 100, and the lowest scoring edges were removed from molecular families until the molecular family size was below this threshold. The spectra in the network were then searched against GNPS spectral libraries (Cite Wang M, et al. Nature Biotech. 2016 and Horai, H. et al. J. Mass Spectrom. 45, 703-714 2010). The library spectra were filtered in the same manner as the input data. All matches kept between network spectra and library spectra were required to have a score above 0.7 and at least 6 matched peaks. The DEREPLICATOR was used to annotate MS/MS spectra (Mohimani, H. et al. Nat. Commun. 9, 4035 (2018)). The molecular networks were visualised using Cytoscape software (Shannon, P. et al. Genome Res. 13, 2498-2504 (2003)).

#### Data Deposition and Job Accessibility
The mass spectrometry data were deposited on public repository (provide the deposition accession number), such as MassIVE or MetaboLights. The molecular networking job can be publicly accessed [here](https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=d9eb8151a9f5459dad892bb449ccc95a) (we recommend sharing this link in your manuscript).

1. [group_C_metadata.txt](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/GroupC_Metadata.txt) 
2. [group_C_quant.csv](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/group_C_quant.csv) 
3. [group_C.mgf](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/group_C.mgf) 

The output files were visualise using [cytoscape](https://cytoscape.org/) software.



## Results


### MS1

How many features could you clean in your final peak list ?
A link to the final feature list (uploaded to github).

### Molecular Network

Screenshots of your molecular network and of some clusters of interest.
The molecular network is link to the [GNPS job](https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=d9eb8151a9f5459dad892bb449ccc95a).

Link to the GNPS identification table.


![Global_network](https://user-images.githubusercontent.com/103578333/169245706-b03ae6b5-0934-4586-b0e0-d0599b9a10bb.png)

![Legend complete](https://user-images.githubusercontent.com/103578333/170486273-529d4e4a-ade3-4f0f-875d-5882dd685eb1.png)
![Legend of molecular Network](https://user-images.githubusercontent.com/103578333/170880503-da5fd5d0-1d01-4847-b7eb-207252299877.png)


Out of 1551 measured peaks 392 identifications have been produced by GNPS.

The compound identified in abundance in each clade is caffeinic acid. It's an important intermediate in lignin biosynthesis. Another one present in abundance is the rosmarinic acid that is a caffeinic acid ester and its supposed function is the defense of the plants [^5]. 

Camphora compound were identify only in the Salvia clade and in the plant salvia candelabrum which wasn't clade defined. This substance is known for its therapeutic effect and usually extracted from leafs of Salvia officinalis which is part of salvia clade [^6]. This evidence suggested a relationship between this plant and salvia clade. 


## Conclusion

Some conclusion that you could get out of this preliminary study.

# References

[^1]: Kozlowski Gregor, Defossez Emmanuel, & Allard Pierre-Marie. (2021). Molecular cartography of the Botanical Garden of the University of Fribourg (1.1). Zenodo. https://doi.org/10.5281/zenodo.5726749

[^2]: Rose Jeffrey P., Kriebel Ricardo, Kahan Larissa, DiNicola Alexa, GonzÃ¡lez-Gallegos JesÃºs G., Celep Ferhat, Lemmon Emily M., Lemmon Alan R., Sytsma Kenneth J. & Drew Bryan T. (2021). Sage Insights Into the Phylogeny of Salvia: Dealing With Sources of Discordance Within and Across Genomes, Frontiers in Plant Science, Vol..12	
https://doi.org/10.3389/fpls.2021.767478   

[^3]: Etat de Fribourg, Energy, agriculture et environnement: Degrés-jours et température moyenne, relevés hebdomadaires, website visited on 27 April 2022 
https://www.fr.ch/energie-agriculture-et-environnement/energie/degres-jours-et-temperature-moyenne-releves-hebdomadaires

[^4]: INaturalist, website visited on 13 April 2022
DBGI project https://www.inaturalist.org/projects/digital-botanical-gardens-initiative

[^5]: Petersen M, Abdullah Y, Benner J, Eberle D, Gehlen K, Hücherig S, Janiak V, Kim KH, Sander M, Weitzel C, Wolters S. Evolution of rosmarinic acid biosynthesis. Phytochemistry. 2009 Oct-Nov;70(15-16):1663-79. doi: 10.1016/j.phytochem.2009.05.010. Epub 2009 Jun 25. PMID: 19560175.

[^6]: Croteau R, Felton M, Karp F, Kjonaas R. Relationship of Camphor Biosynthesis to Leaf Development in Sage (Salvia officinalis). Plant Physiol. 1981 Apr;67(4):820-4. doi: 10.1104/pp.67.4.820. PMID: 16661761; PMCID: PMC425779.

[]Shouchuang Wang, Saleh Alseekh, Alisdair R. Fernie, Jie Luo. (2019). The Structure and Function of Major Plant Metabolite Modifications, Molecular Plant,  vol 12, issue 7, P899-919, https://doi.org/10.1016/j.molp.2019.06.001

[]: Jorge Tiago F., Mata Ana T. & António Carla. (2016). Mass spectrometry as a quantitative tool in plant metabolomics, Phil. Trans. R. Soc. A.3742015037020150370
http://doi.org/10.1098/rsta.2015.0370

[]: Malviya, Rishabha & Bansal, Vvipin & Pal, Om & Sharma, Pramod. (2010). High performance liquid chromatography: A short review. Journal of Global Pharma Technology. 2. 22-26. 

[]: Walther TC, Mann M. Mass spectrometry-based proteomics in cell biology. J Cell Biol. 2010 Aug 23;190(4):491-500. 
https://doi.org/10.1083/jcb.201004052

[]: Metabolomic data https://drive.switch.ch/index.php/s/U6Vezrq5mDVzSld

[]: Filezilla https://filezilla-project.org/download.php?type=client

[]: GNPS https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp


Note that you can make a footnot like this [^1]

[^1]: Ref X
