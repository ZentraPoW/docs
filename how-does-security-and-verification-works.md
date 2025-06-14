# How does Security and verification works?

Security is the foundation of any blockchain system. Security of Zentra consist with many aspects, including:

* Theory foundation
* Blockchain L1 or L2s security
* Zentra system security
* Programming language security



### Theory foundation

Zentra is created with the introduction of [Minus Theory](https://github.com/ZentraPoW/whitepaper). More precisely Minus Theory based on the textbook solid State Machine Theory. (Refer to [https://zentra.gitbook.io/dev/state-machine](https://zentra.gitbook.io/dev/state-machine) if you are not familiar)

The strong mathematics make Zentra design security at the beginning. Any honest individual run a Zentra indexer (unmodified) could always get the same state result unless there is a hardware error.&#x20;

Like Bitcoin, Zentra users trust the majority. Beyond that, Zentra keep the everyone verifiable: people can run Zentra indexer on a personal device, to ensure when malicious indexers is providing the fake state result but people can verifiy.

### Blockchain L1 or L2s security

Zentra is a new type of blockchain infrastructure project. Zentra is not a L1 or L2, but it uses existing L1 or L2 for consensus. The blocks generated by L1 or L2 should be immutable.

In a case that hard fork or reorg was happened in the prior blockchain system, Zentra need to recalculate those blocks to update the latest state.

### Zentra system security

The security issue always goes complex from theory to engineering.

Zentra system may have bug during the engineering process. However, the strength of decouple the consensus process and state calculation would be ideal, as the blocks was frozen by L1 or L2. Zentra can always fix its bug and replay all transactions in the blocks, and get the correct state.

### Programming language security

The modern blockchain system and cryptography is robust for most of time, but the hackers are always looking for gap in the unstable new design, such as programming language. It happened recently in vyper compiler and move language on sui.

This is the reason Zentra never aim to create another language, but only choose the well designed, mature language, and brings Python to blockchain world.

As a dynamic language, developers can focus on high level business logic. The integer in python is infinite and developers would never need to convert type uint128 to uint64. The fact from the industry is that, static analysis in compiler can only catch the syntax level error. In python, we save the compiling time but directly go to the test case coverage.

The best part of the security promised by Zentra is that, the more people can read the on chain code, the more security it could achieve. Imagine 1% of programmer can read the C++/Rust language logic, python code is readable for most of the programmers. It would bring better security for the blockchain.

