_This is a work in progress. If you have questions or suggestions about the fair market principles, please add an issue in this repository._

In order to receive bundles from MEV-share matchmakers, builders agree to the following principles. These principles are intended to ensure that builders act in a market-neutral way and don't use their privileged position to manipulate the auction to the detriment of the user.

- **Not sell or share bundles with external parties**. This includes actors like other builders and searchers. Bundles are shared with the builder and the builder alone.
- **Not break the atomicity of bundles**. This means that either all transactions in a bundle are included in the intended order with no other transactions inserted between them, or no transactions from that bundle are included. Where two bundles' MEV extraction is non-conflicting, it is acceptable to insert transactions from one bundle into another if it does not result in worse execution for users.
- **Respect the privacy of bundles, including failed-trade privacy**. This means not retaining any sensitive data about bundles in internal systems and not publicly sharing information about bundles that were not included on chain.
- **Correctly implement validity conditions**. This means transferring the correct payment to the correct addresses for bundles that have refunds.
- **Provide optimal execution to users**. Builders should not take actions that negatively impact the execution of the bundle (for example, effective price or refund amount). Specifically if a bundle for user X is included with prefix P, there should be no other bundle for tx X that more profitable with prefix P.
- **Be transparent about how orderflow is processed**. Bundle merging algorithms used by the builder are publicly documented and plainly expressed to users (excluding custom optimizations or proprietary techniques). Builders also agree to share non-sensitive data for public analysis, monitoring, and tracking purposes.

Builders who register in `builder-registrations` are committed to uphold these principles. 
