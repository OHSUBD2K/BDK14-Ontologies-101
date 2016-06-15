This example extends the previous one introducing "or" (UnionOf) and "not" (complementOf)

Instructions:

# Open taxslim-with-union.owl
# Briefly check the asserted hierarchy if you like - this is a subset of the NCBI taxonomy
# Examine the "union" classes at the top of the class hierarchy. In particular:
 # 'Nematoda or Protostomia' (note that ncbi classifies nematodes as pseudocoelomata)
 # 'Viridiplantae or Bacteria'
# Select HermiT as the reasoner and start it.
# Navigate to the inferred hierarchy. How have the union terms we examined before been placed? 

* Note that you'll need to know a little taxonomy here to translate the common names into scientific names (Wikipedia is your friend).

# Create your own grouping classes and classify them. Some examples:
 # Mouse or Human
 # Mouse or Primate
 # Pescetarian dietary component (plant or fish)
 # Pescetarian dietary component, more relaxed variant (plant or fish or fungi or mollusc or arthropod)
# Note: don't manually place these in the hierarchy, let the reasoner do this.  How can you quickly tell where this class will be placed using the DL query pane?
# Tip: use the DL query tab to test your class expression first

# Create a non-sensical "transgenic hybrid" class, such as a fly-human - which is both a Drosophila and a human. What happens to this when you classify?
# Try using the explanations feature (the "?").
 # Hint: the explanation is more compact if you choose two sibling taxa - e.g. Deuterostome and Protostome
# Remove the hybrid class before moving on. 

# Use the DL query tab to find all mammals that are not humans
# Try creating one or more of the following paraphyletic classes. This will involve the "not" construct
 # Nonhuman primate (How can you quickly find the label used for "Primates" if you know that human = 'Homo sapiens'?)
 # Invertebrate
 # Invertebrate chordate
 # Reptilia, as traditionally defined: (amniote minus aves and mammals)
 # A Land mammal
# Classify your classes. What does superclass of the classified class represent?  Discuss with your instructors- does this reasoned classification reflect an evolutionary history?! 
# See HINTS.txt or talk to an instructor if you get stuck on how to classify things.
