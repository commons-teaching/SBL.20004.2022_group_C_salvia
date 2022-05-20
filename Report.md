# Metabolomics analysis report
SBL.20004 

18.05.2022

----
Group C
-  Christelle Brumann
-  Gloria Lampo
----


## Introduction


Some words on the backgorund of your projects.
Which plants did you select and why ?


The aim of this report is to study the metabolome of several Salvia strains cultivated in the botanical garden of the University of Fribourg. The ambition is to reconstruct a phylogenetic tree based on the metabolome’s analysis and compare it to databases and similar studies. Data collected will contribute to the molecular cartography of the botanical garden. This project is led by Dr. Emmanuel Defossez and Dr. Pierre-Marie Allard [^1]. 

The study of related plants’s metabolome approaches phylogeny from an innovative perspective. It opens up investigation tracks for understanding the diversity of species we encounter in nature. Mass spectrometry(MS) -based plant metabolomic should be a method of analyse as efficiant as sequencing for phylogenetic studies. It's also what we want to experiment with our project. 

### Salvia

Among the genus Salvia from the lamiaceae family, we collected 14 plants of 11 different species. They represent 3 clades subgenus (Glutinaria, Salvia and Sclarea) of the 11 commonly accepted (1. Audibertia, 2. Calosphace, 3. Dorystaechas, 4. Glutinaria, 5. Heterosphace, 6. Meriandra, 7. Peroskia, 8. Rosmarinus, 9. Salvia, 10. Sclarea, 11. Zhumeria). Heterosphae is not clearly defined as a clade but its heritage differs as a result of geographical events. A genomic study using next-generation sequencing on which we base our comparison, defined Heterosphae as a clade [^2]. To simplify and do easier comparisons we will use the same nomenclature. 

#### Clades studied:

##### 1.  Glutinaria:

