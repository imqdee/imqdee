# Senior Smart-Contract & DeFi Protocol Engineer

8+ years building software • 4+ years building in crypto • **Stake DAO** core maintainer • ex-**Ledger**

I design, build, and secure high-value on-chain systems. My work focuses on solving complex liquidity, pricing, and orchestration challenges in DeFi.

## Core Expertise

- **Smart Contracts:** Solidity, Assembly/Yul, Vyper, with deep Foundry experience
- **DeFi systems:** yield vaults, liquid lockers, lending/borrowing, ve-tokenomics, oracles, AMMs, yield-bearing strategies, cross-chain bridging...
- **Standards & interoperability:** ERC-20/4626/5115/7540/3156...
- **Protocol integrations:** Curve, Morpho, Pendle, Convex, Chainlink, LayerZero, Safe...
- **Account abstraction:** ERC-4337/7702/6900/5792 and on-chain passkeys

## Project Highlights

All of the following contracts have been deployed and battle-tested in production. As the lead architect and maintainer, I’ve designed and built these core on-chain systems from the ground up.

### 1. Universal Curve LP Oracles

Universal, flash-resistant, market-based oracle for Curve LP tokens that lending markets can rely on. Built a hop-chain architecture that prices any pool coin into USD, clamps on Curve’s EMA, denominates the price into the quote asset you want, and scales outputs for the needs of your venues. Ships with adapters, factory wiring, and a full curator playbook for safe listings.

[Implementations & Documentation](https://github.com/stake-dao/contracts-monorepo/tree/606bc4b94f7020b43078313274bce071bb688c7a/packages/periphery/src/lending/oracles) • [Docs](https://github.com/stake-dao/contracts-monorepo/blob/606bc4b94f7020b43078313274bce071bb688c7a/packages/periphery/src/lending/CURATORS.md) • Audited • Granted by Curve and Morpho

### 2. Reward-Preserving Lending Collateral

ERC20 wrapper that turns Stake DAO LP tokens into lending collateral without sacrificing rewards. Users can deposit existing vault shares or underlying LP, auto-claim main + extra rewards on every flow, and enforce authorized-only transfers to the lending protocol. Liquidation claims re-sync internal balances so seized collateral maps to the right vault shares, and operator permissions let routers batch deposits/claims safely.

[View Contract](https://github.com/stake-dao/contracts-monorepo/blob/606bc4b94f7020b43078313274bce071bb688c7a/packages/periphery/src/lending/wrappers/StrategyWrapper.sol) • [Docs](https://github.com/stake-dao/contracts-monorepo/blob/606bc4b94f7020b43078313274bce071bb688c7a/packages/periphery/src/lending/README.md) •Audited • Granted Morpho

### 3. Stateless Modular Router

A minimalist, secure, and composable stateless router with 10+ plug-and-play modules, designed as the single execution entry point for the entire Stake DAO ecosystem. Enforces a Permit2-only flow so users never grant unsafe approvals.

[Implementation & Documentation](https://github.com/stake-dao/contracts-monorepo/tree/606bc4b94f7020b43078313274bce071bb688c7a/packages/periphery/src/router) • In production on 7+ networks

### 4. Streaming Autocompounded Vault

ERC-4626 vault with streaming rewards that roll forward cleanly when new emissions are added. Automatically compounds rewards into principal and exposes predictable reward calendars.

[View Contract](https://github.com/stake-dao/contracts-monorepo/blob/606bc4b94f7020b43078313274bce071bb688c7a/packages/lockers/src/AutocompoundedVault.sol)

### 5. Advanced MEV-Resistant Reward Accumulators

A suite of contracts designed to manage complex reward flows for liquid lockers (Balancer, Pendle, etc.).

- **Delegable Accumulator:** A `veBoost` sharing mechanism that separates economic rights from governance rights. It allows the protocol to boost rewards for users based on their veToken balances without requiring them to transfer custody of their governance tokens.
- **Dripping Accumulator:** Solves the "Sandwich Attack" problem on reward claims. Instead of distributing lump-sum rewards (which incentivize MEV bots to front-run claims), this contract receives rewards and streams them linearly over time ("dripping"), protecting passive stakers.

[View Delegable Variant](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/lockers/src/AccumulatorDelegable.sol) • [View Dripping Variant](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/lockers/src/AccumulatorDripping.sol)

## Contact

Open to discussing smart contract engineering, high-assurance DeFi architecture, and technical advisory.

Twitter/X → [@imqdee](https://x.com/imqdee) _(DMs open)_
