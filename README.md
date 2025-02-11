# Solana Arbitrage Bot
This arbitrage bot implements advanced strategies for detecting and executing profitable trading opportunities across multiple Solana DEXs including Raydium, Orca (Whirlpool), Meteora, and Jupiter, with optional integration for Jito-MEV. Visulize about logic and architecture diagram.

# 👋 Contact Me

### 
Telegram: https://t.me/earthzeta
###
<div style={{display : flex ; justify-content : space-evenly}}> 
    <a href="https://t.me/earthzeta" target="_blank"><img alt="Telegram"
        src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/></a>
    <a href="https://discordapp.com/users/339619501081362432" target="_blank"><img alt="Discord"
        src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white"/></a>
</div>

#### Feel free to contact me if you need the full version.

# Solana Arbitrage Bot Architecture

## On-Chain Arbitrage Limitations

Important note: On-chain arbitrage programs face several limitations and risks:

1. **MEV Competition**
   - Searchers and validators can front-run transactions
   - Transaction ordering can be manipulated
   - Limited control over execution timing

2. **Technical Constraints**
   - Compute unit limitations for complex calculations
   - Transaction size limits for multi-hop trades
   - Higher latency compared to off-chain solutions

3. **Recommended Approach**
   - Use off-chain arbitrage detection
   - Submit transactions through MEV-aware RPC providers
   - Consider integrating with Jito-MEV for better execution

4. **Alternative Architecture**
   ```mermaid
   graph TD
       A[Off-chain Monitor] --> B[Price Analysis]
       B --> C[Opportunity Detection]
       C --> D[Transaction Builder]
       D --> E[MEV-aware RPC]
       E --> F[Validator Network]
   ```

The original implementation should be considered as educational material rather than a production-ready solution. For real-world arbitrage:

- Use off-chain monitoring and calculations
- Integrate with MEV-aware infrastructure
- Consider validator relationships for better transaction placement
- Implement proper slippage and risk management

# Overview

## Folders description
- `offchain/`: off-chain arbitrage bot code 
- `swap/`: on-chain swap program
- `pools/`: dex pool metadata
- `onchain/`: analysis of other arbitrage swaps
- `mainnet/`: fork mainnet account states to test swap input/output estimates

## Current version
This is primary version, not advanced. To get more efficient arbitragy, you need to get advanced version

## Current version dexs supported 
- serum 
- aldrin 
- saber 
- mercurial 
- orca 

## Advanced version dexs supported
- raydium
- meteora
- serum 
- aldrin 
- saber 
- mercurial 
- orca

# Contributing
We welcome contributions! Please submit a pull request or open an issue to discuss any changes.