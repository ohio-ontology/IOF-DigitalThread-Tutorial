# IOF Digital Thread Tutorial
## Overview

# Table of Contents
- [Part 1: Using Protégé](#part-1-using-protégé)
  - [1.1 Introduction to Protégé](#11-introduction-to-protégé)
  - [1.2 Download and Install](#12-download-and-install-protégé)
  - [1.3 Launch and Setup](#13-launch-and-setup)
  - [1.4 Import Ontology Files](#14-import-ontology-files)
  - [1.5 Create Classes](#15-create-classes)
  - [1.6 Create Individuals(Instances)](#16-create-individuals-instances)
  - [1.7 Object Property Assertions](#17-object-property-assertions)
  - [1.8 Practice for Part 1](#18-practice-for-part-1)
    - [1.8.1 Using Practice File](#181-using-practice-file)
    - [1.8.2 HermiT Reasoner in Protégé](#182-hermit-reasoner-in-protégé)
- [Part 2: Get to Know GraphDB(Ontotext)](#part-2-get-to-know-graphdb-ontotext)
  - 
- [Part 3: Transform CSV to OWL Using Ontotext Refine and GraphDB](#part-3-transform-csv-to-owl-using-ontotext-refine-and-graphdb)




## Part 1: Using Protégé
### 1.1 Introduction to Protégé
Protege is a powerful open-source ontology editor and knowledge-based framework. In this tutorial, we will walk you through the process of creating and managing ontologies using Protege.
### 1.2 Download and Install Protégé
You can download it easily from their official website (https://protege.stanford.edu/download/).
> [!NOTE]  
> The platforms-specific archives include the Java JRE, so it is __not_ required_ to have Java installed on your machine.

Looking for to learn more about Protégé visit [protegewiki.stanford.edu]([https://protegewiki.stanford.edu/wiki/Main_Page])

### 1.3	Launch and Setup
After you successfully installed Protégé on your device, subsequently launch the application!
- The first step is to set up an IRI (Internationalized Resource Identifier) for your ontology. In the Ontology header section, you can configure the Ontology IRI yourself. For example, you can set the Ontology IRI to **_<span>ht</span>tp://simpom.ohio.edu/examples/f2f-2024-DigitalThread/_** as shown below.
> [!TIP]  
> IRI of an ontology in Protege is very important in ensuring uniqueness, accessibility, interoperability, documentation, and hence effective use of the ontology. Choose meaningful and well-structured IRIs for your ontology and its components that serve a wider goal of ontology engineering and the Semantic Web while working with Protege or any other development tool for ontologies.

![Picture1](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/c4caedf5-fd13-47cf-89d4-337d5c077d4d)
> [!NOTE]  
> In this tutorial, we will focus on simple tasks such as importing ontologies, creating classes and instances, and adding relations for this ontology only, so feel free to keep it as straightforward as possible.

-	After you are satisfied with the Ontology IRI name, select **_File_** then select **_Save_** *or simply press Ctrl + S*
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/844aeecc-9819-4d63-9cc0-50bc9077dc5d)

-	A dialog box will pop up and you can pick the type of file that you would like to save your file as. For this example, we selected **RDF/XML** Syntax then select **_OK_**
-	Then select a location that you would like to save your file at _(RED 1)_.
-	Type in **File Name**: e.g. **f2f-2024-DigitalThread.rdf** (_RED 2_: this just helps remember the name since the Ontology IRI is “<span>ht</span>tp://simpom.ohio.edu/examples/**f2f-2024-DigitalThread**/”)
-	You now have an RDF file to work on for the first part of this tutorial. :) 
> [!TIP]  
> Make sure to type **.rdf** after the name that you want to save as and please ignore _File of Type:_

![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/1d1dac92-f71b-4cd5-a308-9fe2f4b2a3c5)

### 1.4 Import Ontology Files
Importing existing ontologies into Protégé is Simple! For this part, we will import **Core.rdf** (our IOF core ontology file), which will automatically do _indirect import_ of **bfo-2020.owl**(Basic Formal Ontology) and also **AnnotationVocabulary**.

-	Make sure you are in the **“Active Ontology”** tab *(BLUE 1)*, if not you can just click on the tab.
-	Click on the **Plus Button** (next to the word direct import) *(Blue 2)*. This will open the *Import ontology wizard*.
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/c3fbad7c-20a8-46a9-901d-c4d9a14b7c0f)
-	For this tutorial, we will select the first option which is **_“Import an ontology contained in a specific file.”_**
-	Then, Click **Continue** (at the bottom right corner of the popup window) and then select **Browse…**
-	Locate the file _(Core.rdf)_ that you downloaded to your computer (Tutorial folder and then import).
-	You also can simply _double click_ on the file name or just _select the file_ then click _Open_.
> **EXAMPLE**
> We cloned this (DigitalThred tutorial) repository to our local computer folder, so our file path will be GitHub\IOF-DigitalThread-Tutorial\import\Core.rdf

-	Make sure that the part file is correct and then select **Continue**
-	Lastly, select **Finish**!
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/6e52886b-147f-42d9-b8dd-f169df73071f)

-	If everything went according to plan, your protégé should have (as shown below):
    -	**_Direct Import_**:
        -	*Core* (https://spec.industrialontologies.org/ontology/202301/core/Core/)
    -	**_Indirect Imports_**:
        -	*AnnotationVocabulary* (https://spec.industrialontologies.org/ontology/202301/core/meta/AnnotationVocabulary/)
        -	*bfo* (http://purl.obolibrary.org/obo/bfo/2020/bfo.owl) {local file due to some issue}
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/30dcb44a-2bc6-4cc2-8281-92a2a42d7024)


### 1.5 Create Classes
To relate to our case studies we will create 2 Classes which are Jet Engine and Compressor.
-	Navigate  to the **_“Entities”_** tab *(GREEN 1)* [Protégé will automatically navigate you to the “Classes” tab]
-	Click **owl:Thing** (Green 2)
-	Select **“View”** tab on the top (Green 3)
-	Choose the option **Expand all**, this will allow you to see all the classes that you imported into your ontology.

![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/1cf12ec6-3b6e-40f8-8598-4d050fa67c32)

-	Locate the class named as _“material artifact”_ (_owl:Thing_ --> _entity_ --> _continuant_ --> _independent continuant_ --> _material entity_ --> _object_ --> **material artifact**)
> [!TIP]
> To activate the search engine, simply press Ctrl + F, type the keyword of what you are trying to find, and all the related results will appear. Then, double-click on the item you are interested in to locate it. It is that easy!
-	While class **“material artifact”** is selected, select **Add subclass** ![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/6e6b2c1c-d8a4-4010-b2b5-ad4f51c2e4fe)
   (locate under _“Classes”_ tab)
  -	Or Go to **Edit** _(RED 1)_, then **Create Child** _(RED 2)_
  -	Or JUST _**Ctrl + E**_ (as highlighted).
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/52b877e0-87d5-408f-b1e5-546a2dcb3cd9)

-	In the popup dialog box, for type into _Name_: **JetEngine** , then Select **OK**
-	Repeat the same process to _create_ a **Compressor class** (Name: Compressor)
  _-	You could also create a sibling for the JetEngine class!_
-	Lastly, create a class named **“Thrust”** as _a Child class_ of **quality**


### 1.6 Create Individuals (Instances)
-	Navigate to **“Individuals”** tab (still in the _“Entities”_ group tab)
-	Click **Create individual** ![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/65700046-090c-472c-8ea9-5f1e61995de1)
_ (locate under the purple individual view)_

![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/def12bdb-f22d-41a7-9d7f-30a24c7eb602)

-	A window called Create a new OWLNamedIndividual (a dialog box) will pop up.
-	Type in the Name: **je1**

> [!NOTE]
> je1 is the short name for jet engine number 1.

-	Then make sure you select the je1 individual _(RED 1)_ _[just click on it blue tab will indicate that you are selecting it]_
-	In the Description Box, locate the plus sign next to Type: then click on it. _(RED 2)_ A box will pop up.
-	Select Class expression editor (it should be already automatically selected)
  -	Then type in Jet only, then press Ctrl + spacebar, and the program will autocomplete the class name as JetEngine _(RED 3)_
  -	Press OK to finish assigning a class to the individual
-	REPEAT the 1.6 process to _create an individual_ for **Compressor** (Name: **c1**)
-	REPEAT another round but _create an individual_ for **Thrust** (Name: **th1-720**)
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/5636dbb6-6791-4bd8-ac5e-230b09941c05)


### 1.7 Object Property Assertions
-	According to an example sentence: 
_**“Jet Engine 1 has a Compressor 1 as its component. The engine has a Thrust of 720 kN.”**_

-	Look at the window called **Property assertion** (while in the _“Individuals”_ tab) located at the bottom right corner.
> [!TIP]
> If not on the interface go to the top tabs find _Window-->Views-->Individuals View-->Property assertions_, then click on the screen for the location that you would like to have it at.
-	The object properties that will be added are **"has component part at some time"** and **"has quality"**
  -	First, make sure that you select the je1 individual _(YELLOW 1)_ [just click on it blue tab will indicate that you are selecting it]
  -	Click on the plus sign![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/eedc5cb5-ef53-4b34-8aab-4fae7c4be99b)
next to the Object property assertions (“Property assertions” view ) _(YELLOW 2)_
  -	In the popped-up dialog box, enter the object property name Click on it and Type **"has component part at some time"** _(YELLOW 3)_.
  -	In Enter individual name Click on it and type c1 _(YELLOW 4)_  Then click OK _(YELLOW 5)_ to complete adding the object property.
-	Now you have the part: _“Jet Engine 1 has a Compressor 1 as its component.”_
- <ins>Repeat</ins> a similar process to get the second part: _“The engine has a Thrust of 720 kN.”_
o	Hint The object property name is **"has quality"**. The individual name is **th1-720**.
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/885df871-8539-4ff6-b59b-a29b894288cc)

### 1.8 Practice for Part 1

#### 1.8.1 Using Practice File
#### 1.8.2 HermiT Reasoner in Protégé


## Part 2: Get to Know GraphDB (Ontotext)
- To download for installation on your device --> https://www.ontotext.com/products/graphdb/download/
![Creating Repository in GraphDB](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/457e13ef-6881-4624-9433-e6749f6a01f4)

## Part 3: Transform CSV to OWL Using Ontotext Refine and GraphDB
- Here is a link to Refine Documentation Release 1.2.0 from Ontotext [OntotextRefine-Doc(1.2.0).pdf](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/files/14017364/OntotextRefine-Doc.1.2.0.pdf)
- Use the following link to visit the webpage for the release notes https://platform.ontotext.com/ontorefine/release-notes.html
![Ontotext Refine](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/e0a19878-4be3-4e8a-94e6-5f89ab13cf0f)
