# Decentralized Orderflow Working Group

## About

This repository is in progress and will host the work of the Decentralized Orderflow Working Group.

## Builders

Builders can register to receive orderflow from MEV-share matchmakers by submitting a PR to add their name and RPC to `builder-registrations.json`. In the PR, Builders must attest that they agree to the Fair Market Principles outlined in `fair-market-principles.md`. Builders will eventually need to accept bundles in the format specified by [`mev_sendBundle`](https://github.com/flashbots/mev-share/tree/main/specs/mev_sendBundle.md). For an example of how to integrate this new bundle format (and in particular how to enforce validity conditions), you can reference the open-source [Flashbots MEV-Boost Block Builder](https://github.com/flashbots/builder/tree/mev-share).

Note that registering does not guarantee that a builder will receive orderflow from any or all matchmakers. Matchmakers or users may choose to limit the set of builders that they share orderflow with by default or in general. The purpose of this registry is to signal intent, compatibility, and agreement with the principles. Builders could be removed or flagged if the MEV-share community determines that they have failed to uphold these principles.
