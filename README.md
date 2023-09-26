# Solving Back-To-Genesis | BTG Proposals (BTGP)

This is a repo that acts as a public forum to explore ideas to solve the back to genesis problem, especially in the context of the RUN library on BitcoinSV

For a summary of this problem, check out this video by Joshua Henslee (@jdh7190): https://www.youtube.com/watch?v=hT86Y9wnNkY

The focus is not on implementing, but on exploring solutions and forming one common vision (or many) around a good solution that can be implemented later on.

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
  Title: BTGPs Guidelines
  Authors: Zhell <zhell1057@gmail.com>
  Created: 2011-09-19
  ```

Then each BTGP should have the following parts:

- Header - such as the example provided above with title, authors, etc. Feel free to add more if you think they would improve the process.
- Abstract - short (<200words) description of the proposal
- Motivation - explain why the existing protocols and proposals are inadequate and yours is better or at least interesting to consider
- Specification - explain in details how your idea would work from a technical point of view
- Economics - explain in details how the economics would work to guarantee long term success of each actors in the protocol
- Backwards Compatibility - Explain if you are going to break backward compatibility and the severity of it. Explain eventual transition processes that could be implemented to make the migration more flawless

# Copyrights / public domain

Note that submitting a BTGP means you automatically put it as public domain use.

