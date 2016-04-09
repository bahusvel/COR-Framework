# COR-Protocol definiton over a runtime Callback

To achieve the highest possible efficiency COR-Modules may communicate with each other within runtime using method calls. It is advisable that modules run in separate threads where possible. When sending messages within a runtime Protocol Buffers definition is not strictly neccessary, and messages should not be serialized, they can be exchanged directly given the type and the message object.

Due to the fact that Raw runtime objects may be exchanged modules from different developers may not communicate correctly hence every production module should use Protocol Buffers message defintion format to ensure correct interchange format. As messages will not be serialized no great performance penalty will occur. It is acceptable for Protocol Buffers format not being used if modules are exchanging runtime specific data that cannot be easily represented using Protocol Buffers.
