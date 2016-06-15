This example illustrates how to use object properies to make
existential restrictions.

In OWL, it helps to think in terms of the set of entities represented
by each class. To say: "every finger is part of a hand" we say:

  finger SubClassOf part_of some hand

The anonymous class expression "part_of some hand" represents the set
of all instances that have a part_of relationship to a hand. Every
member of the set of all fingers is a member of the set of all things
that are part of a hand.

Instructions:

# Open er-sec-complex.owl
# Navigate to the class "protein complex" using the search box
# Add a class 'endoplasmic reticulum Sec complex' as a subclass of "protein complex"
# Say that every 'endoplasmic reticulum Sec complex' is part of a 'rough endoplasmic reticulum membrane'
# Say that a 'endoplasmic reticulum Sec complex' has a 'Sec61 translocon complex' as part 

Navigating over the resulting ontology:

# Refresh the reasoner
# Navigate to "rough endoplasmic reticulum membrane".  
# Find the parts of the rough ER membrane.
## Hint1: Existential Tree view? 
## Hint2: Remember writing a query?

== Aside == 

If you like you can look up AmiGO/QuickGO or consult the current GO in
Obo-Edit to examine how the part of restrictions in the actual ontology were created. See also the HINTS.obo file.


