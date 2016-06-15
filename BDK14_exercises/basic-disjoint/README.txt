This example illustrates the use of disjointness axioms to catch errors in the ontology.

Constructs illustrated:

 * Disjoint classes
 * A basic DL query

Instructions:

# Open bad-chromosome.owl
# Turn the reasoner on for good measure
# Do a query for all parts of a nucleus - how many?
## While we haven't covered DL queries yet the quickest way to do this is to select the DL Query pane. 
### Type the Query "part_of some nucleus" in the window.  Make sure the Subclasses and Direct subclasses check boxes in the Query results pane are clicked. Click "Execute" to run the query. How many results to you get?  What's the problem with this result set. 
#### Do a query for all parts of a mitochondrion - how many?  Again, did you expect this number of more?  Hint: Browse the existing class hierarchy.
# Given the results of the previous two queries what is the problem? (NOTE: it is a biological problem).

# Add a disjointness axiom to see if you can isolate the problem (HINT: there are several places that could use a disjoint axiom, you might have to try more than one, though only one is needed)

# Select HermiT and start it up

# Find the problem and get an explanation.

Part 2, A real-life example using a very big ontology. (Bonus)
** Do this ONLY if you have lots of RAM memory, and don't spend more than a few minutes on it.

# Open go.owl. This is a large file, working with it will take some time.
# Open from http://purl.obolibrary.org/obo/go.owl directly in Protege. Use "open from URL."
# Add a disjointness axiom between 'plasma membrane part' and 'cytosolic part'
# Run Hermit (will take a a couple minutes)
# How many unsatisfiable classes are there? Are these problematic, or is the disjointess axiom too strong?
# Discuss: What's the lesson here with respect to developing your own ontologies?