![Clade Glutinaria](https://user-images.githubusercontent.com/103578333/169149050-c9872802-53aa-484a-8532-9ade79ffd77e.png)


##### 2. Heterospheae:

![Clade Heterospheae](https://user-images.githubusercontent.com/103578333/169148462-a52c2976-12aa-49e9-b19a-be57b769ec4c.png)

![Salvia Verticillata](https://user-images.githubusercontent.com/103578333/169152780-40444591-254b-4031-8d3f-d0f57c67624e.png)

##### 3. Salvia:     

![Clade Salvia](https://user-images.githubusercontent.com/103578333/169148133-80c1a659-db9d-4324-b917-2b1bf742079c.png)


##### 4. Sclarea:   

![Clade Sclarea](https://user-images.githubusercontent.com/103578333/169152368-3339366b-4021-40a1-8408-57b84b92f232.png)

##### 5. ???

![Salvia Candelabrum](https://user-images.githubusercontent.com/103578333/169149876-5933a88f-a539-476c-aefc-121d39db55ca.png)

### Sample collection

Firstly it’s important to consider which parameters can affect results and considers some specific aspects. Plants are sessile and cannot escape to their environment. They must adjust their metabolism to both abiotics and biotic stress. Metabolites produced may therefore be likely different in the same plant living in an inhospitable environment than in a hospitable environment. This hypothesis raises the impact of the plant metabolism state that can interfere in the resolution of our biological question. In our study we bypass this potential source of error. Salvia sampling was made in the same area of the botanical garden. It means that we assume that plants have been subjected to identical stress. Of course, this does not decrease the amount of metabolites potentially suitable to detect phylogenetic links between species but it reduce variability between samples. A second interesting aspect to consider is the spatio-temporal distribution of metabolites in the plants. This underlines the importance of sampling points on the plant. For our experiment, we systematically sampled  leaves. It would also have been interesting to take the roots of each plant but for a concern of preservation of our study specimen we did not collect the roots.  Plant metabolites have already been measured by MS and listed in another study [^3]. We will use this list and compare with our results. 

### Sample preparation

At this step  of experimental design the harvest strategy is defined and the wet lab part starts. The solvent used for the extraction is also a delicate concern because it can lead to a metabolit selection before MS-analysis and a sample contamination source. The extraction solution used in this study is MeOH/H2O/formic acid (80:20:0.1). Hydrophilic compounds were extracted with polar organic solvent such as methanol because of its affinity for water molecules that leads to a hydrophilic molecules rearrangement. A low concentration of acid such as formic acid helps the ionisation of molecules and it implies that analytes become more basic than solvent [^4].  As explained, the extraction step modifies our sample and proceeds to a metabolites sorting during extraction steps. So in this study the harvest and extraction steps were performed at the same time and  in the same way for all samples to reduce variability between samples. 

### Sample analysis

After extraction and before MS-analysis an additional step of separation is executed: a liquid chromatography (LC). Briefly explained, metabolites pass through a solid column driven by a mobile phase. This leads to an elution at different speeds based on their affinity properties with the solid column and the mobile phase. At the end of the column molecules come through with a specific retention time according to their electronic properties [^5]. 
The final step of the wet lab part strategy is the MS. This technique has opened up the perspectives of understanding the global molecular cell dynamics and is commonly used in proteomic and metabolomic research. These studies are closely related since many metabolite’s transformations are induced by enzymes which are proteins.

Basic MS -instruments are composed of three elements: an ion source, mass analyser and detector. The first element performs an electrospray ionisation (ESI). It means that the ionized analytes are sprayed through a needle with high electrical potential before entering in the analyser chamber. There is different mass analysers on the market. We used a Time of flight analyzer (TOF) for our study. It correlates time of flight to mass and allows to characterize molecules based on the m/z ratio [^6]. 
The output is a MS -spectra representing the abundance of each molecules. 

### Data analysis

The dry lab has the function to organize, sort and annotate data. Depend on the software used raw files has to be convert in open source format but this modification can introduce errors.

The data treatment required 10 following steps [^7]:
1. Data import
2. MS peak detection
3. Chromatogram building (I don’t remember if we really did it)
4. Chromatogram deconvolution
5. Isotope grouping
6. Feature alignment
7. MS row filter
8. Isotope filter (min.n isotope peaks) and normalisation (TIC or Standard)
9. Gap filling (reanalyse raw data)
10. feature csv export

Based of the clean data it's possible to identify moleculs with database comparaison. GNPS can produce this work that can be long [^8]

## Material & Methods

### Sample collection

***
- Where we the plants collected ? 
- Which species were collected ? 
- Link to the iNaturalist entries of your species.

You can link a csv that you upload on github.
Go to the export link of the DBGI project on inaturalist https://www.inaturalist.org/observations/export?projects=digital-botanical-gardens-initiative
Apply eventual filters (fo rexample by username)
Save the csv and upload to github.

Example see [table X](https://github.com/commons-teaching/SBL.20004.2022/blob/main/data/observations-238383.csv) 
***

On April 13, 2022 14 leaves of plants were collected in the botanical garden of Fribourg and directly frozen in liquid nitrogen. Then samples were dried for 24 hours and stored at -80°C. 
It was a sunny day (average temperature 15.8°C in Fribourg [^10]). Plants observations were loaded with their geo-localisation on the INaturalist website (DBGI project) [^11].

[Salvia entries of the DBGI project on inaturalist](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/GroupC%20-%20Salvia%20-%20DBGI%20project%20on%20Inaturalist.csv)

Material :
- Smartphone (take picture and load them with the application INaturalist)
- Knife and tweezers (collect more or less one leave of each plants: ≥50g dry sample per strain)
- 14x 15mL Eppendorf tubes
- Liquid nitrogen in expanded polystyrene box or in its suitable bucket
- Dryer (Manufacturer Zirbus technology)

### Sample preparation

To prepare samples, we used the following material and proceeded as mentionned below in the protocol steps. 

Material :
- Tweezers
- Analytical weight-scale 
- 15x 1.5mL Eppendorf tubes and 15x glass vials with their caps 
- Liquid nitrogen in its bucket 
- Iron beads (3x per samples)
- Mixer mill MM 400 (Manufacturer Retsch)
- Spinner for 1.5mL Eppendorf tube

Protocol :
- Weigh 50g  ± 0.5g in a 1.5mL Eppendorf tube (use gloves, glasses and lab coat)
- Add 3 iron beads per tubes and add one tube with 3 beads (blank)
- Disrupt cells (Program: 30Hz, 3min) at room temperature
- Add 170µL of extraction solution MeOH/H2O/formic acid (80:20:0.1) in each sample tubes and blank
- Spin tubes (this step is not required for the blank tube)
- Prepare labels : DBGI-07-n°sample
- Transfer 1mL supernatant in glass vial and screw caps
- Store them at -80°C  

### LCMS Analysis

- Describe the LC conditions

We don’t wash the LC -column between samples and don’t add blanks between them either. The first run is performed with the blank and samples are stored in a cold chamber at 10°C before loading. Then a mixture of all samples is made and injected as a wash to set basis conditions before the injection of samples. The column is heated in order to reduce the viscosity of the running phase. It reduced the pressure required to push samples and analysis time. One run is done in 8 min. The gradient increases until the 6th minute and then stays at a high level of hydrophobicity. It means at the beginning of the run it’s low hydrophobic and then it’s high hydrophobic. 

- Describe the MS conditions

*...add things* (Q-Exactive)
The conditions set for the MS are accessible on the following link: https://github.com/commons-teaching/SBL.20004.2022/blob/main/ms_conditions.txt. 


### Data treatment

- Describe the software and parameters used.

Raw  data is on a switchdrive [^12]. Raw data files extension is converted in .mzML by proteowizard software [^13] and then processed with MzMine 2.53 software [^14]. It allows us to filter pics and identify for example possible contaminants such as environmental pollution or plastic coming from lab furniture. Pics are centroiding and then isotopes are grouped. Then clean data is loaded on filezilla to have common access on the internet [^15]. From filezilla data is loaded on GNPS (Global Natural Products Social Molecular Networking) with metadata file [^16]. We also used another software named cytoscape to visualise molecular networks [^17].

1. [group_C_metadata.txt](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/GroupC_Metadata.txt) 
2. [group_C_quant.csv](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/group_C_quant.csv) 
3. [group_C.mgf](https://github.com/commons-teaching/SBL.20004.2022_group_C_salvia/blob/main/group_C.mgf) 

#### MzMine
MzMine is a software used for the MS-data processing. A tutorial explains steps executed on our data. 
[Tutorial](https://ccms-ucsd.github.io/GNPSDocumentation/featurebasedmolecularnetworking-with-mzmine2/)

#### GNPS (Global Natural Products Social Molecular Networking)

The following setting were used:
Molecular Networking and Spectral Library Search
A molecular network was created with the Feature-Based Molecular Networking (FBMN) workflow (Nothias L-F, Petras D, Schmid R et al. Nature Methods 17, 905–908 (2020)) on GNPS (https://gnps.ucsd.edu, Wang M et al. Nat. Biotech. 2016). The mass spectrometry data were first processed with MZMINE2 (cite accordingly, see below in the Citations section) and the results were exported to GNPS for FBMN analysis. The precursor ion mass tolerance was set to 0.02 Da and the MS/MS fragment ion tolerance to 0.02 Da. A molecular network was then created where edges were filtered to have a cosine score above 0.7 and more than 6 matched peaks. Further, edges between two nodes were kept in the network if and only if each of the nodes appeared in each others respective top 10 most similar nodes. Finally, the maximum size of a molecular family was set to 100, and the lowest scoring edges were removed from molecular families until the molecular family size was below this threshold. The spectra in the network were then searched against GNPS spectral libraries (Cite Wang M, et al. Nature Biotech. 2016 and Horai, H. et al. J. Mass Spectrom. 45, 703-714 2010). The library spectra were filtered in the same manner as the input data. All matches kept between network spectra and library spectra were required to have a score above 0.7 and at least 6 matched peaks. The DEREPLICATOR was used to annotate MS/MS spectra (Mohimani, H. et al. Nat. Commun. 9, 4035 (2018)). The molecular networks were visualised using Cytoscape software (Shannon, P. et al. Genome Res. 13, 2498-2504 (2003)).
Data Deposition and Job Accessibility
The mass spectrometry data were deposited on public repository (provide the deposition accession number), such as MassIVE or MetaboLights. The molecular networking job can be publicly accessed at https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=d9eb8151a9f5459dad892bb449ccc95a (we recommend sharing this link in your manuscript).

#### Cytoscape

***add things***


## Results


### MS1

How many features could you clean in your final peak list ?
A link to the final feature list (uploaded to github).

### Molecular Network

Screenshots of your molecular network and of some clusters of interest.
Link to the GNPS job.
Link to the GNPS identification table.


![Global_network](https://user-images.githubusercontent.com/103578333/169245706-b03ae6b5-0934-4586-b0e0-d0599b9a10bb.png)


![Molecular Cluster 1](https://user-images.githubusercontent.com/103578333/169107814-5c613ec1-5651-46ab-9ef1-e9e1d2b6b4d6.png)

![Molecular Cluster 2](https://user-images.githubusercontent.com/103578333/169251784-85e0e214-0ea8-43fc-adb9-f89397f2f6a2.png)


## Conclusion

Some conclusion that you could get out of this preliminary study.

# References

[^1]: Kozlowski Gregor, Defossez Emmanuel, & Allard Pierre-Marie. (2021). Molecular cartography of the Botanical Garden of the University of Fribourg (1.1). Zenodo. https://doi.org/10.5281/zenodo.5726749

[^2]: Rose Jeffrey P., Kriebel Ricardo, Kahan Larissa, DiNicola Alexa, GonzÃ¡lez-Gallegos JesÃºs G., Celep Ferhat, Lemmon Emily M., Lemmon Alan R., Sytsma Kenneth J. & Drew Bryan T. (2021). Sage Insights Into the Phylogeny of Salvia: Dealing With Sources of Discordance Within and Across Genomes, Frontiers in Plant Science, Vol..12	
https://doi.org/10.3389/fpls.2021.767478   

[^3]: Shouchuang Wang, Saleh Alseekh, Alisdair R. Fernie, Jie Luo. (2019). The Structure and Function of Major Plant Metabolite Modifications, Molecular Plant,  vol 12, issue 7, P899-919, https://doi.org/10.1016/j.molp.2019.06.001

[^4]: Jorge Tiago F., Mata Ana T. & António Carla. (2016). Mass spectrometry as a quantitative tool in plant metabolomics, Phil. Trans. R. Soc. A.3742015037020150370
http://doi.org/10.1098/rsta.2015.0370

[^5]: Malviya, Rishabha & Bansal, Vvipin & Pal, Om & Sharma, Pramod. (2010). High performance liquid chromatography: A short review. Journal of Global Pharma Technology. 2. 22-26. 

[^6]: Walther TC, Mann M. Mass spectrometry-based proteomics in cell biology. J Cell Biol. 2010 Aug 23;190(4):491-500. 
https://doi.org/10.1083/jcb.201004052

[^7]:

[^8]:

[^9]:

[^10]: Etat de Fribourg, Energy, agriculture et environnement: Degrés-jours et température moyenne, relevés hebdomadaires, website visited on 27 April 2022 
https://www.fr.ch/energie-agriculture-et-environnement/energie/degres-jours-et-temperature-moyenne-releves-hebdomadaires

[^11]: INaturalist, website visited on 13 April 2022
DBGI project https://www.inaturalist.org/projects/digital-botanical-gardens-initiative

[^12]: Metabolomic data https://drive.switch.ch/index.php/s/U6Vezrq5mDVzSld

[^13]: Proteowizard https://proteowizard.sourceforge.io/

[^14]: MzMine 2.53 https://github.com/mzmine/mzmine2/releases

[^15]: Filezilla https://filezilla-project.org/download.php?type=client

[^16]: GNPS https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp

[^17]: Cytoscape https://cytoscape.org/

Note that you can make a footnot like this [^1]

[^1]: Ref X
