# COR-Framework

COR is designed to help developers efficiently utilize and share code to build distributed control systems.
The framework can be used in Cloud computing and Internet of Things fields to provide an easy to implement and use architecture for responding to events.

Normally system developed with COR Framework will consist of Input, Analysis and Response modules.
Inputs are sources of data (that is completely defined by the developer)
Analysis is business logic that uses the inputs and decides the response
Responses are modules responsible for conducting actions on the infrastructure

The modules communicate via messages described in detail the protocol specification:
https://github.com/bahusvel/COR-Framework/blob/master/protocol.md

Typical application for COR include:
* Real time backup based on system risk
* Machine health estimation
* Enforcing security policies
* Detailed resource usage and KPI reporting
* Intelligent system management
* YOUR OWN IDEA HERE!!!

COR-Framework is designed interopperate between any platform, any language and over any network. To achieve such flexibility COR defines a protocol that needs to be impletmented in the target language/platform. Once the protocol is implemented others may develop modules using the implementation and use any existing module developed by others in the project. The protocol is designed to be easy to implement and use.

Currently supported environments are:
* Python 3.X: https://github.com/bahusvel/COR-Framework-Python
* Go: https://github.com/bahusvel/COR-Framework-GO
* Feel free to develop your own... It's Easy!

To develop your own modules please visit the module development guide:
https://github.com/bahusvel/COR-Framework/blob/master/moduledev.md

# Application Developing using COR-Framework

## Event or Message Driven
COR modules do not support Request-Reply communication, COR is event driven by design so your application should consider steping away from traditional client-server approach and consider everything as events or messages. COR is designed best to solve those distributed real time problems and respond to events as soon as possible, COR models natural data flows of the system, and if you require Request-Reply based communication consider changing it to message driven approach, this will allow your application not to block waiting for responses.

## Not only COR
Applications that intend to use COR should understand its philosophy COR is not intended to replace every kind of communication, sometimes application should resort to traditional communication approaches when appropriate. For example if you are developing a web application, the client doesn't have to communicate with the back end using COR, even though its possible to use COR, RESTful service with JSON encoding would be a much better option.
