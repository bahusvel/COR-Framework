# COR-Protocol definition for communication over Domain Socket

Domain socket communication method is designed for good performance communication between different runtimes within the system. Due to the fact that the domain sockets are platform specific multiple implementations may exist for each framework.

Messages sent through domain sockets are serialized in the same way as TCP/IP. And each COR-Module must be capable of acting as server or a client, the same way as in TCP/IP.
