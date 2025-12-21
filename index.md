# Selection and Retention of Files in Big Data Collections: The Example of the Pergamon Excavation of the DAI Istanbul

2013, Archaeology Data Service.

*This case study was produced as a component of a two week work placement during June 2013 at the ADS funded by the [IANUS](http://www.ianus-fdz.de/) and [ARIADNE](http://www.ariadne-infrastructure.eu/) projects.*

All material in this guide is available [open access](https://archaeologydataservice.ac.uk/about/policies/use-access-to-data/) under a CC-BY 4.0 licence.

```{image} ads_logo.png
:height: 50px
:align: left
:alt: ADS Logo
```

```{image} /images/DAI-logo.jpg
:height: 50px
:align: left
:alt: DAI Logo
```

```{image} /images/IANUS_logo.jpg
:height: 50px
:align: left
:alt: IANUS Logo
```

```{image} /images/ariadne_logo.jpg
:height: 50px
:align: left
:alt: ARIADNE logo
```

## 1 Background to Research and Documentation at Pergamon

Pergamon, as the capital of the Attalid dynasty, has been one of the most important and lavishly built cities in the Hellenistic Greek world. During the Roman Empire it was a prosperous city with an estimated population of about 200,000 inhabitants. It is located in the northwest of Turkey in the ancient region of Mysia, about 25km from the sea. Having its historical origin on the top of a 330m high promontory, it successively expanded downwards to the plain of the river Kaikos from the 3rd century BC onwards. Today, the modern city of Bergama at the foot of the hill overlies great parts of the Roman city.

The first modern excavations of the impressive and widespread ruins took place in the 1870s and began with the spectacular discovery of the Great Altar which had been reconstructed at the Pergamon Museum in Berlin. Since then the ancient site has been a place of continuous investigation and research and is nowadays one of the major, long running excavation projects of the German Archaeological Institute (DAI) and its department in Istanbul[^1].

With the last change of the director of the excavations, Prof. Felix Pirson, in 2005 the digital era began at Pergamon. Under his guidance, for the first time at this site IT-related infrastructures and methods, as well as digital documentation and analysis, have been established. A new database for recording trenches, finds, surveys, boreholes, architectural studies, etc. has been developed; internal guidelines for data management, file naming strategies and formats have been established; and a local network with a server for centralised data storage and backup routines has been setup. Over the last eight years the total amount of data relating to Pergamon and its hinterland has totalled c.2 terabytes, distributed over c.150,000 single files. An example of the whole folder structure can be seen in Fig.1.
	
```{figure} /images/figure_01.jpg
:alt: Figure 1

__Figure 1__: The existing file structure of the Pergamon excavation; selection of the numbered top-level-folders for the year 2009 and the first level of subfolder within the excavations 0026. Ar, Ar-Mus, Säu, So and Zi are abbreviations for different type of trenches.
```

Although the question of how to archive this 'virtual pile of information' was never completely out of sight, only minor steps have been taken in this direction, e.g. systematically converting camera raw images to TIF or DNG format or omitting space characters in files and folder names. As the ADS has already undertaken research projects concerning 'big data'[^2]  in general, the aim of this case study will be slightly different, it should prove the feasibility of the recommendations in these Guides to a new project conducted by a German institution in a foreign country and whose data will be archived with IANUS, the future German equivalent of the ADS.

## 2 Focus of the Case Study

Often, one reason for a data collection to become a ‘big data collection’ is the involvement of longer, multi-phased and multi-disciplinary processes of generating, transforming and finalizing data. Not only can the files themselves be big in size, but also in many cases the applied methods require a multiple storing of files each presenting a different, presumably enhanced level of data. For instance, one 3D-data model as a final outcome could have been created from dozens of original source files. 

For this case study, the graphic documentation of trenches and sondages at the Pergamon project are a good example because since 2005 they are done in a nearly digital-only, multi-phased way involving different persons, file formats, applications, and stages. The resulting folder structure for one exemplary sondage is shown in Fig.2. A detailed description follows in the next chapter.

```{figure} /images/figure_02.jpg
:alt: Figure 2

__Figure 2__: The folder structure of sondage no. 2 (2009) with all subfolders extended.  The total number of files is 259, the total storage size is 1,02 GB.
```

When it comes to archiving these processes and files for the future, among others, two questions arise: 

* Is it worth keeping all of them - from the earliest raw data to the very final product - and if not, what are the criteria to discard some? 
* What are the best means to document the files and their interdependencies in order to make the whole process understandable for - and repeatable by - others?

The ADS gives some advice on these issues in these chapters:

* Guidance on the Selection of Material for Deposit and Archive[^3]
* G2GP - [Data Selection: Preservation Intervention Points()
* G2GP - [Close-Range Photogrammetry: Section 2. Data Collection and Documentation](https://doi.org/10.5284/wngr-en16)
* G2GP - [Laser Scanning: Section 1. Introduction to the Laser Scanning Guide](https://doi.org/10.5284/rt5g-dm24)

They form the theoretical basis for the following discussion.

## 3 Trench Documentation Process

This chapter describes the workflow for how the drawings of trenches are produced and what type of files are generated at different stages:

__Step 1.__ Once the plan or profile of a trench has been cleaned and prepared for documentation, several references points are distributed on the ground. Then photos are taken from an elevated point in order to get a view as vertical as possible.  The resulting camera raw image is converted as soon as possible into DNG and for practical reasons also into JPG. They are stored in different folders. The next processing steps are based on the JPG-versions of the photos.

```{list-table}
:header-rows: 1

* - Resulting file format:
  - DNG / JPG
* - File name:
  - *PE09-So-02_M003.dng* (the ‘M’ indicates that it is a ‘Messbild’  (measured image)  in contrast to ‘normal’ pictures of the trench).
* - File size:
  - c.10-17 MB per DNG
* - 
  - c.2-5 MB per JPG
* - Folder:
  - .../So-02/Fotos/Roh-Bilder/
* - 
  - .../So-02/Fotos/JPEG-Gross/
```

```{figure} /images/figure_03.jpg
:alt: Figure 3

__Figure 3__: Original image PE09-So-02_M003.dng.
```

__Step 2.__ The different reference points on the ground are surveyed with a total station or similar equipment.

```{list-table}
:header-rows: 1

* - Resulting file format:
  - CSV / SCR / ASC / GSI
* - File name:
  - *Festpunkte.asc*, *Festpunkte.gsi* (Coordinates of bench marks used for georeferencing the survey equipment and actual measurements of image reference points).
* - 
  - *180909_1.csv*, *180909_1.scr* (Reduced files only with the needed measurements as point coordinates, formatted in two similar ways).
* - File size:
  - each 0.5-2 KB
* - Folder:
  - .../_Vermessung/So-02/GSI-Dateien/180909/
```

```{figure} /images/figure_04.jpg
:alt: Figure 4

__Figure 4__: Content of the file Festpunkte.gsi opened with BBedit.
```

```{figure} /images/figure_05.jpg
:alt: Figure 5

__Figure 5__: Content of the file 180909_1.scr opened with TextEdit.
```

__Step 3.__ With the help of the coordinates the photograph gets georeferenced and rectified using a specialised application (e.g. PhoToPlan add-on for AutoCAD)

```{list-table}
:header-rows: 1

* - Resulting file format:
  - PPB / PRK / JPG
* - File name:
  - *PE09-So-02_M003-E.jpg* (the ‚-E’ indicates that the file is a ‘entzerrtes’ (rectified) picture)
* - 
  - *PE09-So-02_M003-E_jpg.ppb*, *PE09-So-02_M003-E_jpg.prk* (they both document the process of georeferencing (automated protocols) and are basically plain text files).
* - File size:
  - c.2-5 MB per JPG
* - 
  - c.0.5-2 KB per PPB and PRK
* - Folder:
  - .../So-02/Fotos/entzerrte Messbilder/
```

```{figure} /images/figure_06.jpg
:alt: Figure 6

__Figure 6__: Rectified image PE09-So-02_M003-E.jpg.
```

```{figure} /images/figure_07.jpg
:alt: Figure 7

__Figure 7__: Content of the file  PE09-So-02_M003-E_jpg.ppb opened with TextEdit.
```

```{figure} /images/figure_08.jpg
:alt: Figure 8

__Figure 8__: Content of the file  PE09-So-02_M003-E_jpg.prk opened with TextEdit.
```

__Step 4.__ One or several rectified, planar and orthogonal images get imported into AutoCAD to draw borders of stratigraphical units, to hatch and label features, to mark the spots of special finds, to add scales and north arrows and further information necessary to understand the final drawing. This usually is a longer process including checks with printouts on site. For the ease of working and consistent relative file references within AutoCAD the necessary JPGs are copied in the special drawing folder.

```{list-table}
:header-rows: 1

* - Resulting file format:
  - DWG
* - File name:
  - *PE09-So-02_Z002.dwg* (according to the naming rules the 'Z’ indicates that the file is a ’Zeichnung’ (drawing)).
* - File size:
  - c.0.5-2 KB per dwg
* - Folder:
  - .../So-02/Zeichnungen/umgezeichnete Messbilder/
```

```{figure} /images/figure_09.jpg
:alt: Figure 9

__Figure 9__: Screenshot of  the rectified image within AutoCAD.
```


__Step 5.__ The drawing is laid out in AutoCAD and then exported to PDF and JPG for easy viewing and reuse in publications, presentations, printouts, etc. By doing so the intended scale (often 1:20 or 1:50) of the drawing is also preserved.

```{list-table}
:header-rows: 1

* - Resulting file format:
  - PDF / JPG
* - File name:
  - PE09-So-02_Z002.jpg
* - 
  - PE09-So-02_Z002.pdf (both files show identical content just in different file formats)
* - File size:
  - c.2-5 MB per JPG
* - 
  - c.30-100 MB per PDF 
* - Folder:
  - .../So-02/Zeichnungen/umgezeichnete Messbilder/
```

```{figure} /images/figure_10.jpg
:alt: Figure 10

__Figure 10__: Final drawing PE09-So-02_Z002.jpg.
```


__Step 6.__ At the end it should be mentioned that the drawing is documented in the database system used by the Pergamon project, where it is described with few attributes and related to the archaeological records.


```{figure} /images/figure_11.jpg
:alt: Figure 11

__Figure 11__: Screenshot of the drawing record in the used database iDAI.field.
```

## 4 Issues of Selection and Retention

If we summarize the whole process in technical terms in the simplest case - i.e. one drawing is based on just one image - we realize that in total 13 files, including one duplication, are involved. In the example of the screenshot (Fig.12) they need about 60 MB of disk space which gives just a random, but not a representative estimate of size. The total number of file formats used is ten, of which six describe differently structured text files (PPB / PRK / SCR / CSV / ASC / GSI), two raster images (DNG / JPG), one vector graphics (DWG) and one portable and printable file (PDF). The folder structure could be as follows where the order of the different steps is integrated in the second-level folder names.

```{figure} /images/figure_12.jpg
:alt: Figure 12

__Figure 12__: An ideal and simplified folder structure for working purposes, appropriate for submitting as an SIP (excluding the documentation files with metadata).
```

Regarding the file formats, these are not critical because all of them are either already - or can easily be migrated to - long-term preservation formats such as DNG, CSV, DXF and PDF/A. More challenging is the question of which of the files are worth keeping and curating and which can be deleted as they are not useful for an AIP and/or DIP. In the following table this is briefly discussed for each file type separately.

The main criteria are as follows:
* Has a file significantly been changed so that it documents a new 'intellectual' status?
* Is a file necessary to understand the next step within a larger process?
* Is a file necessary to reproduce the whole process in future?
* Is a file needed or suitable for practical issues, especially for dissemination and retrieving?

```{list-table}
:header-rows: 1

* - Step in Process
  - Files
  - Keep for AIP
  - Keep for DIP
  - Comment
* - 1a
  - Original images in DNG
  - X (as DNG)
  -
  - Keep it in the archive as they represent the original, unchanged raw photos; not suitable for dissemination purpose
* - 1b
  - Original images converted to JPG
  -
  - X (as JPG)
  - As the images are part of the photographic documentation of a trench (regardless from their use to function as the visuals basis for a drawing) it makes sense to include them as the dissemination version of the original DNG
* - 2
  - Measurements of reference points in CSV
  -
  - X (as CSV)
  - The CSV files contain only the necessary information for the rectification of an image. In principal it can be deduced from the GSI files (documentation required) and is suitable as a dissemination version of these as they are easier to understand.
* -  
  - Measurements of reference points in SCR
  -
  -
  - The SCR files contain the same information as the CSV files with the difference of using other separators (spaces and commas). There is no need to curate them as all relevant information is deducible from the equivalent CSV files or from the preservation version of this data, i.e. the GSI files. 
* -  
  - Measurements of bench marks in ASC
  -
  -
  - The ASC files are a reduced version of the GSI files with different separators and less numbers (e.g. without leading zeros). There is no need to curate them as all relevant information is deducible from the equivalent GSI files.
* -  
  - Measurements of bench marks in GSI
  - X (as TXT)
  -
  - The GSI files contain both the coordinates for referencing the image as well as the coordinates used to position the total station on the ground. As it is the raw data produced by the surveying hardware (i.e. in this case a total station by Leica) and as the measured points are crucial for the transformation of the picture and only with them a re-rectification and re-georeferencing could be undertaken they should be archived and disseminated. For archiving the files should be converted to plain TXT-files. Important for understanding all the numbers of columns, a detailed documentation is necessary explaining how the file should be interpreted, what geodetic reference system was used, and how this can be reduced to the actual required  information (e.g. for dissemination or for re-rectification of the image)
* - 3
  - Rectified image in JPG
  - X (as TIF)
  - X (as JPG)
  - The resulting image after a successful rectification process. The answer to the question whether to archive it or not is difficult. On the one hand one could argue that it can be re-created using the original image and the coordinates and thus it does not need archiving. On the other hand, the image manifests a considerable change to the original photo, its generation depends on unknown algorithms of commercial software and the result is essential for the next stage. Therefore the migration into a TIF and the archiving seems worth the effort and it should be kept, together with the protocol PRK (see below).
* -  
  - Transformation information in PRK
  - X (as TXT)
  - X (as TXT)
  - These are auto-generated protocols describing the rectification process of an image with the help of a number of measured points. Thus it forms part of the documentation and can be migrated into a plain TXT file. 
* -  
  - Transformation information in PPB
  -
  -
  - These provide also information about the rectification process but without a technical description of the file-structure which must be provided by the software company (in this case PhoToPlan) the file is of hardly any use. Thus its reuse potential is doubtful and it probably can be dismissed.
* - 4
  - AutoCAD working file in DWG
  - X (as DXF)
  - X (as DXF)
  - The desired plan of a trench combining photographic (raster) and drawing (vector) information. As it is the final product of the process, the file requires full curatorial efforts for archiving and dissemination.
* -  
  - Rectified image in JPG
  -
  -
  - For ease of use (especially to rely only on relative and not absolute file paths when including external resource in AutoCAD) a rectified JPG image gets copied to the same folder as the DWG. As it is a duplicate of step 3 it can be deleted but in the documentation its relevance for the drawing should clearly be stated. 
* - 5
  - Final Drawing as PDF
  - X (as PDF)
  - X (as PDF)
  - The DWG is exported for the ease of presentation and use. As the DWG file itself gets archived and disseminated one could safely delete these files but as they show the targeted layout in a fixed scale they could also be useful for users in this format. Thus in this case it is decided to keep them. For the preservation version it might be necessary to convert the existing PDF into PDF/A files.
* -  
  - Final Drawing as JPG
  -
  -
  - As the JPGs are equivalent to the PDF-drawings they can be discarded.
```

In the end we get the following number of files: six files are archived (DNG, TXT, TIF, DXF, PDF/A) and six are used for the dissemination (JPG, CSV, TXT, DXF, PDF). This still seems to be a high number just for one drawing but ensures that the whole creation process is traceable. All files are available for a later repetition and the future results can be checked against the original results. In order to be able to do this the documentation of the whole process is crucial.

```{figure} /images/figure_13.jpg
:alt: Figure 13

__Figure 13__: Possible structure of AIP.
```

```{figure} /images/figure_14.jpg
:alt: Figure 14

__Figure 14__: Possible structure of DIP.
```

## 5 Documentation of processes

In Section 1 *Introduction* to the [Laser Scanning Guide](https://doi.org/10.5284/rt5g-dm24) of the G2GP there is a comprehensive overview of which metadata and documentation is required for each individual file at each step of a process. 

```{figure} /images/figure_15.jpg
:alt: Figure 15

__Figure 15__: Overview on Laser Scanning processes and documentation from Section 1.1 of *Laser Scanning for Archaeology: A Guide to Good Practice*.
```

Although the example above refers to the process of laser scanning it can easily be adopted to the process described previously. For example, for the original image the standard attributes for photos (e.g. date, camera type, photographer, etc.) need to be recorded, equally the specifications of the coordinates and the output files of the total station require additional documentation and so on. Parallel to the separate documentation of the individual files and steps, a user also needs a description of the whole process which gives an overview of the general workflow, explains the interdependencies of the different file types, lists the implications for the management of folders and files, and gives information about the decision which files are archived and disseminated and which are not. Categories for a structured documentation should contain at least the following attributes for each single step:

* Sources i.e. input files, file types, folder location
* Output i.e. destination files, file types, folder location
* Further resources i.e. used files, file types, folder location
* Hardware and software
* Selected for AIP / DIP
* Relevant metadata and general description

A documentation of the process could look like this:

```{list-table}
:header-rows: 0

* - __Step in Process__
  - 1
* - __Sources / Folder__
  - no input files
* - __Output / Folder__
  - DNG files in *.../Fotos/01a_Roh-Bilder*; JPG files in *.../Fotos/01b_JPG Gross*
* - __Further resources / Folder__
  - None
* - __Hardware__
  - Camera equipment
* - __Software__
  - Software on camera to create DNG and JPG
* - __Relevant for AIP__
  - Yes, as DNG
* - __Relevant for DIP__
  - Yes, as JPG
* - __Description__
  - Photos are taken on site with measurement points, view as vertical as possible.
* - __Relevant Metadata__
  - List of photos with detailed information.
* -  
  - 
* - __Step in Process__
  - 2.1
* - __Sources / Folder__
  - No input files
* - __Output / Folder__
  - GSI files in *.../Vermessung/02_{date}*
* - __Further resources / Folder__
  - None
* - __Hardware__
  - Survey equipment
* - __Software__
  - Software in Total Station; File Manager for transferring the files from the total station on a PC
* - __Relevant for AIP__
  - Yes, as TXT
* - __Relevant for DIP__
  - No
* - __Description__
  - Measurement points are taken with survey equipment.
* - __Relevant Metadata__
  - Detailed information about geodetic parameters in survey documentation folder.
* -  
  - 
* - __Step in Process__
  - 2.2
* - __Sources / Folder__
  - GSI files
* - __Output / Folder__
  - ASC, SCR, CSV files in *.../Vermessung/02_{date}*
* - __Further resources / Folder__
  - None
* - __Hardware__
  - PC
* - __Software__
  - Leica Point Management, TextEditor
* - __Relevant for AIP__
  - No
* - __Relevant for DIP__
  - Yes, as CSV
* - __Description__
  - The Leica-output files GSI get transformed to easier understandable files; coordinates of fixed reference points are deleted, leading numbers extracted, decimals in coordinates marked with a ".".
* - __Relevant Metadata__
  - Metadata for GSI files see step 2.1; for other files no further metadata required.
* -  
  - 
* - __Step in Process__
  - 3
* - __Sources / Folder__
  - JPG files in *.../Fotos/01b_JPG Gross*
* - __Output / Folder__
  - PPB, PRK, JPG files in *.../Fotos/03_entzerrte Messbilder*
* - __Further resources / Folder__
  - CSV files in *.../Vermessung/02_{date}*
* - __Hardware__
  - PC
* - __Software__
  - AutoCAD 2007 and Add-On PhoToPlan
* - __Relevant for AIP__
  - Yes, as TIF and TXT
* - __Relevant for DIP__
  - Yes, as JPG and TXT
* - __Description__
  - The original photos are rectified with the help of the coordinates of the measurement points.
* - __Relevant Metadata__
  - The used Software PhoToPlan produces an automated protocol about the rectification process (= PRK files).
* -  
  - 
* - __Step in Process__
  - 4
* - __Sources / Folder__
  - JPG files in *.../Zeichnungen/ 04_umgezeichnete Messbilder*
* - __Output / Folder__
  - DWG files in *.../Zeichnungen/ 04_umgezeichnete Messbilder*
* - __Further resources / Folder__
  - None
* - __Hardware__
  - PC
* - __Software__
  - AutoCAD 2007
* - __Relevant for AIP__
  - Yes, as DXF
* - __Relevant for DIP__
  - Yes, as DXF
* - __Description__
  - The rectified image (the version in the folder 04_umgezeichnete Messbilder is an identical copy of the version in 03_entzerrte Messbilder) is imported into AutoCAD and functions as the visual basis for the vector-drawing.
* - __Relevant Metadata__
  - The structure of the DWG-drawings (styles, layers, layouts, etc.) is described in the drawing documentation folder.
* -  
  - 
* - __Step in Process__
  - 5
* - __Sources / Folder__
  - DWG files in *.../Zeichnungen/ 04_umgezeichnete Messbilder*
* - __Output / Folder__
  - PDF files in JPG files *.../Zeichnungen/ 05_finale Zeichnung*
* - __Further resources / Folder__
  - None
* - __Hardware__
  - PC
* - __Software__
  - AutoCAD 2007
* - __Relevant for AIP__
  - Yes, as PDF/A
* - __Relevant for DIP__
  - Yes, as PDF
* - __Description__
  - The final drawing is exported as PDF and JPG to preserve the proper scale and layout. 
* - __Relevant Metadata__
  - Relevant metadata about the final drawing is recorded in the used database system.
```

[^1]: [http://www.dainst.org/index_650_de.html]
[^2]: *Preservation and Management Strategies for Exceptionally Large Data Formats: Big Data*. Final report: http://archaeologydataservice.ac.uk/attach/bigData/bigdata_final_report_1.3.pdf
[^3]: [http://archaeologydataservice.ac.uk/advice/selectionGuidance]