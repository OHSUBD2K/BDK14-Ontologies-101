This example illustrates adding classes and class annotations into an existing SubClass hierarchy.
* The example does not make use of reasoning / automated classification or class expressions.

Constructs illustrated:

 * SubClasses (adding them)
 * Annotations
 * DatabaseCrossReferences (=xref)

Instructions:

# Open chromosome-parts.owl

== Subclasses ==

# Add the class "replication fork" to the ontology under "chromosomal part".
  * Don't worry about the ID

Moving around classes: 
# Add the term "intracellular non-membrane-bounded organelle" as a SubClass of "Thing"
# Move it, by dragging and dropping, to place it as a Subclass of 'non-membrane-bounded organelle' 

== Annotations == 

* The goal is to _replicate the existing information from GO_ on the "replication fork" class. 

# Click on the 'replication fork' class you just created.  
  # Use the (+) next to Annotations to add an annotation.
  * The annotation values are:

id: GO_0005657
name: replication fork
def: “The Y-shaped region of a replicating DNA molecule, resulting from the separation of the DNA strands and in which the synthesis of new strands takes place. Also includes associated protein complexes.” [GOC:mah, ISBN:0198547684]
database_cross_reference: Wikipedia:Replication_fork
has_related_synonym: replication focus 
xref: Wikipedia:Replication_fork

  # Add the following (using the values above)
    # A text definition for the class
      # Click on the "replication fork" class, then click (+) by Annotations
      # Choose the “Literal” tab
      # Click (select) "definition" on the left
      # Enter the definition in the "Value" window. Do not include the quotes. You can leave Type and Lang blank.
      # Click OK. THe annotation should appear in the Annotations window.
    # 2 dbxrefs to the text definition
      # Click the (@) icon beside the definition annotation
      # Click the (+) beside annotations
      # Select "database_cross_reference" in the left pane
      # Enter a value (mah). 
      # Repeat for the other cross reference (ISBN:0198547684)
    # A related synonym
      # Add an annotation to "replication fork" with the (+)
      # Choose "has_related_synonym" and enter the value
    # An xref to the class itself
      # click the (+) beside annotations
      # Choose database_cross_reference
      # Add xref (Wikipedia:Replication_fork)
      # Click OK

Synonym properties:

# Add the SubClass "site of double-strand break" to the ontology under "chromosomal part"
 # Add a synonym dbxref annotation. E.g. synonym: "site of DSB" has_exact_synonym [PMID:21035408]
    # In the Annotations window click (+) to add an annotation
    # Select "has_exact_synonym"
    # In the Literal tab, in the value field, add "site of DSB"
    # In the value field add has_exact_synonym with annotation[PMID:21035408]", click to continue.  Notice that the synonym annotation (@) is now yellow indicating it has an annotation.
    * What is the difference between an exact and narrow synonym?

