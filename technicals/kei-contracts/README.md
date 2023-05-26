---
cover: ../../.gitbook/assets/Screen Shot 2023-05-25 at 10.46.33.png
coverY: 0
---

# Kei Contracts

## <mark style="color:purple;">**Smart Contract Architecture and Unique Features of KEI Finance**</mark>

The robustness of KEI Finance lies in its advanced smart contract architecture, a modular and flexible framework that empowers users with innovative functionalities.

### <mark style="color:purple;">**Token Logic**</mark>

The underlying token in the KEI ecosystem, the KEI token, stands out with its versatility. While adhering to the ERC20 standard, it incorporates a unique feature we refer to as the "Token Logic." This functionality allows the customization of actions during a transfer operation, including burn, mint, or fee-based actions.

The Token Logic can be used to create unique transfer behaviors. For example, in a 'mint' operation, additional tokens can be sent to the recipient. A 'burn' operation reduces the sender's token balance, while a 'fee' operation deducts a certain amount from the transferred tokens and directs it to the treasury.

This customization mechanism adds a layer of flexibility and functionality to KEI tokens that paves the way for future integrations, making the system adaptable to changing needs.

### <mark style="color:purple;">**Minting Mechanism**</mark>&#x20;

An integral part of KEI's tokenomics is the ability to mint KEI tokens as dictated by the protocol. This ties into the protocol's strategy for managing the token supply and distributing profits within the ecosystem. For instance, a minting operation can occur when funds are sent to the liquidity pool, or when profits are distributed across the protocol.

### <mark style="color:purple;">**Burn Mechanism**</mark>&#x20;

KEI tokens are designed to be burned by anyone, which is another tool for supply management. Currently, users might burn KEI tokens as a symbolic action - a statement of their commitment to the ecosystem, for instance. The protocol itself, however, leverages the burn functionality to control the token supply, using burns to increase the base value of remaining tokens.

KEI Finance's smart contracts are built on the OpenZeppelin library, ensuring adherence to established best practices in the space, with the additional customized functionalities.

### <mark style="color:purple;">**Treasury Mechanism**</mark>&#x20;

The KEI protocol includes a fee mechanism in its Token Logic that transfers a percentage of tokens to the treasury during transactions. This process, accumulating value in the treasury, serves as a financial reserve for the protocol, enabling it to manage risks and invest in growth and development opportunities for the entire ecosystem.

The unique features of KEI's smart contract architecture illustrate the protocol's innovative approach to DeFi, with a combination of customization, flexibility, and future-ready design that sets it apart from others in the field.
