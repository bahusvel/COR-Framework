# Definition of COR-Protocol over TCP/IP

Messages sent over TCP/IP must have a Protocol Buffers definition, they will be serialized using that definition. After the message is serialized it must be encapsulated in CORMessage buffer, which contains the name and the data for actual message. The entire message is then serialized and sent with its length in bytes prepended to it in order to separate the messages efficiently.

Each COR-Module acts as a server and a client at the same time, in order for a module to send messages to another module it must connect() to it's server socket. This is done in order to achieve symmetry in the system design without having to rely on a specific server to serve all modules. Note that multiple message types may be sent over one TCP/IP socket, multiple sockets are not required.
