# Senior Smart-Contract & DeFi Protocol Engineer

8+ years building software • 4+ years building in crypto • **Stake DAO** core maintainer • ex-**Ledger**

I design, build, and secure high-value on-chain systems. My work focuses on solving complex liquidity, pricing, and orchestration challenges in DeFi.

## Core Expertise

- **Smart Contracts:** Solidity, Assembly/Yul, Vyper, with deep Foundry experience
- **DeFi systems:** yield vaults, liquid lockers, lending/borrowing, ve-tokenomics, oracles, AMMs, yield-bearing strategies, cross-chain bridging...
- **Standards & interoperability:** ERC-20/4626/5115/7540/3156...
- **Protocol integrations:** Curve, Morpho, Pendle, Convex, Chainlink, LayerZero, Safe...
- **Account abstraction:** ERC-4337/7702/6900/5792 and on-chain passkeys

## Selected Work

I architect and maintain core protocol infrastructure. Below are highlights of the recent production systems I have designed and developed.

### 1. Universal Curve LP Oracles

**The Standard for Pricing Curve LP Tokens**
Universal, flash-resistant, market-based oracle for Curve LP tokens that lending markets can rely on. Built a hop-chain architecture that prices any pool coin into USD, clamps on Curve’s EMA, denominates the price into the quote asset you want, and scales outputs for the needs of your venues. Ships with adapters, factory wiring, and a full curator playbook for safe listings.

[**Implementations & Documentation**](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/periphery/src/lending)

### 2. Stateless Modular Router

**Permit2-Native Protocol Entrypoint**
A minimalist, secure, and composable stateless router designed to act as the single execution entry point for the entire Stake DAO ecosystem. Enforces a Permit2-only flow so users never grant unsafe approvals.

[**Implementation & Documentation**](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/periphery/src/router)

### 3. Autocompounded Vault (ERC-4626)

**Streaming Yield Architecture**
ERC-4626 vault with streaming rewards that roll forward cleanly when new emissions are added. Automatically compounds rewards into principal and exposes predictable reward calendars.

[**View Contract**](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/lockers/src/AutocompoundedVault.sol)

### 4. Pre-Launch Locker

**Trust-Minimized Escrow State Machine**
Pre-launch locker that mints sdTokens 1:1 on deposit, optionally stakes into gauges, and bridges users into the final locker once governance flips the switch. Includes a real safety net: refund path on cancellation and a force-cancel timer that only starts when the first deposit is received.

[**View Contract**](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/lockers/src/LockerPreLaunch.sol)

### 5. Advanced Reward Accumulators

**MEV-Resistant Distribution Engines**
A suite of contracts designed to manage complex reward flows for liquid lockers (Balancer, Pendle, etc.).

- **Delegable Accumulator:** A `veBoost` sharing mechanism that separates economic rights from governance rights. It allows the protocol to boost rewards for users based on their veToken balances without requiring them to transfer custody of their governance tokens.
- **Dripping Accumulator:** Solves the "Sandwich Attack" problem on reward claims. Instead of distributing lump-sum rewards (which incentivize MEV bots to front-run claims), this contract receives rewards and streams them linearly over time ("dripping"), protecting passive stakers.

[**View Delegable**](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/lockers/src/AccumulatorDelegable.sol) • [**View Dripping**](https://github.com/stake-dao/contracts-monorepo/tree/af51de3b94e47824f551b43a141068eaea1d6b53/packages/lockers/src/AccumulatorDripping.sol)

## Contact

Open to discussing smart contract engineering, high-assurance DeFi architecture, and technical advisory.

Twitter/X → [@imqdee](https://x.com/imqdee) _(DMs open)_
