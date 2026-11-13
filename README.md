# Market Microstructure & Dealer Plumbing
![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-blue.svg)

**Technical Notes & Practitioner Reference (41 Pages)**  
**Author:** Amir Ghanbariha — *Electronic Trading & Dealing Infrastructure Software Engineer*

📄 **[Download / Read Full PDF Monograph (v3)](./Market-Microstructure-and-Dealer-Plumbing-Amir-Ghanbariha.pdf)**

---

### Overview
A resting quote is a free option written to the market, and every rule, spread, skew, and limit in an electronic venue exists to price or avoid that option. 

This 41-page practitioner reference bridges formal market microstructure models with the low-level engineering and risk arithmetic of multi-tier electronic trading infrastructure (CLOB matching engines, FIX 4.4 connectivity bridges, LP aggregation, markout analytics, and dealing-desk risk engines).

### Key Contents
* **Part I — Foundational Microstructure & Applied Cases (§1–§8):**
  * Price-time FIFO & pro-rata matching engine invariants, L3 queue dynamics, and order types.
  * Spread decomposition (Roll, Glosten–Harris) and multi-horizon taker markout curves $M_\tau = q(m_\tau - m_0)$.
  * Adverse selection (Glosten–Milgrom, Kyle's $\lambda$) and stochastic inventory skew (Avellaneda–Stoikov reservation price & optimal warehouse bounds $q^*$).
  * Case studies: Liquidity vacuums & stale-quote pick-offs during NFP, perpetual-futures skew balancing, and non-predictive toxicity routing pipelines (`ASOF JOIN` + Spearman rank persistence).
* **Part II — Multi-Tier Plumbing, Latency & Desk Arithmetic (§9–§25):**
  * Principal vs. agency counterparty chains, back-to-back STP/FIX session mechanics (`35=D`, `35=8`, sequence gap recovery), and PoP/PB credit layers.
  * Multi-layer internalization timelines ($10\text{--}100\,\mu\text{s}$ last-look windows to CRB factor netting).
  * The 7-band horizon ladder and the 3-loop hardware reflex arc (FPGA gates at $100\text{--}500\,\text{ns}$, kernel-bypass CPU via Onload/DPDK, and eBPF per-session TCP retransmit forensics).
  * Multilateral CLOB prices vs. bilateral marks, price discovery (Hasbrouck information shares), execution slicing (Almgren–Chriss, square-root impact law), CIP tom-next swap engines, and live EWMA/Cholesky Book VaR.
* **Part III — Formula Sheet & Verification Suite (§26–§27 & Appendices):**
  * 25 closed-form microstructure and desk-risk equations, a 12-part empirical verification suite, dual-ledger simulator invariants, and 10 stylized facts of tiered markets.
