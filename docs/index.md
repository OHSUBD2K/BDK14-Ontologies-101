### Ontology 101 Tutorial
#### History of this tutorial

This tutorial was based upon an earlier version developed at a [Hinxton Workshop](http://wiki.geneontology.org/index.php/Hinxton_OBO-Edit/Protege_4_workshop_Jan_2012) authored by Chris Mungall, David Osumi-Sutherland, and Simon Jupp.

In 2012 and 2013, Melissa Haendel and Matt Yoder created a full tutorial for the NESCent/Phenoscape sponsored Ontology short course. Related files, and the short course version of this document are available [here](https://github.com/NESCent/ontologies-in-evobio-course-2013).

Here, Nicole Vasilevsky has updated and augmented the tutorial for use with Protégé 5.1, with funding from BD2K grant: 1R25GM114820. 

Thank you to Kent Shefchek for help with conversion to ReadTheDocs.

### Initial Preparation

These exercises were tested under Protégé 5.1.

Associated exercise files are in the Exercises folder. The files included are:

- basic-classification
- basic-disjoint
- basic-dl-query
- basic-restriction
- basic-subclass
- domain-range
- taxon-union

_Note: some screenshots may appear different if you are using a prior version of Protégé._

#### Dowloading Protégé

To download Protégé, go to: [http://protege.stanford.edu/](http://protege.stanford.edu/)

### Starting Protégé

When you start Protégé you are presented with a default empty ontology. Note that command line users on the Mac can type “open <FILE>.owl” to open the ontology in Protégé.

![](./media/Figure1.png)

We will begin by clicking into the Ontology IRI field and providing an IRI. The IRI will be used to identify our ontology on the Web. You can set the IRI to anything you want at this stage, for this tutorial we will use "http://purl.obolibrary.org/obo/owl-tutorial/ao-workshop.owl"

Figure2

You will also want to save this ontology file to your computer. Under the File menu select Save.  Use the next dialog box to specify the format of your ontology file.

Figure 3

Protégé allows you to save your ontology in a variety of OWL formats, including the OBO 1.2 flat file format. We recommend that you save your ontology in RDF/XML, as this is the most stable format to work with in Protégé. You can always choose to export your file in one of the other formats later.  Click OK to continue. Name your ontology, perhaps tutorial.owl. Choose a location on your computer to save your ontology.

#### The Protégé UI

The Protégé interface follows a basic paradigm of Tabs and Panels. By default, Protégé launches with the main tabs seen below. The layout of tabs and panels is configurable by the user.  The Tab list will have slight differences from version to version, and depending on your configuration.  It will also reflect your customizations.

To customize your view, go to the Window tab on the toolbar and select Views. Here you can customize which panels you see in each tab. In the tabs view, you can select which tabs you will see. You will commonly want to see the Entities tab and/or Classes tab and the Object Properties tab.

Figure 4

The first tab you see is the Active Ontology tab. Here you will find some basic meta-data about the ontology you are viewing. At the very top you see the IRI and file name of the active ontology you are viewing. Protégé allows you to work with multiple ontologies at once, so _this top bar is very important as it lets you know which ontology you are viewing and editing_.

Note: if you open a new ontology while viewing your current ontology, Protégé will ask you if you&#39;d like to open it in a new window. If you select no;, it will open in the current window and you can then switch back and forth to it from the Active Ontology tab.

If you say yes, it will open in a new window. If you use a Mac, you can toggle back and forth between each window by using the hot keys Command ~.

Figure5

The panel in the center is the ontology annotations panel. You can use this panel to add basic meta-data to your ontology, such as the creation date, the authors and a short description. Using the annotation panel, create a simple comment on the ontology describing what it is about. First select the + button that is labelled Annotations.

Figure6

A dialog will open, select the comment annotation on the left, and type your text into the text box on the right-hand side.  Click OK; to add the annotation.

Figure7

The comment should appear in the ontology annotations where you have the option to either edit or delete it. Throughout the application, the grey-circle icons have related functionality: a **+** is used to add, **x** to delete, and **o** to edit.

Figure8

The active ontology tab contains additional information about the ontology that we will explore later. These include a panel for managing ontology imports.

### The entities tab

You will see along the top of the screen various tabs. Each tab provides a different perspective on the ontology. An entity is any class, property (object, data, or annotation), or individual. For example, the classes tab allows us to view and edit the classes in the ontology, and similarly the object properties tab focuses on the object properties in the ontology. The _primary tab_ where you will spend most of your time is the Entities tab.

Figure 9

Select the Entities tab and then select the Thing class. Thing is the root class for all OWL ontologies and it cannot be deleted in Protégé.  

The Entities tab is split into two halves. The left-hand side provides a suite of panels for selecting various entities in your ontology. When a particular entity is selected the panels on the right-hand side display information about that entity. The entities panel is context specific, so if you have a class selected (like Thing) then the panels on the right are aimed at editing classes. The panels on the right are customizable. Based on prior use you may see new panes or alternate arrangements. 

Figure 10

#### Creating your first class

By far the most common panel for working with your ontology is the **Class hierarchy panel.**

Figure 11

There are three button at the top of the class hierarchy view. These allow you to add a **subclass (L-shaped icon)**, **add a sibling class (c-shaped icon)**, or **delete a selected class (x’d circle)**. Click the add subclass button to add a child class to OWL thing. 

Figure 12

A dialog will popup. For now, simply name this class **cellular_component**.  Click “OK” to add the class.

Figure 13

The class should have been created as follows. By default, Protégé will use the ontology IRI, followed by a #, followed by your specified name (replacing spaces with underscores) as the unique IRI for this entity. If you hover over this class with your mouse you will see the full IRI for this class.  Important: If you have previously configured an IRI generation scheme you may see your IRI being generated in an alternate format (see below).

Figure 14

#### Renaming an entity

We can change the IRI for a concept using the rename function in the Refactoring menu. Note that this function can also be accessed with a command U keystroke. Rename the **cellular_component** class to use its proper IRI from the Gene Ontology [http://purl.obolibrary.org/obo/GO_0005575](http://purl.obolibrary.org/obo/GO_0005575)

Figure 15

Make sure to check the “Show full IRI” box so you can edit the full IRI.

Figure 16

And then paste or type in the correct GO URI (http://purl.obolibrary.org/obo/GO_0005575). 

Figure 17

Now the correct GO URI appears in the ontology; in the Class hierarchy panel, the class will appear as “GO_0005575” (to those who have used Protégé before you might see a different label). Luckily you don’t have to rename every entity you create when building your own ontology; Protégé provides a “New Entities” preferences panel where you can specify how new IRI should be created, described in the next section. 

#### New entities

Terms in the ontologies we use have separate names and IDs. The names are annotation values (labels) and the IDs are represented using IRIs. The OBO foundry has a policy on IRI (or ID) generation (http://www.obofoundry.org/principles/fp-003-uris.html). You can set an ID strategy using the “New Entities” tab under the Protégé preferences – on the top tool bar, click the “Protégé dropdown, then click Preferences.

Figure 18

Set your new entity preferences as in the following screenshot, then choose the New Entities tab):

Figure 19

For ontologies other than GO, change the value of the prefix. 

Note that all OBO library ontologies should use the “Specified URI” value: http://purl.obolibrary.org/obo

#### Adding annotations properties

Using Protégé you can add annotations such as labels, descriptions, cross references (xrefs) to any OWL entity. The panel on the right, named Annotations, is where these annotations are added. Use this panel to add a **cellular_component** label to the class you created previously (notice how when changed the IRI, you also lost your label. This is because the label was previously part of the IRI, and Protégé was rendering the label based on the IRI. We’ll fix that in a minute.)  Click on the GO labelled class to select it.

Figure 20

Select the + button to add an annotation to the selected entity. Protégé has a set of built in annotation properties, such as label and comment – add rdfs:label “cellular_component” and click OK. You can also add a comment such as “created during BDK14 tutorial”, by clicking the + sign again, choosing “rdfs:comment” on the left hand side bar, and typing your comment in the “Literal” box, then click OK. 

Figure 21

Note that often you will start from an existing OWL file, then your ontology will include a pre-declared set of annotation properties such as ‘has exact synonym’ and ‘definition’. _You may never need to create your own annotation properties._

#### Setting label rendering

You can change how Protégé renders entities. It is common to want to view entities by their **label**, rather than **identifiers.** In fact, you can tell Protégé to render on any annotation property you choose. Experiment with the different options in the menu, and to conclude, set the rendering to use the class label (rdfs:label). 

In the View menu choose “Render by label”:

Figure 22

The **cellular_component** class will now render in the hierarchy view using the value of the label annotation property. Note that the ability to flip between different renderings can often be very useful in old versions of Protégé, as the Protégé search box in the upper right searches on whatever is rendered.  If you are using an older version of Protégé, searching for a term by ID for example, it can be useful to render by ID and then flip back to render by label. In the 5.1 version, the search box will search for either labels or ID.

Figure 23

#### Creating the class hierarchy

We will now create a simple class hierarchy. In Protégé, ‘class hierarchy’ typically refers to a sub/superclass hierarchy (also known as an _‘is_a’_ hierarchy in OBO format). We will return to relations such as _‘part_of’_ later on in this tutorial. For now, we will take advantage of the fact that the GO cell component ontology allows us to bypass this for now by means of classes such as ‘cell part’ and ‘nuclear part’.

Classes may be quickly added to an ontology with the **add subclass (vertical arrow below)** and **add sibling class (horizontal arrow below)** icons in the class hierarchy view.

Figure 24

Use the **add subclass (vertical arrow below)** and add **sibling class (horizontal arrow below)** buttons to create a hierarchy that looks like the following (your window will look slightly different than the view below which is from an earlier version of Protégé).  Note that you can click and drag classes in the hierarchy to re-arrange them. When planning your own ontology take a good amount of time to standardize your label format, check other ontologies, and be consistent.

Figure 25

Don’t bother to add textual definitions, synonyms, etc. at this stage, as you won’t be using this ontology in latter exercises. _Note: the order of the classes in your Class hierarchy may not be the same as you see in the screenshot (e.g. 'cell part' may appear above cell). Don’t worry about this. Just make sure that the subclass relationships are correct._








### Exercise: Basic Subclass Hierarchy

From ReadTheDocs (maybe can remove?)
Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

This will be my documentation.

.. toctree::
   :maxdepth: 2
   :caption: Contents:
   
   .. Ontology101Tutorial documentation master file, created by
   sphinx-quickstart on Tue Feb 20 10:22:22 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


