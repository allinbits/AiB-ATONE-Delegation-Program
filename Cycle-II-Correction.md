# Cycle II Correction — redelegation of 8 allocations

> [!NOTE]
> **Executed on 10 August 2026.** This correction to the Cycle II allocation recorded in
> [Delegations-Cycle-II-20-November-2025.md](./Delegations-Cycle-II-20-November-2025.md)
> was broadcast and included on chain.
>
> | | |
> |---|---|
> | Transaction | [`750AC9C7…E69D4E9`](https://www.mintscan.io/atomone/tx/750AC9C7C6C2834A9AE7B33A852CB72A4C4CCE0724314A99CF9F3B199E69D4E9) |
> | Block height | 9836088 |
> | Timestamp | 2026-08-10T18:49:07Z |
> | Result | `code 0` — success |
> | Messages | 81 × `MsgBeginRedelegate` |

## Summary

Eight of the 85 Cycle II allocations did not stand. This correction reclaimed
**929,597.97 ATONE** from them and redistributed it across the remaining
**74 active recipients**, using AiB's own Cycle II allocation formula.

| Ground | Validators | ATONE |
|---|---:|---:|
| Undisclosed common control (sybil) | 5 | 508,433.63 |
| Operator has ceased or abandoned operations | 3 | 421,164.33 |
| **Total** | **8** | **929,597.97** |

No validator loses an allocation for a missed upgrade, for downtime, or for any
performance reason. Nothing here is a re-scoring — the two grounds below are the only
bases on which stake is reclaimed.

## Grounds

### 1. Undisclosed common control — 5 validators, 508,433.63 ATONE

PrimeStake, Stella and Nodedog form one operator cluster; Nurturra and Shire form a
second. The on-chain evidence is set out in full in the accompanying sybil report and
includes direct transfers between the validators' own wallets, shared reward-withdrawal
addresses, same-block co-signing, coordinated unjailing and identical governance voting.

All five answered the mandatory *Disclosure of Conflict of Interest* field — which requires
disclosure of "affiliations with AiB, its employees or **any other validator**" — by
denying any affiliation. Each therefore holds a Level 3-equivalent allocation obtained on
an incomplete disclosure, and the two operators between them hold five allocations where
the programme intended two.

The co-signing pattern remains live: on **2026-08-01 all three cluster A validators were
jailed in the same block, 9698922** — a fourth such event after 2026-02-08, 2026-03-26 and
2026-07-12. All three are `UNBONDING` and outside the active set, with downtime-slash
counts of 5, 4 and 4.

### 2. Ceased or abandoned operations — 3 validators, 421,164.33 ATONE

| Validator | Jailed since | State | Basis |
|---|---|---|---|
| Moonkitt | 2025-11-10 | `UNBONDED` | moniker: `CEASING OPS NOV 10 - REDELEGATE NOW` |
| CosmicNode | 2026-06-11 | `UNBONDED` | no contact, unrelated to the upgrade, ~2 months out |
| Cosmostation | 2026-07-20 | `UNBONDED` | moniker: `[Shutting down] cosmostation please redelegate` |

Two of the three state it in their own moniker, and both are effectively asking for this
redelegation. Moonkitt's request has gone unactioned for nine months; the date in its
moniker matches its jail block exactly. Cosmostation announced its shutdown on 2026-07-20,
three days before the `v4` upgrade, so its exit is unrelated to that event.

CosmicNode was jailed on 2026-06-11, six weeks before the upgrade, and has been fully
unbonded since 2026-07-02 with no communication. It is included on duration alone; if the
operator is reachable and intends to return, it should be removed from the sources.

## Sources

| Validator | Address | Ground | Reclaimed |
|---|---|---|---:|
| PrimeStake | `atonevaloper1n5z25m5…uyaur8` | Sybil cluster A | 91,663.40 |
| Stella | `atonevaloper1rs3vdtd…kh989j` | Sybil cluster A | 85,438.22 |
| Nodedog | `atonevaloper1s730pkr…y0aw32` | Sybil cluster A | 116,059.91 |
| Nurturra | `atonevaloper1dqw494n…x30jgz` | Sybil cluster B | 106,199.28 |
| Shire | `atonevaloper1rhspxhk…nd0n5s` | Sybil cluster B | 109,072.83 |
| Moonkitt | `atonevaloper17v5lwnd…uej2mx` | Ceasing operations — jailed 2025-11-10, moniker reads `CEASING OPS NOV 10 - REDELEGATE NOW` | 180,606.02 |
| Cosmostation | `atonevaloper1wez3ehd…gnlwc8` | Shutting down — jailed 2026-07-20, moniker reads `[Shutting down] please redelegate` | 122,278.96 |
| CosmicNode | `atonevaloper1v2srqza…503lj6` | Abandoned — jailed 2026-06-11, unbonded since 2026-07-02, unrelated to the v4 upgrade | 118,279.35 |
| | | **Total** | **929,597.97** |

## Redistribution

Cycle II allocated `score x (pool / total_score)`. This correction re-runs that same
formula with the eight removed, so no new methodology is introduced:

```
allocation_i = score_i x ( 929,597.97 / 1,913.32 )
             = score_i x 485.8560 ATONE
```

Every remaining recipient's allocation rises by the same proportion. Each receives
`floor(score x rate)`; the sub-1-uatone remainder from 74 floor operations goes to the highest
scorer so the totals reconcile exactly.

**Three scored recipients were excluded as destinations** because they were jailed at the
time of execution, and a redelegation to a jailed validator would have sat idle. They were
not sources and kept everything they hold:

| Validator | Score | Holds | Jailed |
|---|---:|---:|---|
| 🚀 WHEN MOON 🌕 WHEN LAMBO 🔥 RESTAKE ✅ | 30.55 | 186,762.43 | block 9819662, 2026-08-09 |
| Revonode | 23.84 | 145,727.37 | block 9819662, 2026-08-09 |
| NosNode🔮 | 16.81 | 102,754.91 | block 9819662, 2026-08-09 |

Their combined 71.20 score leaves the divisor, which is why the rate is 485.8560 rather than
468.4246. Their exclusion applies only to this correction; they retain their existing
allocations in full.

| Validator | Score | Current | Gains | New total |
|---|---:|---:|---:|---:|
| AVIAONE.com 🟢 | 44.06 | 269,381 | +21,406.81 | 290,787.36 |
| Nodes Hub 🛡️ 100% Slash Protected 🛡️ | 39.53 | 241,684 | +19,205.89 | 260,890.25 |
| PRO Delegators | 37.48 | 229,151 | +18,209.88 | 247,360.65 |
| ChainTools | 37.40 | 228,662 | +18,171.01 | 246,832.67 |
| POSTHUMAN 🧬 StakeDrop | 37.36 | 228,417 | +18,151.58 | 246,568.67 |
| Cogwheel ⚙️ | 37.07 | 226,644 | +18,010.68 | 244,654.73 |
| Inter Blockchain Services | 36.24 | 221,569 | +17,607.42 | 239,176.89 |
|  Silk Nodes | 34.39 | 210,259 | +16,708.59 | 226,967.26 |
| GATA HUB | 34.23 | 209,280 | +16,630.85 | 225,911.29 |
| ECO Stake 🌱 \| REStake.app | 33.77 | 206,468 | +16,407.36 | 222,875.38 |
| PathrockNetwork | 33.57 | 205,245 | +16,310.19 | 221,555.42 |
| Umbrella ☔ | 32.37 | 197,908 | +15,727.16 | 213,635.65 |
| [NODERS] | 32.16 | 196,625 | +15,625.13 | 212,249.69 |
| ksalab | 31.72 | 193,846 | +15,411.35 | 209,257.85 |
| NODEJUMPER | 31.64 | 193,445 | +15,372.48 | 208,817.80 |
| StakerHouse | 31.59 | 193,140 | +15,348.19 | 208,487.81 |
| VALIDARIOS | 31.54 | 192,834 | +15,323.90 | 208,157.81 |
| Regenerator \| Green Validator 🌱 | 31.28 | 191,244 | +15,197.58 | 206,441.87 |
| silent | 31.21 | 190,816 | +15,163.57 | 205,979.88 |
| Nodeist 🛡️ Slash Protected | 31.18 | 190,633 | +15,148.99 | 205,781.89 |
| Ubik Capital | 30.81 | 188,371 | +14,969.22 | 203,339.96 |
| KalpaTech | 30.60 | 187,087 | +14,867.19 | 201,954.00 |
| Provalidator | 30.54 | 186,720 | +14,838.04 | 201,558.01 |
| NyanCat | 30.45 | 186,170 | +14,794.31 | 200,964.03 |
| UTSA | 30.44 | 186,109 | +14,789.46 | 200,898.03 |
| Kleomedes | 30.44 | 186,109 | +14,789.46 | 200,898.03 |
| plantree | 30.07 | 183,834 | +14,609.69 | 198,443.92 |
| Oneiric Stake | 29.83 | 182,370 | +14,493.08 | 196,863.01 |
| LuckyStar | 29.65 | 181,279 | +14,405.63 | 195,684.19 |
| bitszn \| valopers.com | 29.55 | 180,667 | +14,357.04 | 195,024.21 |
| Foxinodes | 29.30 | 179,139 | +14,235.58 | 193,374.25 |
| KonsorTech | 29.24 | 178,772 | +14,206.43 | 192,978.27 |
| Roomit | 29.02 | 177,409 | +14,099.54 | 191,508.57 |
| equinoxDAO | 28.77 | 175,898 | +13,978.08 | 189,876.36 |
| ITRocket | 27.66 | 169,112 | +13,438.78 | 182,550.58 |
| Citizen Web3 | 27.49 | 168,072 | +13,356.18 | 181,428.61 |
| cunum | 27.34 | 167,122 | +13,283.30 | 180,405.21 |
| TaxiStake | 26.58 | 162,509 | +12,914.05 | 175,422.79 |
| ruangnode | 26.45 | 161,714 | +12,850.89 | 174,564.81 |
| 🔥STAVR🔥 REStake ON✅ | 26.30 | 160,797 | +12,778.01 | 173,574.84 |
| SyaNodes | 26.21 | 160,247 | +12,734.29 | 172,980.86 |
| AlxVoy ⚡ ANODE.TEAM | 25.85 | 158,046 | +12,559.38 | 170,604.93 |
| CroutonDigital | 25.73 | 157,312 | +12,501.07 | 169,812.95 |
| Kynraze | 25.48 | 155,777 | +12,379.61 | 168,156.91 |
| sychonix | 25.47 | 155,722 | +12,374.75 | 168,097.01 |
| HazenNetworkSolutions | 24.94 | 152,482 | +12,117.25 | 164,599.11 |
| Tecnodes | 24.58 | 150,281 | +11,942.34 | 162,223.18 |
| StakeUp | 24.56 | 150,159 | +11,932.62 | 162,091.18 |
| NexuSecurus | 24.44 | 149,425 | +11,874.32 | 161,299.21 |
| BonyNode💚 | 24.30 | 148,569 | +11,806.30 | 160,375.23 |
| CrowdControl | 23.23 | 142,013 | +11,286.43 | 153,299.24 |
| Vinjan.Inc | 22.18 | 135,607 | +10,776.29 | 146,383.65 |
| BZE Community | 22.09 | 135,057 | +10,732.56 | 145,789.67 |
| Shazoes | 21.86 | 133,614 | +10,620.81 | 144,234.50 |
| 🏆OshVanK🏆 | 20.81 | 127,231 | +10,110.66 | 137,341.92 |
| linkednode | 20.72 | 126,681 | +10,066.94 | 136,747.94 |
| StakeLab.zone | 19.70 | 120,409 | +9,571.36 | 129,980.01 |
| owlstake | 19.25 | 117,693 | +9,352.73 | 127,046.23 |
| Apollo | 19.12 | 116,899 | +9,289.57 | 126,188.25 |
| 👋 79anvi 🍀 | 19.00 | 116,165 | +9,231.26 | 125,396.27 |
| SECARD | 18.22 | 111,356 | +8,852.30 | 120,207.87 |
| CoinHunters | 17.35 | 106,050 | +8,429.60 | 114,479.29 |
| NodeRuneR | 17.17 | 104,968 | +8,342.15 | 113,309.91 |
| 🔥 BIERFORGE ⚒ 🔥 REStake | 16.00 | 97,823 | +7,773.70 | 105,596.86 |
| Fluxen | 15.13 | 92,504 | +7,351.00 | 99,855.03 |
| 🐾TRACE™ | 15.07 | 92,137 | +7,321.85 | 99,459.04 |
| 0base.vc | 15.00 | 91,709 | +7,287.84 | 98,997.06 |
| dnsarz | 14.77 | 90,294 | +7,176.09 | 97,470.07 |
| Tanjira | 14.19 | 86,748 | +6,894.30 | 93,642.54 |
| Chiter in Cosmos ⚛ | 11.00 | 67,253 | +5,344.42 | 72,597.84 |
| MIPEnode | 10.00 | 61,139 | +4,858.56 | 65,998.04 |
| MictoNode | 8.71 | 53,252 | +4,231.81 | 57,484.29 |
| Winnode | 7.87 | 48,107 | +3,823.69 | 51,930.83 |
| Simply Staking | 3.00 | 18,342 | +1,457.57 | 19,799.41 |
| | **1,913.32** | | **+929,597.97** | |

## Consequences

- Nurturra and Shire leave the 100-validator active set as a result. Stella and
  Nodedog are already out, jailed on 2026-08-01. PrimeStake retains a third party's
  62,904 ATONE.
- Moonkitt, CosmicNode and Cosmostation are already outside the set; reclaiming their stake
  changes nothing for them operationally.
