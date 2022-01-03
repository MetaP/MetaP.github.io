# GUI Definition Language
## Goal
Create graphical user interfaces with minimal effort for any development platform.

### Kind of Graphical User Interface (GUI)
Forms that display and update data. The data is mainly structured. 
The GUI is the frontend of a system and communicates with a backend by exchanging data. That communication can be represented by API calls.

### Abstraction
Abstraction is key. By leaving out unnecessary details the effort is reduced. And the fewer details there are, the more generic a description can be.

Conventions can be implemented by tools.

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

## Principles

### Content not Presentation
The [separation of content and presentation](https://en.wikipedia.org/wiki/Separation_of_content_and_presentation) [Wikipedia] is a very useful design principle. GDL intends to specify only the content. Content and presentation are the responsibilities of different roles. Content is a responsibility of the developer and presentation of the designer.
Modern development platforms support this principle. Just think about the use of CSS to control the presentation of HTML. Developers can create and test functional screens without any concern about presentation and use a design system to give all screens a consistent presentation.

### Model not Syntax
- Metamodel
- Abstract syntax
- Concrete syntax

Concepts, not representation

Possible model representations: 
- UML
- XML
- JSON
- C#
- ...

### Bootstrapping
- Domain Specific Languages

A metamodel can be tailored for a specific environment.

A development team often has its own slang. For instance, in my current development team we have three main types of pages called consult, manage and search pages. It is a good idea to add such shared concepts to your metamodel. Be aware that by defining them as metamodel elements, you give them a precise meaning and a delimited set of well-defined properties.

It is often possible to describe higher-level abstractions in terms of lower-level ones. For instance, our manage screen is a page of which the content is loaded during initializing by the call of a retrieve method that takes the ID of a particular entity instance as input and returns a data tree with that instance as root. The page further has a submit and a cancel button. The submit button calls a save method that accepts the modified data tree (or part of it), while the cancel button will close the page after prompting the user - and this only if the user made some changes to the data tree - with a message that his changes will be lost if he continues.

In our model we use a ManagePage element for 

### Convention over Configuration
The systematic use of conventions simplifies the models.
Configuration - the specification of particular choices - is then only necessary where the conventions - the default alternative - are not followed.

Let's elaborate the previous example. In the implementation of our GUI, we use Angular services to implement the interaction with the backend. A particular screen corresponds with a particular service, we call a task service. E.g. The "Manage Person" page - ManagePersonComponent class - uses a "Manage Person" task service - ManagePersonService class. - 

We use following conventions:
- The default name of a page ends with Component (Angular convention)
- The default name of a service ends with Service (Angular convention)
- The default name of a task service is the name of the corresponding page where the suffix Component is replaced by Service

(For simplicity, I leave out some rules concerning "namespace" and relative positioning of files in the projects workspace to avoid name clashes in bigger projects)

With these conventions it is not necessary to specify a task service unless the conventions are not followed.

By adding other rules we can further restrict the information that has to be provided in a GUI model:
- The default name of the method that returns the initial data of the page is "retrieve"
- The default name of the method to submit the modified data is "save"

If all rules are followed, the complete page can be described by stating that:
- The page is an ManagePage instance.
- Its root entity is Person.
And providing a model of the data that is retrieved and indicating 
Make sure to document your conventions. 

Or experssed as XML:
```
    <MangePage name="Person">
        ...
    </ManagePage>
```

## Data Types and Widgets
### Data Structure
- Atom
- Group
- Array

A widget (type) can manipulate certain data types. E.g. a DatePicker allows the user to enter or modify a Date.

A lot of data types can be represented by a string. Those data types can thus be manipulated by a Text widget.

Some data values are represented differently in different languages. E.g. 
- English: 1,234.5 - 12/09/21 (December 9, 2021)
- French: 1.234,5 - 12/9/21 (9 Décembre 2021)

In computing, the concept [locale](https://en.wikipedia.org/wiki/Locale_(computer_software)) [Wikipedia] is often used instead of language. The string representation of certain data types is locale-specific. 

... two functions are needed - lets call them parse and display - 
- Parse converts the text entered by a user into a value of the data type. This is not always possible. The user can enter text that can not be interpreted as a valid representation of a data type value. The same text can also represent different in different locales.
- Display converts data type values into text strings. The values of many data types can have multiple representations. The representation can depend on the locale, but even within a single locale, there can be different formats.

One can imagine a single widget that can be configured with a Display and a Parse and a 

## GDL Citizens
- Data
- Widgets
- Methods

---
<!-- Blank lines are intenional  -->
    
<!-- Blank lines are intenional  -->
Classic GUI development ... a lot of "plumbing".
An application with a consistent GUI is attractive.
The same 
### Visual Clues

GDL .. to define the content. Still there are some concepts that could be interpreted as presentation. E.g. grouping, layout . See it as 
It can be important to define the relation between (visual) elements.
Example: The capture of a time period by specifying a start and end date. 
A business rule can guard the relation;
If the rule is violated, how do we provide feedback to the user. There are a few possible scenarios. 

Suppose the user has already entered the start date and is now about to enter an end date that violates the rule. In this case it seems logical to display an error message near the representation of that end date stating something like "This end date comes before the start date."

Suppose both the start and the end date are loaded when the page opens. In this case there . So we could show two messages. One near the start date stating "This start date does not precede the end date". And one near the end date the 

A platform uses some way to represent the relation between the message and its subjects. A message could for instance be displayed as red text under the representation of their main subject. 

### Remark
Remark that the formulation of the message can depend on where it is displayed. E.g.
- If displayed near the start date: "This start date does not precede the end date" 
- If displayed near the end date: "This end date does not succeed the start date"


