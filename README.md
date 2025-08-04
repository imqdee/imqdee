**Senior Smart-Contract & DeFi Protocol Engineer**

8+ years building software • 4+ years building in crypto (long-time DeFi user) • [Stake DAO](https://www.stakedao.org/) (>$300M TVL) core maintainer • ex-[Ledger](https://www.ledger.com/)

I design, build, and secure high-value on-chain systems.

## Core Expertise

- **Smart-contract** — Solidity, Vyper, forge/cast/anvil/chisel
- **DeFi mechanics** — yield-bearing vaults, liquid lockers, ve-environments (gauge/boosting/integrals), bond stripping, lending/borrowing, yield strategies, oracles, bridges
- **ERC standards** — ERC-20, ERC-4626, ERC-5115 (SY Token), ERC-7540 (async vaults), ERC-3156 (flash loans), custom extensions
- **Account Abstraction** — ERC-4337, ERC-7702, ERC-6900, ERC-5792, on-chain passkey verification
- **Protocol integrations** — Stake DAO, Curve, Convex, Pendle, Morpho, Chainlink, LayerZero, Safe
- **Tooling & infra** — wagmi/viem, OpenZeppelin, solady, solmate, subgraphs, CI/CD, static analysis (Slither, Foundry fuzzing), TypeScript/Node.js, Vercel

## Recent Contracts I've Worked On

<sub>This table tracks a rotating sample of my most recent on-chain work; it is updated as new code ships.</sub>

| Contract                 | What it does                                                                                                                                                                                                                                                                                                   | Source                                                                                                                                                                      |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Curve Oracles**        | Production-ready oracles for Curve LP tokens with flexible hop-chain pricing and Morpho Blue compatibility. Features EMA-based conservative pricing, and plug-and-play integration with lending protocols. Handles any token0→USD conversion path via configurable Chainlink feed chains.                      | [_link_](https://github.com/stake-dao/contracts-monorepo/tree/2f11d737bfa9dc705207aa33e9cffe3e699eaeb6/packages/strategies/src/integrations/curve/oracles)                  |
| **Stake DAO Wrapper**    | Production-ready ERC20 wrapper for Stake DAO RewardVault shares, allowing them to be used as collateral on a lending protocol while preserving yield.                                                                                                                                                          | [_link_](https://github.com/stake-dao/contracts-monorepo/blob/987d25d3c37124c40c5b9422b05cc12522201ffd/packages/strategies/src/wrappers/StrategyWrapper.sol)                 |
| **LockerPreLaunch**      | Escrow contract allowing early deposits into upcoming Stake DAO lockers; accumulates rewards and mints shares once the main locker goes live. Used for the integration of **Yieldnest**.                                                                                                                       | [_link_](https://github.com/stake-dao/contracts-monorepo/blob/7cdc94ac0d05bba239b275244ecaa0ef897875fe/packages/lockers/src/LockerPreLaunch.sol)                            |
| **AutocompoundedVault**  | ERC-4626 vault that auto-harvests and compounds yield back into principal, exposing a simple share token to depositors. Used for the integration of **Yieldnest**.                                                                                                                                             | [_link_](https://github.com/stake-dao/contracts-monorepo/blob/7cdc94ac0d05bba239b275244ecaa0ef897875fe/packages/lockers/src/AutocompoundedVault.sol)                        |
| **AccumulatorDelegable** | Accumulator variant that manages and distributes rewards to a delegation contract using the veBoost mechanism. Enable flexible reward sharing based on veToken balances and a configurable multiplier, enhancing distribution without transferring governance rights. Used for the integration of **Balancer** | [_link_](https://github.com/stake-dao/contracts-monorepo/blob/7cdc94ac0d05bba239b275244ecaa0ef897875fe/packages/lockers/src/AccumulatorDelegable.sol)                       |
| **AccumulatorDripping**  | Accumulator variant that streams ("drips") accrued rewards over time to mitigate MEV and sudden dump risk. Used for the integration of **Pendle**.                                                                                                                                                             | [_link_](https://github.com/stake-dao/contracts-monorepo/blob/7cdc94ac0d05bba239b275244ecaa0ef897875fe/packages/lockers/src/AccumulatorDripping.sol)                        |
| **MorphoMarketFactory**  | Factory that deploys Curve-based lending markets on **Morpho** Blue, seeds initial liquidity, and ensures deterministic healthy positions at launch.                                                                                                                                                           | [_link_](https://github.com/stake-dao/contracts-monorepo/blob/9a4c9de69bee6b7286696bc8c1a56182a06d565f/packages/strategies/src/integrations/morpho/MorphoMarketFactory.sol) |

## Contact

Open to discussing smart-contract engineering in DeFi, consulting, or technical advisory.

Twitter → [@imqdee](https://x.com/imqdee) _(DM open)_<br>
