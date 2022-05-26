# Form Definition Language
Forms are essential on parts of a GUI.

A Form is an essential GUI construct.

A form displays information 
A form represents data.

## Textual Representations
Part of the information is displayed as text. 
If the information itself is text, it can be displayed as such.
Other types of information can be represented as text. The correct representation of a value often depends on the context. Think about the representation of decimal numbers or dates. The locale, the combination of a language and region, is often a parameter of the context. User preferences can also be context parameters.

## Positional Representation
The relative position of 
The relative position of the rerpesentations of 
Indentation can be used to represent links[^1] between the represented entities.  hierarchy ("tree") is often used to represent 

# Model
A form has a visual structure.

A form has a data structure.

The data structure can often be inferred from the visual structure.


## Data Binding
Elements of the visual structure are linked to elements of the data structure.

Visual elements can represent elements of the data structure and their relative positions can represent the links between those data elements. As such the form becomes a visual representation of the data structure.

If the visual elements can be modified by the user, they can be used to modify the values of the bound data elements or modify the structure itself by adding, removing or displacing data elements. 

The data structure can often be inferred from the visual structure. (Elaborate...)

It is possible that multiple visual elements on the form bind to the same data element.

# Concepts
I try to use ... names and concepts. Some terms have precise definitions in particular contexts. use the following [UML](https://en.wikipedia.org/wiki/Unified_Modeling_Language) terminology and concepts:
- An object is an instance of a class.
- A link is an instance of an association.
### Relations
The UML term <span class="concept" style="color: red; font-weight: bold; font-style: italic">association</span> is used here to denote structural relationships between classes. 

> In the UML the term [relation(ship)](https://www.ibm.com/docs/en/rational-soft-arch/9.5?topic=diagrams-relationships-in-class) is more general. [Association](https://www.uml-diagrams.org/association.html) is only one particular type of relation, next for instance [generalization](https://www.uml-diagrams.org/generalization.html) or [dependency](https://en.wikipedia.org/wiki/Dependency_(UML)).

[^1]: A <span class="concept" style="color: red; font-weight: bold; font-style: italic">link</span> is an instance of an ***association*** like an ***object*** is an instance of ***class***. If an association connects two classes, the links of that association connect instances of those classes.