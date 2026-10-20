<h1 align="center">Omeiza</h1>
<p align="center"><b>Web3 security researcher · Smart contract auditing · DeFi protocol analysis</b></p>
<p align="center"><i>I hunt for high-impact vulnerabilities in decentralized protocols — and I validate every finding with evidence, not vibes.</i></p>

<p align="center">
  <img src="https://img.shields.io/badge/Solidity-363636?logo=solidity&logoColor=white" />
  <img src="https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white" />
  <img src="https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white" />
  <img src="https://img.shields.io/badge/Foundry-1C1C1C" />
  <img src="https://img.shields.io/badge/Anchor-512BD4" />
  <img src="https://img.shields.io/badge/Ethereum-3C3C3D?logo=ethereum&logoColor=white" />
  <img src="https://img.shields.io/badge/Solana-9945FF?logo=solana&logoColor=white" />
</p>

<p align="center">
  <a href="https://github.com/JayJay64th"><img src="https://img.shields.io/badge/GitHub-@JayJay64th-181717?style=for-the-badge&logo=github" /></a>
  <a href="https://x.com/yourhandle"><img src="https://img.shields.io/badge/X-@yourhandle-000000?style=for-the-badge&logo=x" /></a>
  <a href="mailto:your@email.com"><img src="https://img.shields.io/badge/Email-your@email.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open%20to-Security%20research%20%26%20audit%20collabs-2ea44f?style=for-the-badge" />
</p>

I hunt for high-impact vulnerabilities in decentralized protocols — with an emphasis on fund-loss classes: accounting drift, access-control bypass, oracle manipulation, and cross-mechanism inconsistencies.

📌 I focus on DeFi protocol security, particularly where economic logic, state transitions, and access boundaries intersect.

---

## Focus

| Area | What I look at |
|---|---|
| DeFi lending / money markets | Interest accounting, liquidation, share/asset math, isolation modes |
| Perp & AMM design | Fee ledgers, PnL conservation, oracle integration, settlement |
| Launchpads | Token vesting logic, sale mechanics, allocation fairness, privileged release paths |
| Prediction markets | Settlement logic, oracle tampering, payout accounting, market resolution integrity |
| Cross-chain & bridges | Message replay, mint/burn parity, endpoint trust |
| Consensus-adjacent | Validator economics, slashing paths, finality assumptions |

**Stack:** Solidity · Rust (Anchor/Solana) · Go · Foundry · on-chain state forensics

---

## Methodology

**Manual, invariant-driven security auditing.**

**1. Scope & Threat Model**  
Establish the impact boundaries, identify trust assumptions and privileged actors, and define the invariants that must hold.

**2. Architecture & State Mapping**  
Trace entry points, authorization paths, cross-contract calls, and state transitions. Map who can change what, and under which conditions.

**3. Systematic Code Review**  
Review the codebase through three lenses:
- **Accounting:** Asset/share consistency, debt tracking, fee flows, and rounding.
- **Authorization:** Caller permissions, lifecycle checks, and inconsistencies across equivalent paths.
- **Trust boundaries:** External calls, oracles, user-controlled inputs, and transaction-level manipulation.

**4. Attack Enumeration**  
Challenge each relevant path with adversarial inputs, call sequences, transaction ordering, reentrancy, and boundary conditions. Trace the path from violated invariant to economic impact.

**5. Impact Validation**  
Require concrete evidence: a failing test, fork-based verification, or quantified execution analysis. Establish the attacker's cost, the victim's loss, and the conditions required for exploitation.

**6. Falsification & Variant Hunting**  
Reject hypotheses only when a specific safeguard or economic constraint explains why they fail. For confirmed issues, search equivalent functions and related code paths for variants before reporting.

---

## Toolkit

- Foundry (unit, invariant, fork tests)
- On-chain forensics (`eth_getLogs`, archive replay, bytecode decompile)
- Static analysis (Slither, custom grep packs)
- Exact-integer modeling before forking
- Manual cross-checks of state transitions and whitelist logic

---

## Selected work

### Findings
- **Contests** — Sherlock, Code4rena, HackenProof: **3 findings** across protocol attack surfaces and economic edge cases.
- Focus areas: **state drift, access control, oracle assumptions, liquidation logic**.
- Every finding validated by direct exploit modeling — a test, a forked-state query, or a priced trigger; no code-only suspicion ships.

### Tools & autonomous pipeline
- [web3-security-tools](https://github.com/JayJay64th/web3-security-tools)
- Custom tooling for **protocol recon, state diffing, invariant checks, and exploit validation**.
- Autonomous hunting pipeline: **target selection → state modeling → pattern sweep → exploit proof → closeout**.
- Supporting infrastructure: findings ledger, class-specific grep packs, exact-integer models, bytecode decompile when source is missing.

### Protocols built
- [protocols-built](https://github.com/JayJay64th/protocols-built)
- Protocol experiments, model-based stress tests, and attack-surface explorations built to validate assumptions and pressure-check economic invariants.

### Writeups
- [security-notes](https://github.com/JayJay64th/security-notes)
- Security notes, protocol breakdowns, and technical writeups covering **root cause analysis, exploit path validation, and mitigation thinking**.

---

## Currently

- Active on **Immunefi** and **private audit / bug bounty work**
- Building multi-pass hunt pipelines: recon → model → pattern sweep → closeout
- Open to protocol design review and high-signal audit collaborations

---

## Contact

- GitHub: [@JayJay64th](https://github.com/JayJay64th)
- X: [@yourhandle](https://x.com/yourhandle) — add in profile settings
- Email: your@email.com — add in profile settings

> No fake stats. No inflated totals. Only public repos and verified work are presented.

---

<p align="center">
  <sub>Responsible disclosure first. Public material reflects verified or already-public work only.</sub>
</p>
