# SW-Project
Project of the course of Semantic Web 2020/2021 @ University of Pisa
Exercise
The fundamental concepts in an application domain related to narratives (intended as stories about a specific
topic) are: events, characters, objects and locations. Some of the facts that characterise this domain can be
stated as follows:
1. A narrative is composed of one or more events.
2. A narrative is composed exclusively of events.
3. Each event occurs in exactly one location and has exactly one beginning and one ending, both
represented as a datetime using the appropriate XSD datatype.
4. A character can be human or not human.
5. Each location can be a real location or a fictional location.
6. Each character, each location and each object have a name (a string).
7. Each event has at least one participating character or object.
8. Each narrative is created by at least one narrator.
9. The narrator has at least one contract with a publisher.
10. A book reports one or more narratives.
11. A book has a title (a string) and it is identified by an ISBN code (a string).
12. A book has exactly one publisher (that is an organisation). The publisher is identified by a name (a
string) and an ID (a positive integer).
13. A publisher publishes more than one book.
14. A book has exactly one price (a positive integer).
15. The publisher sells the books through more than one bookshop.
16. Narrative, event, location, character, object, narrator, book, bookshop and publisher are pairwise
disjoint concepts.

The candidate should express all the above statements in an OWL 2 DL ontology, using the RDF Turtle
notation. In particular, the ontology must:

Q1. Declare the required classes, providing for each class a textual label and a concise textual description of
the intension of the class, using the appropriate annotation properties from the RDF Schema vocabulary
Q2. Provide the sub-class axioms defining the class taxonomy
Q3. Declare the required object properties, providing for each property:
Q.1. a textual label, using the appropriate annotation property from the RDFS vocabulary
Q3.2. a textual description of the intension of the property, using the appropriate annotation property
from the RDFS vocabulary
Q3.3. one axiom defining the domain of the property
Q3.4. one axiom defining the range of the property
Q3.5. one axiom defining the inverse of the property
Q3.6. any additional axioms expressing disjointness of the property with other object properties, and
the property characteristics.
Q4. Provide the sub-property axioms defining the object property taxonomy
Q5. Declare the required data properties, providing:
Q5.1. a textual label, using the appropriate annotation property from the RDFS vocabulary
Q5.2. a textual description of the intension of the property, using the appropriate annotation property
from the RDFS vocabulary
Q5.3. one axiom defining the domain of the property
Q5.4. one axiom defining the range of the property
Q5.5. any additional axioms expressing disjointness of the property with other data properties, and
whether the property is functional.
Q6. Define the axioms necessary for expressing any statement in 1 to 16 that has not already been
expressed.
Q7. Populate the ontology with at least one individual for each class, and at least one assertion for each
property.
In addition, the candidate must:
Q8. Identify two different assertions that would make the ontology inconsistent.
Q9. Define the complex role inclusion axiom capturing the fact that if a narrator creates a narrative that is
reported in a book that is published by a publisher, then the narrator has a contract with that
publisher.
Q10. Verify if the created ontology (including the complex role inclusion axiom defined in Q9) satisfies
the global restrictions on the axioms of an OWL 2 DL ontology.
Q11. Write the following queries in SPARQL:
Q11.1. Find how many events occurred in real locations, grouped by location.
Q11.2. Find all the books with the ID of the publisher lower than 5000.
Q11.3. Find all the events that do not have any human participants.
Q11.4. Find the number of the narratives that are published in a book, along with the title of the book,
the ISBN code of the book and the publisher of the book.
Q11.5. Find all the distinct events that have a human participant or occur in a real location.