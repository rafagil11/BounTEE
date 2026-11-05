# ADR-0018: Mainnet Demo Execution Plan

## Context
To satisfy the demo bounty requirements, we are deploying BounTEE to mainnet. The total budget is $50 USD. We must ensure the demo is secure, reproducible, and verifiable.

## Plan
1. **Deployment**: Deploy bounty contract and judge to NEAR mainnet. Verify hashes match local build (R15.2).
2. **Funding**: The demo vault will be funded with real USDC only minutes before the exploit claim to minimize exposure.
3. **Security Checks**:
   - Sealed exploit sent to OutLayer: Must be refused (R5.2).
   - Cheat claim via CLI: Must score zero and move no funds (R4.11).
4. **Execution**: An independent AI agent will be provided with the instructions and a claim key to find the bug and win the bounty.
5. **Budget**: Total transaction costs must remain under $50.

## Consequences
- All mainnet transactions require explicit approval from Liam.
- The demo run is recorded for the final video evidence.
- The bounty pays exactly once.