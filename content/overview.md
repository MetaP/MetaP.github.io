# Overview
## Entity Model
An entity model is an UML class diagram that represents the concepts of the domain.

An entity is a UML class that represents a domain concept.

## Software Artifacts
Many relations exist between software artifacts. Artifacts can be composed of other artifacts. A GUI page consists of widgets. 

Applications manipulate entity representations.

### Link Software Artifacts to Entity Model Elements
Many software artifacts are representations of elements of the entity model. For instance, a database table can represent an entity class, and its rows the instances of that class. A field on a GUI page can represent an attribute of an entity.
This traceability can guide the software implementation. For instance, the tooltip that appears when a user hovers the mouse over a widget linked to an entity attribute can display the description of that attribute from the entity model.

## Data Model
The same entity is linked to different GUI parts. Different GUI parts can be linked to different
A form can display or manipulate only part of an entity. 
In general there is a many-to-many relation between software artifacts and entity model elements.
A data model describes how the entity model elements are linked to the entity model.
Any element of the entity model can be incorporated in the data model, but more complex mappings are also possible.
A data element can be defined by an expression involving zero, one or more elements of the entity model. For example: The address printed on an envelope composed of different elements - like the first and last name - of a person entity and an address entity linked to that person - like the street, house number, postal code, city and country.