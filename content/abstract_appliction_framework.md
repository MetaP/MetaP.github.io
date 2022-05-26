# Abstract application framework






There are a lot of application frameworks for different environments. (See [Application Framework](https://www.techopedia.com/definition/6005/application-framework) [TechOpedia])
 Is it possible to define an abstract application framework that describes the desired or possible features of any concrete application framework.
A concrete application framework is then an implementation of the abstract application framework for a particular environment.

What are the essential features of an application framework to build SPAs ?

- GUI
  - Page
  - Navigation
  - Menu
  - Session management
  - Messages (Validation, Errors, Warnings)
- Services
  - Business API
  - Security
    - Authentication
    - Authorization
  - Translation
  - Configuration
    - User settings

## Development Environment
- Technology
- Framework
- DSL

## Channels
(See [Operating system](https://en.wikipedia.org/wiki/Operating_system) [Wikipedia])
- Native desktop OS
  - Windows
  - macOS
  - Linux
- Native mobile OS
  - Android
  - iOS
- Browser

## Characteristics of a modern application
- cloud-based
- client/server
- client runs in browser (or on native mobile OS)
- all client/server interaction is done via Web APIs (REST, microservices?)

Web applications are currently often implemented as single-page applications. (SAP) 

> SAP (single-page application) is an implementation technique. (See [Single-page application](https://en.wikipedia.org/wiki/Single-page_application) [Wikipedia]) Pages are modeled as separate entities. SAP is thus not an essential characteristic of the abstract application framework. My former naming "abstract single-page application framework" was not correct.