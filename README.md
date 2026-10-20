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
| Cross-chain & bridges | Message replay, mint/burn parity, endpoint trust |
| Consensus-adjacent | Validator economics, slashing paths, finality assumptions |

**Stack:** Solidity · Rust (Anchor/Solana) · Go · Foundry · on-chain state forensics

---

## Methodology

Security work is evidence work:

- Scope first — authorized programs only; impact bar driven by the protocol’s own rules.
- Comparison over guesswork — same economic operation via alternate entry points, diffed field by field.
- Proof before claim — every finding ships with a test, state query, or priced trigger.
- Ledger discipline — every lead tracked; kills record what protected the system.
- Variant search on confirm — one finding is often a pattern; sweep the codebase and audit corpus.

---

## Toolkit

- Foundry (unit, invariant, fork tests)
- On-chain forensics (`eth_getLogs`, archive replay, bytecode decompile)
- Static analysis (Slither, custom grep packs)
- Exact-integer modeling before forking
- Manual cross-checks of state transitions and whitelist logic

---

## Selected work

### Bug bounty findings
- Sherlock
- Code4rena
- HackenProof

### Contest findings
- 3 contest findings across protocol attack surfaces and economic edge cases.
- Focus on state drift, access control, oracle assumptions, and liquidation logic.
- Each finding was validated through direct exploit modeling and proof-oriented reproduction.

### Tools built + autonomous pipeline
- Custom tooling for protocol recon, state diffing, invariant checks, and exploit validation.
- Autonomous hunting pipeline: target selection → state-modeling → pattern sweep → exploit proof → closeout.

### Writeups
- Security notes, protocol breakdowns, and technical writeups covering root cause analysis, exploit path validation, and mitigation thinking.

---

## Currently

- Active on Immunefi, Code4rena / Codehawks, HackenProof, and Sherlock
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
