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

Manual auditing, in the order I actually work:

1. Scope & threat model  
Read the program rules and impact bar first. Identify who can call what, who trusts whom, and where value sits. Write the invariants before looking for bugs — if you can't state what must always be true, you can't spot what breaks it.

2. Architecture pass  
Map every entry point (external, admin, callback, cross-contract) to the state it mutates. Build the actor matrix: for each function, ask who is allowed to reach this, and what are they allowed to affect. Most real bugs live in the gap between intended and enforced authorization.

3. Line-by-line review  
Three lenses, repeated across the codebase:

Accounting — do the numbers balance? Shares vs assets, supply vs debt, fees vs revenue, rounding direction on every mul/div.  
Access control — does every state change bind to the right caller, the right inputs, and the right lifecycle phase? Check equivalent entry points side by side for asymmetric checks.  
Trust boundaries — every external call, oracle read, and user-supplied parameter: what happens if it lies, reverts, returns garbage, or is manipulated in the same transaction?

4. Attack enumeration  
For each function, enumerate the abuse cases: who loses money, how much, and what does the attacker pay? Walk the happy path, then the hostile path — front-run it, re-enter it, batch it, call it out of order, call it with zero/empty/max values, call it from a contract instead of an EOA.

5. Proof before report  
Every candidate gets a concrete demonstration: a failing test, a forked-state query, or a priced calculation with numbers. If impact can't be shown with the attacker's profit and the victim's loss spelled out, it isn't ready to be a finding.

6. Kill or confirm  
A lead dies only when you can name the specific check, invariant, or economic force that stops it — and you record that protection, because it's usually the answer to the next hypothesis too. Confirmed findings get swept for variants elsewhere in the codebase before they're written up.

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
