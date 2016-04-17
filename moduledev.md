# Module Development Guide

Even though specific module development guidelines should be viewed at the page of the COR-Framework implementation you are using, COR defines a standard for its modules to be intuitive to develop and use in any language.

### Communcation
Modules in every COR-Framework implementation may communicate via TCP/IP, Callback and Domain Sockets (other options are possible specific to the platoform), however the developer of the module does not have to worry about how the modules communicate or what they connect to. The communication protocol is implemented by COR-Framework in your specific runtime, and communcation itself is abstracted from the module. All the modules have to do is send_message() and receive messages via handlers.

### Message Encoding
Messages in COR are encoded using Protocol Buffers binary protocol, in order to send a message from one module to another they have to agree to use the same protocol for the message being sent. Messages are identified by their type a string name "Type" and messages whose types are the same are considered to be compatible (Measures must be taken to avoid "Type" mismatches). In order for two modules to communicate they must define a common message type and protocol buffer file for each message, this file is later compiled into a specific language of the runtime and is used to serialize and deserialize messages between objects. Please note that modules themselves do not have to worry about serialization or deserialization of the messages, the messages will be passed to them directly as native runtime objects, COR-Framework implementation encodes and decodes messages automatically.

In COR-Framework messages are defined as follows:
'''
message Person {
  required string name = 1;
  required int32 id = 2;
  optional string email = 3;
}
'''
Each message is then converted to a native runtime code that can be used to efficiently and safely manipulate the data, for more information on the syntax please refer to: https://developers.google.com/protocol-buffers/
