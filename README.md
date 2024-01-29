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
- 
- [Part 2: Get to Know GraphDB(Ontotext)](#part-2-get-to-know-graphdb-ontotext)
- [Part 3: Transform CSV to OWL Using Ontotext Refine and GraphDB](#part-3-transform-csv-to-owl-using-ontotext-refine-and-graphdb)




## Part 1: Using Protégé
### 1.1 Introduction to Protégé
Protege is a powerful open-source ontology editor and knowledge-based framework. In this tutorial, we will walk you through the process of creating and managing ontologies using Protege.
### 1.2 Download and Install Protégé
You can download it easily from their official website (https://protege.stanford.edu/download/).
> [!IMPORTANT]  
> Ensure that your computer is installed with Java because Protégé works based on Java application.

Looking for more tutorial visit [protege.stanford.edu](https://protege.stanford.edu/conference/2006/submissions/slides/OWLTutorial_Part1.pdf)

### 1.3	Launch and Setup
After you successfully installed Protégé on your device, subsequently launch the application!
- The first step is to set up an IRI (Internationalized Resource Identifier) for your ontology. In the Ontology header section, you can configure the Ontology IRI yourself. For example, you can set the Ontology IRI to **_http://simpom.ohio.edu/examples/f2f-2024-DigitalThread/_** as shown below.
> [!TIP]  
> IRI of an ontology in Protege is very important in ensuring uniqueness, accessibility, interoperability, documentation, and hence effective use of the ontology. Choose meaningful and well-structured IRIs for your ontology and its components that serve a wider goal of ontology engineering and the Semantic Web while working with Protege or any other development tool for ontologies.

![Picture1](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/c4caedf5-fd13-47cf-89d4-337d5c077d4d)
> [!NOTE]  
> In this tutorial, we will focus on simple tasks such as importing ontologies, creating classes and instances, and adding relations for this ontology only, so feel free to keep it as straightforward as possible.

-	After you are satisfied with the Ontology IRI name, select **_File_** then select **_Save_** *or simply press Ctrl + S*
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/844aeecc-9819-4d63-9cc0-50bc9077dc5d)

-	A dialog box will pop up and you can pick the type of file that you would like to save your file as. For this example, we selected **RDF/XML** Syntax then select **_OK_**
-	Then select a location that you would like to save your file at _(RED 1)_.
-	Type in **File Name**: e.g. **f2f-2024-DigitalThread.rdf** (_RED 2_: this just helps remember the name since the Ontology IRI is “http://simpom.ohio.edu/examples/**f2f-2024-DigitalThread**/”)
-	You now have an RDF file to work on for the first part of this tutorial. :) 
> [!TIP]  
> Make sure to type **.rdf** after the name that you want to save as and please ignore _File of Type:_
![image](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/1d1dac92-f71b-4cd5-a308-9fe2f4b2a3c5)


### 1.4 Import Ontology Files

### 1.5 Create Classes 
### 1.6 Create Individuals (Instances)
### 1.7 Object Property Assertions

## Part 2: Get to Know GraphDB (Ontotext)
- To download for installation on your device --> https://www.ontotext.com/products/graphdb/download/
![Creating Repository in GraphDB](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/457e13ef-6881-4624-9433-e6749f6a01f4)

## Part 3: Transform CSV to OWL Using Ontotext Refine and GraphDB
- Here is a link to Refine Documentation Release 1.2.0 from Ontotext [OntotextRefine-Doc(1.2.0).pdf](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/files/14017364/OntotextRefine-Doc.1.2.0.pdf)
- Use the following link to visit the webpage for the release notes https://platform.ontotext.com/ontorefine/release-notes.html
![Ontotext Refine](https://github.com/ohio-ontology/IOF-DigitalThread-Tutorial/assets/60668676/e0a19878-4be3-4e8a-94e6-5f89ab13cf0f)
