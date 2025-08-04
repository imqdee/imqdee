# Senior Smart-Contract & DeFi Protocol Engineer

8+ years building software · 4+ years in crypto · **Stake DAO** core maintainer · ex-**Ledger** (Blockchain R&D)

From Ledger's passkey-powered AA wallets to Stake DAO's DeFi infrastructure, I architect systems that handle real money at scale. I specialize in the hard problems: oracle design, yield generation, and tokenomics migrations.

**$200M+ TVL secured** · **5 audits (Trust, Pashov, Omniscia)** · **2 grants** · **~200k DeFi LOC** · **ETHGlobal NY '23 Winner**

## Core Expertise

- **Smart Contracts:** Solidity, Yul, Vyper · Foundry (unit, fork, fuzz, invariant testing) · ERC-20/1155/2612/3156/4626/5115/7540...
- **DeFi Primitives:** Yield vaults, liquid lockers, ve/vl-tokenomics, lending markets, oracles, gauge systems, reward distribution...
- **Protocol Integrations:** Curve, Morpho, Pendle, Yearn, Chainlink, LayerZero, CCIP, Safe, Succinct, Flashbots...
- **Background:** Fullstack web engineering · Language agnostic · Quick to adopt new stacks

## Featured Work

Production systems I recently architected and built from the ground up. All deployed and battle-tested.

### Curve LP Oracle

First universal, flash-resistant oracle for pricing Curve LP tokens in lending markets. Hop-chain architecture prices any pool coin into any quote asset, supporting both Stableswap and Cryptoswap pools. Powers 10+ Morpho lending markets.

[View Documentation](https://github.com/stake-dao/contracts-monorepo/blob/main/packages/periphery/src/lending/CURATORS.md) · [View Contract](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/periphery/src/lending/oracles) · `Granted by Curve`

### Yield-Preserving Lending Collateral

ERC-20 wrapper that turns yield vault positions into lending collateral without sacrificing rewards. Users keep earning while borrowing. Handles reward accounting through deposits, withdrawals, and liquidations. Unlocked Stake DAO's lending product line.

[View Documentation](https://github.com/stake-dao/contracts-monorepo/blob/main/packages/periphery/src/lending/README.md) · [View Project](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/periphery/src/lending/wrappers) · `Granted by Morpho`

### vlSDT Tokenomics Migration

Redesigned Stake DAO's governance system, replacing Curve's decaying vote-escrow model with flat voting power and flexible unstaking. Multi-contract architecture handling migration paths, fee distribution, and boost delegation while maintaining backwards compatibility during transition. Migrating $7M+ SDT.

[View Project](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/vlsdt)

### Votemarket ZK Verifier

Full-stack ZK architecture replacing expensive on-chain Merkle-Patricia Trie verification with constant-size proofs. Rust circuit (SP1) verifies storage proofs off-chain while Solidity contract validates and commits data on-chain. Achieves 45x calldata reduction for batch claims.

[View Circuit (Rust)](https://github.com/stake-dao/votemarket-sp1) · [View Verifier (Solidity)](https://github.com/stake-dao/contracts-monorepo/blob/main/packages/votemarket/src/verifiers/ZKVerifier.sol)

### Universal Composable Router

Modular, stateless entrypoint for the entire Stake DAO ecosystem. 10+ plug-and-play modules covering deposits, withdrawals, migrations, claims, and zaps. Permit2-only flow eliminates approval phishing vectors.

[View Project](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/periphery/src/router) · Deployed on 7+ networks

## More Work

- [**Streaming Autocompounded Vault**](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/lockers/src/AutocompoundedVault.sol) · ERC-4626 vault with linear reward streaming and automatic rollover on new emissions
- [**Dripping Accumulator**](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/lockers/src/AccumulatorDripping.sol) · MEV-resistant reward distribution via weekly dripping instead of lump-sum payouts
- [**Delegable Accumulator**](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/lockers/src/AccumulatorDelegable.sol) · veBoost sharing mechanism separating economic rights from governance rights
- [**Multi-Token Delegable Accumulator**](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/lockers/src/AccumulatorDelegableMultiToken.sol) · Multi-token variant supporting flexible fee charging across different reward types
- [**Pendle Accumulator**](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/lockers/src/integrations/pendle/Accumulator.sol) · Reward distribution for Pendle liquid locker with dripping and fee splitting
- [**PreLaunch Locker**](https://github.com/stake-dao/contracts-monorepo/tree/main/packages/lockers/src/LockerPreLaunch.sol) · State-machine token locking before protocol deployment with built-in refund mechanism
- **Liquidation Bot & Indexer** · Closed-source infrastructure for automated liquidations and on-chain data indexing

## Open Source Tools

The tools listed here are open-source tools that I primarily developed for my daily needs.

- [**wtree**](https://github.com/imqdee/wtree) · Git worktree automation with lifecycle hooks
- [**stargate**](https://github.com/imqdee/stargate) · Blockchain network switcher CLI for the Foundry suite
- [**xplorer**](https://github.com/imqdee/xplorer) · Etherscan API CLI wrapper
- [**serve-it**](https://github.com/imqdee/serve-it) · Serve a single local file over HTTP in one command
- [**raycast-zerion**](https://github.com/imqdee/raycast-zerion) · Browse Zerion portfolios via Raycast
- [**raycast-evm-toolkit**](https://github.com/imqdee/raycast-evm-toolkit) · A Raycast extension for Ethereum power users

## Availability

I am open to full-time roles, part-time roles, and technical advisory engagements.

Twitter/X · [@imqdee](https://x.com/imqdee)
Email · [contact@push20labs.com](mailto:contact@push20labs.com)
