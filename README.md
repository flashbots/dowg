# Decentralized Orderflow Working Group

## About

This repository is in progress and will host the work of the Decentralized Orderflow Working Group.

## Builders

Builders can register to receive orderflow from MEV-share matchmakers by submitting a PR to this repository. In the PR, they should add an entry to `registrations.json` with the following information:
* Their name as they would like it displayed.
* The RPC endpoint that matchakers should send bundles to.
* The API versions they support. Builders can find the complete set of bundle APIs [here](https://github.com/flashbots/mev-share/tree/main/specs/bundles) (version names are indicated by the file name). We recommend that builders upgrade to the latest version when new versions are released. For an example of how to integrate the new `mev_sendBundle` method (and in particular how to enforce validity conditions), you can reference the open-source [Flashbots MEV-Boost Block Builder](https://github.com/flashbots/builder/tree/mev-share).

In the PR description, Builders must attest that they agree to the Fair Market Principles outlined in `fair-market-principles.md`.

Note that registering does not guarantee that a builder will receive orderflow from any or all matchmakers. Matchmakers or users may choose to limit the set of builders that they share orderflow with by default or in general. The purpose of this registry is to signal intent, compatibility, and agreement with the principles. Builders could be removed or flagged if the MEV-share community determines that they have failed to uphold these principles.
