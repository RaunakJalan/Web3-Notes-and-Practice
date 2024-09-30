# Notes

## Smart contract

1. Created by Nick Szabo 1994

2. Piece of code running on blockchain, it is a state machine and
   needs transactions to change state. It can do logic operations.

3. State change of any contract happens through mining+transactions

4. It is turing complete:  In theory it can solve any computational problem.

5. Computational power is calculated in Gas Amount.

6. Programming languages: 
        - Solidity <br />
        - Vyper: Comes from Vitalik. More secure but for academic purposes <br />
        - LLL:  Looks like Python. Legacy now. Not much development
        - Serpent: Like Python
        - Mutan: Deprecated

7. Compliler converts any of the high level language into EVM Bytecode.

8. EVM Bytecode then runs onto blockchain.

9. EVM Bytcode does not stay constant, because there are hard forks.

### Solidity:
1. Compared to ECMA script.

2. Then every Ethereum node in the network executes the same code,
   because every node has a copy of the chain.

4. Structure:
    - Class like structure
    - Contains functions
    - Control structures like if/else.
    - Loops
    - Data types 
        - (U)Int, Booleans, Array
        - Struct, Mapping, Address
        - NO FLOATS. To accomodate decimal points, make sure to make large integer.
    - Inheritance
    - Special Structures like modifiers
    - Imports

5. Layout:
    - //SPDK-License-Identifier: MIT
        - License identifier of source code.
    - pragma solidity 0.8.25
        - Version Pragma. Pre-compile statement. Locks in Solidity Compiler version
    - contract MyContract{...}
        - Contract Name Format: CamelCase
        - Inside Curly Brackets:
            - Storage Variables
            - Events
            - Modifiers
            - Functions/Constructors

6. Deployment:
    - During deployment, we sent of a transaction
    - The data field gets populated
    - The data in the data field is the compiled bytecode
    - If there is no TO attribute, then the EVM will know it is
      is a bytecode and that it has to deploy it to blockchain,
      for which it creates a new deterministic address and then
      deploys it to the address which is sent in data field of the bytecode.

    
