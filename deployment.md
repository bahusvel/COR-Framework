# COR-Architechtures

COR provides 3 basic architechtures for distributed system deployment, each of which will be suitable for specific scenarious.

## Free Structure

In free structure any module may connect to any module and send messages anywhere, this is the most basic kind of architecture that offers the most flexibility but does not provide any resiliency or optimisations provided by other architectures. Ultimately any architecture can be represented as free structure.

## Aggregation Tree

In case of aggregation tree, all modules are leaves a connected as leaves of a tree, in which tree nodes are special types of aggregation modules that provide points of exchange for the messages. Modules may not communicate with each other but only with their correspoding exchanges. The exchanges employ responsobility passing technique in order to deliver messages to the right modules:
* Passing Down - If the recipient of the message (module or exchange) is connected directly to the exchange node, the node will delivery the message directly to the module.
* Passing Up - If no node (module or exchange) is connected to the exchange node the node must pass the message towards the root of the tree (to the exchanges parent), in which case it is up to the parent to decide what to do with the message and it will follow the same two rules.

    +------------------------------+
    |	     +------------+        |
    |	     | Aggregator |        |
    |	     +------------+        |
    |       /	           \	   |
    |+-----^--+	         +--^-----+|	
    || Module |	         | Module ||
    |+--------+	         +--------+|
    +------------------------------+

## Aggregation Mesh
