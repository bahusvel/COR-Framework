# COR-Framework

COR is designed to help developers efficiently utilize and share code to build distributed control systems.
The framework can be used in Cloud computing and Internet of Things fields to provide an easy to implement and use architecture for responding to events.

Normally system developed with COR Framework will consist of Input, Analysis and Response modules.
Inputs are sources of data (that is completely defined by the developer)
Analysis is business logic that uses the inputs and decides the response
Responses are modules responsible for conducting actions on the infrastructure

The modules communicate via messages described in detail the protocol specification:
TODO

Typical application for COR include:
* Real time backup based on system risk
* Enforcing security policies
* Detailed resource usage and KPI reporting
* Intelligent system management
* YOUR OWN IDEA HERE!!!

COR-Framework is designed interopperate between any platform, any language and over any network. To achieve such flexibility COR defines a protocol that needs to be impletmented in the target language/platform. Once the protocol is implemented others may develop modules using the implementation and use any existing module developed by others in the project. The protocol is designed to be easy to implement and use.

Currently supported environments are:
* Python 3.X: https://github.com/bahusvel/COR-Framework-Python
* Go: https://github.com/bahusvel/COR-Framework-GO
* Feel free to develop your own... It's Easy!
