# Vision

As developers, we automate the business of others, but often tend to forget to automate our own.

The development of software involves a lot of tedious repetitive work.

Emphasis is often on the differeneces between technologies , while similarities are ignored. This process of ... the details to 

still, I feel as if I am building the same type of application over and over again.

to see different situtations as instances of the same problem is called abstraction.

A development team has often an elaborate jargon (slang) to talk about the work to be done. For instance, in my current development team we have three main types of pages called consult, manage and search pages. But until recently we did not have 

If those common concepts are formalize, they can be used as ... and it is possible to create concrete software artifacts that implement them.

Not all words . This can be discovered by trying to formally define the concepts behind these words. If you discover 
It is possible that . The discussion can still be interesting since it sometimes leads to new more precise concepts and corresponding terms.

## DSL

Abstraction is key.

Formalize the 

try to ... what exactly is a manage consult or manage page. When I did that exercise for our team, I discovered that consult and manage pages were very similar except that the former only displays data while the other allow to edit it. So, I introduced the context page as a generalization ... the common aspects of both.

(This only from a technical point of view. Functionally consult and manage pages are used differently. While the data content of manage pages is often restricted around a single entity (and its constituent parts), consult pages are used to visualize larger "root" entities. Typically, a user first opens a consult page and navigates to particular parts of the page, by scrolling or using tabs, to view the details. To make modification he then opens management pages to edit particular parts, returning to the manage page when done.)

The DSL to describe your application will depend on your 

It captures the concepts of your environment.

What this site describes is the DSL for a hypothetical application development environment - a kind of simplified summary of the environments I encountered during my career. - Chances are that it will not fit exactly your environment. But, I am confident that you can easily adapt the artifacts and tools presented here to fit your needs.

Not so strange since a DSL is by definition adapted to its specific domain.

A remark about domain here. There are in fact two categories of domains. 
One category captures the concepts used by developers to create applications. It is about websites and pages, APIs and DTOs, classes and tables. The other category captures the concepts of the business the applications are used for. This site is about the first category.

## Model or Models
A collection of models is also a model. A collection of DSLs is also a DSL. I sometimes use the plural and sometimes the singular. As you see, it doesn't matter that much.