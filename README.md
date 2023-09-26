# Solving Back-To-Genesis | BTG Proposals (BTGP)

This is a repo that acts as a public forum to explore ideas to solve the back to genesis problem, especially in the context of the RUN library on BitcoinSV (cf https://Runcraft.io)

The focus is not on implementing, but on exploring solutions and forming one common vision (or many) around a good solution that can be implemented later on.

# Summary of the back-to-genesis problem

For a summary of the problem, check out this video by Joshua Henslee (@jdh7190): https://www.youtube.com/watch?v=hT86Y9wnNkY

Here is a summary of the problem in the context of the RUN library, which adds a layer2 smartcontract virtual machine on top of the back-to-genesis problem.

1) smartcontracts are executed in a virtual machine that acts as a second layer
2) the only way to sync/validate the latest state of a contract is to process the entire chain up to its genesis (hence the "back to genesis")
3) as contracts interact with each other, they become reliant on indexing each other, which can quickly grow the indexation cost exponentially 
4) the (bad) current solution is to prevent interoperability and only allowing manually white-listed contracts to interacts with your contracts
5) we need a solution that doesn't compromise interoperability as much, while preventing exploding indexing costs, especially for newcomers that cannot pay to run a pricy indexing node


# How to contribute

For a starter, read the different proposals in this repo.

You can contribute by opening issues for discussion or by opening new proposals with pull-requests.

You can open a new pull-request to contribute to a proposal or to create a new one if you have an idea that hasn't be proposed yet. See the section on Formatting below.

Eventually if a few main different solutions emerge, we will organize each in its own folder with a summary in this README file.

# Formatting

(this is roughly inspired by the concept of bitcoin BIPs as defined here: https://github.com/bitcoin/bips)

It is highly recommended that a single BTGP contain a single key proposal or new idea. The more focused the BTGP, the more successful it tends to be.

```txt
  BTGP: 1
  Title: first BTGP proposal
  Authors: Zhell <zhell1057@gmail.com>
  Created: 2023-09-26
  ```

Then each BTGP should have the following parts:

- **Header** - such as the example provided above with title, authors, etc. Feel free to add more if you think they would improve the process.
- **Abstract** - short (<200words) description of the proposal
- **Motivation** - explain why the existing protocols and proposals are inadequate and yours is better or at least interesting to consider
- **Specification** - explain in details how your idea would work from a technical point of view
- **Economics** - explain in details how the economics would work to guarantee long term success of each actors in the protocol
- **Backward Compatibility** - Explain if you are going to break backward compatibility and the severity of it. Explain eventual transition processes that could be implemented to make the migration more flawless

# Copyrights / public domain

Note that submitting a BTGP means you automatically put it as public domain use.

