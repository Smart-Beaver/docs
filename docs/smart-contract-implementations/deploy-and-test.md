# How to deploy and test contracts

To test our contracts locally you can follow these simple steps:

1. Build contract: `cargo contract build --release --features "contract"`
2. Run local substrate node: `substrate-contracts-node`
3. Deploy your contract using contracts-ui: https://contracts-ui.substrate.io/
    1. Make sure to select "Local Node" in the upper left corner

The easiest way to call contract functions is to use the same `contracts-ui` wep app.

For more detailed tutorial to get you onboarded on ink! development look here: [https://use.ink/getting-started/setup](https://use.ink/getting-started/setup)

