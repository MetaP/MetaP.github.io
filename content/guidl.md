# GUI Definition Language
## Goal
Create graphical user interfaces with minimal effort for any development platform.

### Kind of Graphical User Interface (GUI)
Forms that display and update data. The data is mainly structured. 
The GUI is the frontend of a system and communicates with a backend by exchanging data. That communication can be represented by API calls.

### Abstraction
Abstraction is key. By leaving out unnecessary details the effort is reduced. And the fewer details there are, the more generic a description can be.

From a generic description different implementations can be generated by applying the conventions of the respective development environments. Conventions can be implemented by tools.


## Conceptual Model
A system is fully defined by its APIs.
An API consists of methods that:
- return data
- trigger actions, possibly requiring input data

A GUI lets the user interact with a system by:
- calling API methods
- display data (returned by the API methods)
- allow the user to enter and modify data

GDL describes the GUI. It should thus specify:
- which API methods are called when
- how the output of the API methods is displayed
- how the user can specify the input of the API methods

That's all folks! Should be simple, no? :smirk:
