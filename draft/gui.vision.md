# GUI Definition - Vision
The implementation of a GUI involves a lot of "plumbing".
A lot is convention.
Most forms can be described with a very 
Often the definition of a form is nothing more than the description of a data structure and
The GUI is nothing more than the description of how an end user can interact

The interaction of the front- and backend of an application can be fully described by set of API methods.

A frontend is composed of pages. Pages interact with the backend via API methods. Each page interacts with one or more API methods. The role of the uses one or more 

A user interacts with the backend via the pages of the GUI. This results in the calling of API methods to retrieve data from the backend and  exchange data with the backend. The purpose of the page is

A page retrieves the data it displays from the backend and allows the user modify the retrieved data, enter new data, send those modifications to the server and trigger actions. All interaction between page and backend can be represented by method calls.

A method call can be modeled as an exchange of data. During a call, input arguments are sent from frontend to backend and some time later the backend responds by sending back return values and output arguments. Whether this exchange is performed in a synchronous way - the caller is blocked between the start of the call and the return of the method - or in an asynchronous way - the caller makes the call and continues and is interrupted later when the return data (or some part of it) becomes available - is an implementation detail. Although a synchronous implementation differs considerably from an asynchronous one, the abstract description of the page can be the same.

## Model
 
A ***view*** consists of one or more pages that allow the manipulation of a particular data structure, we call a ***view model***. Widgets on the pages interact with elements of the view model. They can display the values of those elements and eventually modify them.

API method calls also interact with the view model. Typically, the view model is initialized with backend data obtained from a call to a retrieve method during initialization of the view and view model data is passed back to the backend by the call of a save method.

Method calls are triggered by life-time events of the pages and events of the widgets.

A view often consists of a single page, in which case the view model represents the data of the page. 
 

## Widgets
Widgets interact with the 

# Attempt 2

The DSL to describe your application will depend on your 

It captures the concepts of your environment.

What this site describes is the DSL for a hypothetical application development environment - a kind of simplified summary of the environments I encountered during my career. - Chances are that it will not fit exactly your environment. But, I am confident that you can easily adapt the artifacts and tools presented here to fit your needs.

Not so strange since a DSL is by definition adapted to its specific domain.

A remark about domain here. There are in fact two categories of domains. 
One category captures the concepts used by developers to create applications. It is about websites and pages, APIs and DTOs, classes and tables. The other category captures the concepts of the business the applications are used for. This site is about the first category.

## Model or Models
A collection of models is also a model. A collection of DSLs is also a DSL. I sometimes use the plural and sometimes the singular. As you see, it doesn't matter that much.