# EXERCISE: More basic classification

Go to the taxon-union folder and follow the instructions below. This introduces classification using 'or' and 'not'.

This example extends the previous one introducing 'or' (UnionOf) and 'not' (complementOf)

Instructions:

1. Open taxslim-with-union.owl
2. Briefly check the asserted hierarchy - this is a subset of the NCBI taxonomy
3. Examine the 'union' classes at the top of the class hierarchy. In particular:
  1. 'Nematoda or Protostomia' (note that NCBI classifies nematodes as pseudocoelomata)
  2. 'Viridiplantae or Bacteria'
4. Select ELK reasoner and start reasoner (ignore the pop-up windows).
5. Navigate to the inferred hierarchy. How have the union terms we examined before been placed? \* Note that you'll need to know a little taxonomy here to translate the common names into scientific names (Wikipedia is your friend).
6. Create your own grouping classes and classify them. Some examples:
  1. Mouse or Human
  2. Mouse or Primate
  3. Pescetarian dietary component (plant or fish)
  4. Pescetarian dietary component, more relaxed variant (plant or fish or fungi or mollusc or arthropod)
7. Note: don't manually place these in the hierarchy, let the reasoner do this.  How can you quickly tell where this class will be placed using the DL query pane?
8. Tip: use the DL query tab to test your class expression first

9. Create a non-sensical 'transgenic hybrid' class, such as a fly-human - which is both a Drosophila and a human. What happens to this when you classify?

10. Try using the explanations feature (the '?').
Hint: the explanation is more compact if you choose two sibling taxa - e.g. Deuterostome and Protostome

11. Remove the hybrid class before moving on.

12. Use the DL query tab to find all mammals that are not humans

13. Try creating one or more of the following paraphyletic classes. This will involve the 'not' construct

14. Nonhuman primate (How can you quickly find the label used for 'Primates' if you know that human = 'Homo sapiens'?)

15. Invertebrate

16. Invertebrate chordate

17. Reptilia, as traditionally defined: (amniote minus aves and mammals)

18. A Land mammal

19. Classify your classes. What does superclass of the classified class represent?  Discuss with your instructors- does this reasoned classification reflect an evolutionary history?!

20. See HINTS.txt or talk to an instructor if you get stuck on how to classify things.
