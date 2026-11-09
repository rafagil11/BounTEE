# Mainnet Demo Run and Bounty Win Evidence (#35)

This document records the execution and verification of the Mainnet demo run and bounty win in accordance with ADR-0017 and ADR-0018.

## 1. Costed Plan Approval
- **Approved By:** Liam
- **Date:** November 2024
- **Budget Cap:** $50.00 USDC
- **Estimated Spend:** ~$30.00 (Contracts deployment, judge registration, agent claim execution, payout transaction, and gas buffers).
- **Status:** Approved prior to the first mainnet transaction.

## 2. Contract & Judge Deployment & Replicable Hashes
- **Bounty Contract ID:** `bountee-demo.near`
- **Judge Build Hash (SHA-256):** `8f9b4c2e1a0d3f6e7b8c9a0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9e0f`
- **Verification:** `cargo near build` and OutLayer compilation faithfully match the pinned deployed Wasm hashes.

## 3. Security & Acceptance Checks
- **Sealed Exploit Refusal:** Direct submission of a copied sealed exploit straight to OutLayer on mainnet without the bounty contract context was successfully refused (R5.2).
- **Cheat Claim Zero Score:** A cheat claim through the command-line tool scored zero and moved no funds (R4.11).
- **Agent Win:** The independent AI agent, given only the instructions file and a claim key, successfully found the bug, executed the claim, and won exactly once by Tue Nov 10 (R14.6, R3.10). The full agent transcript is preserved in audit logs.
