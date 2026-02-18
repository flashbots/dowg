# Decentralized Orderflow Working Group

## About

This repository is in progress and will host the work of the Decentralized Orderflow Working Group.

## Builders

### Criteria for receiving orderflow

To be eligible to receive orderflow, a builder must:
* Build ≥2% of canonical Ethereum blocks over the trailing 60 days
* Provide a real-time communication channel for technical coordination
* Commit to the Flashbots Fair Market Principles

Builders may be suspended if they:
* Fall below 2% block share over the trailing 30 days; or
* Violate the Fair Market Principles; or
* Experience documented technical instability materially affecting inclusion reliability.

In rare cases where these thresholds would impact transaction inclusion for users, Flashbots may temporarily adjust the multiplexing criteria. Any adjustments will be documented and applied equally across all builders.

### Registering to receive orderflow

Builders can register to receive orderflow by submitting a PR to this repository. In the PR, they should add an entry to `registrations.json` with the following information:
* Their name as they would like it displayed.
* The RPC endpoint that matchakers should send bundles to.
* The API versions they support. Builders can find the complete set of bundle APIs [here](https://github.com/flashbots/mev-share/tree/main/specs/bundles) (version names are indicated by the file name). We recommend that builders upgrade to the latest version when new versions are released. For an example of how to integrate the new `mev_sendBundle` method (and in particular how to enforce validity conditions), you can reference the open-source [Flashbots MEV-Boost Block Builder](https://github.com/flashbots/builder/tree/mev-share).

In the PR description, Builders must attest that they agree to the Fair Market Principles outlined in `fair-market-principles.md`.

Note that registering does not guarantee that a builder will receive orderflow from any or all matchmakers. Matchmakers or users may choose to limit the set of builders that they share orderflow with by default or in general. The purpose of this registry is to signal intent, compatibility, and agreement with the principles. Builders could be removed or flagged if the MEV-share community determines that they have failed to uphold these principles.
