# Solving Back-To-Genesis | BTG Proposals (BTGPs)

This repository serves as a public platform for the exploration of ideas aimed at resolving the Back-To-Genesis problem, particularly within the framework of the RUN library on BitcoinSV (refer to https://Runcraft.io).

At this stage, the primary emphasis is on brainstorming solutions and cultivating a shared vision, or multiple visions, for a viable solution that can be implemented at a later stage.

## Table of contents

> - [Summary of the Back-to-Genesis Problem](#summary-of-the-back-to-genesis-problem)
> - [How to Contribute](#how-to-contribute)
> - [Formatting Guidelines](#formatting-guidelines)
> - [Copyrights and Public Domain](#copyrights-and-public-domain)
> - [Seed Ideas for Inspiration](#seed-ideas-for-inspiration)


# Summary of the Back-to-Genesis Problem

For a detailed explanation of the problem, you can watch this video by Joshua Henslee (@jdh7190): [Watch Video](https://www.youtube.com/watch?v=hT86Y9wnNkY)

In the context of the RUN library, which introduces a layer 2 smart contract virtual machine on top of the Back-to-Genesis problem, here is a concise summary of the issue:

1) Smart contracts operate within a virtual machine as a second layer.
2) The sole method to synchronize and validate the latest state of a contract is by processing the entire chain of transaction back to its genesis (thus the term "back to genesis").
3) As contracts interact with each other, they depend on indexing each other, leading to potentially exponential growth in indexing costs.
4) The current, suboptimal solution involves restricting interoperability and allowing only manually whitelisted contracts to interact with your own contracts.
5) A more desirable solution should aim to preserve better interoperability while mitigating the escalating indexing costs, particularly for newcomers who are unable to afford running expensive indexing nodes.

# How to Contribute

To get started, begin by reading the various proposals within this repository.

You can contribute in two ways:

1) Open issues to initiate discussions.
2) Submit new proposals via pull requests.

For contributions to existing proposals or for creating new ones that haven't been suggested yet, feel free to open a pull request. Refer to the "Formatting" section below for guidelines on how to structure your proposals.

As the project progresses, if distinct solutions start to emerge, we will categorize each of them into separate folders, providing a summary in this README file.

# Formatting Guidelines

These formatting guidelines are loosely inspired by the concept of Bitcoin BIPs (Bitcoin Improvement Proposals) as defined [here](https://github.com/bitcoin/bips). It is highly recommended that each BTGP contains a single key proposal or new idea. The more focused the BTGP, the more likely it is to be successful.


Each BTGP should include the following sections:

- **Header** - like the example header provided below including title, authors, etc. Feel free to add more fields if you think they would improve the review process.

```txt
  BTGP: 1
  Title: First BTGP proposal
  Authors: Zhell <zhell1057@gmail.com>
  Created: 2023-09-26
  ```

- **Abstract:** A concise description of the proposal in fewer than 200 words.
- **Motivation:** An explanation of why existing protocols and proposals are inadequate, and how your proposal is superior or at least worthy of consideration.
- **Specification:** A detailed technical explanation of how your idea would work.
- **Economics:** In-depth insight into the economics to ensure the long-term success of all participants in the protocol.
- **Backward Compatibility:** Clarification regarding whether backward compatibility will be affected and the severity of such an impact. Describe potential transition processes that could be implemented to facilitate a smooth migration.

# Copyrights and Public Domain

Please be aware that by submitting a BTGP, you are automatically placing it in the public domain for unrestricted use.

# Seed Ideas for Inspiration

1) **Full Indexer**

Build a full indexer that covers the entire protocol. However, it's worth noting that maintaining such an indexer is prohibitively expensive and resource-intensive. The lack of a clear economically viable business model presents a challenge. This issue was exemplified by the original RunConnect indexer node, which went bankrupt due to a single app generating an overwhelming number of transactions, degrading service quality for other apps, and becoming unsustainable.

2) **Co-Signer**

Introduce a co-signer (aka authorizer) for each transaction, or even establish a pool of co-signers. Keep in mind that this approach may increase centralization at the transaction creation level.

3) **Full History**

Include the complete token history within each transaction. However, be aware that this could lead to exponentially rising transaction fees as the transaction chain grows.

4) **Script Protocol Implementation**

Implement the entire RUN protocol in script (using [scrypt](https://scrypt.io/)) and integrate it into each transaction's lock. This is most likely too burdensome to implement though.
  
5) **Trusted Nodes with Proof of Code Ownership**

Develop a protocol for trusted nodes to provide contract states they are responsible for, along with a means to prove ownership of the contract's code. This approach could serve as an initial iteration since it appears more feasible than previous ones, while striking a good balance among various properties.

6) **Onchain Delegation**

Extend the previous idea by allowing code owners to delegate onchain the responsibility of indexing states to nodes they trust.
  
7) **Onchain Commitments**

Build upon the above concepts by having nodes commit onchain to the states of smart contracts they are concerned with.

8) **Commitments with Proofs**

Enhance the previous proposal by enabling nodes to verify each other to some extent. This verification may incorporate elements like proof of work or proof of stake in addition to commitments. While this approach seems promising to us, the ultimate solution remains uncertain.

