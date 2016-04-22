# COR Common Protocols

This directory contains protocols commonly used in COR-Framework, these are considered the standard to be used with all implementations of COR.

# Current Protocols:
* message.proto - describes CORMessage protocol which is used for message exchange over networking channels that require serialization of runtime objects. (TCP/IP or Domain Sockets), this protocol must be implemented in every version of COR-Framework.
