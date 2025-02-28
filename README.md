<p align="center"><img src="etherdog.png"></p>

This repository contains specifications for the peer-to-peer networking protocols used by
Ethereum.

- [Node Discovery Protocol v4]
- [Node Discovery Protocol v5] **(Draft Specification)**
- [RLPx transport protocol] (version 5) and several RLPx-based capabilities:
  - [Ethereum Wire Protocol] (version 63)
  - [Light Ethereum Subprotocol] (version 2)
  - [Parity Light Protocol] (version 1)

The issue tracker here is for discussions of protocol changes. It's OK to open an issue if
you just have a question. You can also get in touch through our [Gitter channel].

Protocol level security issues are valuable! Please report serious issues responsibly
through the [Ethereum Foundation Bounty Program].

### The Mission

devp2p is a set of network protocols which form the Ethereum peer-to-peer network.
'Ethereum network' is meant in a broad sense, i.e. devp2p isn't specific to a particular
blockchain, but should serve the needs of any networked application associated with the
Ethereum umbrella.

We aim for an integrated system of orthogonal parts, implemented in multiple programming
environments. The system provides discovery of other participants throughout the Internet
as well as secure communication with those participants.

The network protocols in devp2p should be easy to implement from scratch given only the
specification, and must work within the limits of a consumer-grade Internet connection. We
usually design protocols in a 'specification first' approach, but any specification
proposed must be accompanied by a working prototype or implementable within reasonable
time.

### Relationship with libp2p

The [libp2p] project was started at about the same time as devp2p and seeks to be a
collection of modules for assembling a peer-to-peer network from modular components.
Questions about the relationship between devp2p and libp2p come up rather often.

It's hard to compare the two projects because they have different scope and are designed
with different goals in mind. devp2p is an integrated system definition that wants to
serve Ethereum's needs well (although it may be a good fit for other applications, too)
while libp2p is a collection of programming library parts serving no single application in
particular.

That said, both projects are very similar in spirit and devp2p is slowly adopting parts of
libp2p as they mature.

### Implementations

devp2p is part of most Ethereum clients. Implementations include:

- C#: Nethermind <https://github.com/tkstanczak/nethermind>
- C++: Aleth <https://github.com/ethereum/aleth>
- C: Breadwallet <https://github.com/breadwallet/breadwallet-core>
- Elixir: Exthereum <https://github.com/exthereum/ex_wire>
- Go: go-ethereum/geth <https://github.com/ethereum/go-ethereum>
- Java: Cava RLPx library <https://github.com/consensys/cava/tree/master/rlpx>
- Java: EthereumJ <https://github.com/ethereum/ethereumj>
- Java: Pantheon <https://github.com/PegaSysEng/pantheon>
- JavaScript: EthereumJS <https://github.com/ethereumjs/ethereumjs-devp2p>
- Kotlin: Cava Discovery library <https://github.com/consensys/cava/tree/master/devp2p>
- Nim: Status eth_p2p <https://github.com/status-im/nim-eth-p2p>
- Python: Trinity <https://github.com/ethereum/trinity>
- Ruby: Ciri <https://github.com/ciri-ethereum/ciri>
- Ruby: ruby-devp2p <https://github.com/cryptape/ruby-devp2p>
- Rust: Parity Ethereum <https://github.com/paritytech/parity-ethereum>

WireShark dissectors are available here: <https://github.com/ConsenSys/ethereum-dissectors>

[Ethereum Foundation Bounty Program]: https://bounty.ethereum.org
[Ethereum Wire Protocol]: ./caps/eth.md
[Gitter channel]: https://gitter.im/ethereum/devp2p
[Light Ethereum Subprotocol]: ./caps/les.md
[Node Discovery Protocol v4]: ./discv4.md
[Node Discovery Protocol v5]: ./discv5/discv5.md
[Parity Light Protocol]: ./caps/pip.md
[RLPx transport protocol]: ./rlpx.md
[libp2p]: https://libp2p.io
