# Delegations Cycle II, 20 November 2025

## How Cycle II was allocated

Unlike Cycle I, Cycle II used **no delegation levels**. Every allocation is the
validator's score multiplied by a single constant — the pool divided by the sum of all
scores:

```
allocation_i = ( score_i / 2,136.59 ) x 13,062,926 ATONE
             = score_i x 6,113.91 ATONE
```

## Execution

Cycle II was executed on **20 November 2025** in two successful transactions:

| Height | Timestamp (UTC) | Contents |
|---|---|---|
| 5933857 | 2025-11-20T22:10:09 | 38 `MsgBeginRedelegate` |
| 5934176 | 2025-11-20T22:40:59 | 57 `MsgDelegate` |

## Reconciling with the Cycle I document

The "held before" figures here are larger than the amounts in
[Cycle I](./Delegations-Cycle-I-27-March-2025.md). The difference is an **undocumented
top-up delegated on 2 June 2025**, applied as a uniform **+28.96%** across all four tiers:

| Tier | Cycle I document | June 2025 top-up | Held before Cycle II |
|---|---:|---:|---:|
| Level 1 | 159,473 | +46,183 | **205,656** |
| Level 2 | 106,315 | +30,788 | **137,103** |
| Level 3 | 70,877 | +20,525 | **91,402** |
| Level 4 | 47,252 | +13,684 | **60,936** |

In total the multisig has made five delegation events, of which one has been published:

| Date | Event | Published |
|---|---|---|
| 2024-10-18 | 6 seed delegations of 278,000 each | no |
| 2025-01-06 | 63 delegations, 3,359,979 ATONE | no |
| 2025-03-27 | Cycle I | yes |
| 2025-06-02 | uniform +28.96% top-up | no |
| 2025-11-20 | Cycle II | no — reconstructed here |

## Validators removed in Cycle II — all for missing KYC

Eleven validators held an AiB delegation before Cycle II and hold nothing after it,
totalling **1,194,003 ATONE**. Every one of them has not provided KYC.

| Validator | Score | KYC | Held before | Residual |
|---|---:|---|---:|---:|
| Forbole | 29.58 | No | 205,656 | 0 |
| 01node | 29.43 | No | 205,656 | 1,152 uatone |
| Crosnest | 28.60 | No | 205,656 | 927 uatone |
| Neta DAO | 22.00 | No | 137,117 | 0 |
| Chainroot | 16.32 | No | 137,103 | 0 |
| interchain.FM🥩 | 16.18 | No | 120,000 | 816 uatone |
| Onbloc Node | 20.44 | No | 60,936 | 0 |
| SIPALING-TESTNET | 7.34 | No | 60,942 | 0 |
| tRDM \| Nodera | 14.48 | No | 60,936 | 1,052 uatone |
| nylira.net | 15.00 | No | 1 | 0 |
| FIVETECH | 10.00 | No | 0 | 0 |
| | | | **1,194,003** | |

Residual dust of a few hundred uatone is rounding left by the redelegation, not an
intentional allocation.

Score was not the deciding factor. Forbole scored 29.58, 01node 29.43 and Crosnest 28.60
— all above the cohort median of 28.77 or within a whisker of it — and all three were
removed in full, while validators scoring 3.00 and 7.87 kept and grew their allocations.
Forbole is bonded, unjailed and holds 1,561,926 ATONE today; nothing about its operation
explains the removal.

This is the source of most of Cycle II's movement: **1,193,922 of the 1,474,509 ATONE
redelegated (81%) came from these eleven**. The remaining ~280,587 came from partial
reductions of KYC'd validators whose score-derived target fell below what they already
held.

## Allocation table

Sorted by delegation received. Total: **13,062,926 ATONE** across **85 validators**.

| Validator                                            | Score | Delegation Received | Validator Address                                   |
|------------------------------------------------------|-------|---------------------|-----------------------------------------------------|
| AVIAONE.com 🟢                                        | 44.06 |             269,381 | atonevaloper1342p4lqh94s8qrk48vz2x6nlh3p2hqx4autnd9 |
| Nodes Hub 🛡️ 100% Slash Protected 🛡️                 | 39.53 |             241,684 | atonevaloper1d3hahjfnr6579rpt7fkste4jaj6ne0jvqttj05 |
| PRO Delegators                                       | 37.48 |             229,151 | atonevaloper1zrp3cnmqg7rlr7n4mc3cfl4khn5p9a2frykp2c |
| ChainTools                                           | 37.40 |             228,662 | atonevaloper1per5z63kvyzgy0hqfkkwd45gg4rnjt4c7jdrkr |
| POSTHUMAN 🧬 StakeDrop                                | 37.36 |             228,417 | atonevaloper1vcp7pkg8sk0n8ylhezxxs8qqrnwfld4dsv2sew |
| Cogwheel ⚙️                                          | 37.07 |             226,644 | atonevaloper14ddv0apf90h6u46zy4e6msct9hx04nte0zcyfe |
| Inter Blockchain Services                            | 36.24 |             221,569 | atonevaloper1ngchl63yr5ew7ua7y72z4p80s32u6g9u09vguf |
| Silk Nodes                                           | 34.39 |             210,259 | atonevaloper1fvpj4kfk49s6her9fmak4dykz447vlx3uuj9hw |
| GATA HUB                                             | 34.23 |             209,280 | atonevaloper10unx6s0cdqntvrumd5hs07rgd5ytcztq7w6s7f |
| ECO Stake 🌱 \| REStake.app                           | 33.77 |             206,468 | atonevaloper1v6pes3zvpu926pep0l636wwda357uc20t0x5vd |
| PathrockNetwork                                      | 33.57 |             205,245 | atonevaloper1ke507rker0xenhf2zwvjwr8m9srfwgzsfxp0kk |
| Umbrella ☔                                           | 32.37 |             197,908 | atonevaloper1lktjhnzkpkz3ehrg8psvmwhafg56kfsscfjshg |
| [NODERS]                                             | 32.16 |             196,625 | atonevaloper1f2r68y2htcmp4rfe2wfn9f3nvzh9xsq9y0vdyz |
| ksalab                                               | 31.72 |             193,905 | atonevaloper16yfrzsnnk8qk85h2c2e33czm8h6ezdxrrpulqv |
| NODEJUMPER                                           | 31.64 |             193,445 | atonevaloper1pptwysv6ew8e55kzf8nr3vtfxhc9x0gfyfahx0 |
| StakerHouse                                          | 31.59 |             193,140 | atonevaloper18t9fc4fdg6y7fa3ctmyfcun9td6ema3f34j6lr |
| VALIDARIOS                                           | 31.54 |             192,834 | atonevaloper1euytennr2awmshq6e55kcw5v0fe5yvx62kndyh |
| Regenerator \| Green Validator 🌱                     | 31.28 |             191,244 | atonevaloper174tvh2dty7vsvwn2cfsmkwq8tplqgr5f7rsyuj |
| silent                                               | 31.21 |             190,816 | atonevaloper1cl9p5p60znznu297ka6lxgtl9fax53c74r7hwk |
| Nodeist 🛡️ Slash Protected                           | 31.18 |             190,633 | atonevaloper15e709ulu0sxgpwzu3vftkxd00eexapmj76e7kh |
| Ubik Capital                                         | 30.81 |             188,371 | atonevaloper1q6d3d089hg59x6gcx92uumx70s5y5wadlklzhr |
| KalpaTech                                            | 30.60 |             187,087 | atonevaloper1w8cs54tjx5yc9hzp0e2pfmde905pr670hglth4 |
| 🚀 WHEN MOON 🌕 WHEN LAMBO 🔥 RESTAKE ✅                 | 30.55 |             186,781 | atonevaloper1h5z3pc84rfnxludga8wg0yazl9x87d3tf0lv5z |
| Provalidator                                         | 30.54 |             186,720 | atonevaloper1g48268mu5vfp4wk7dk89r0wdrakm9p5xlxr0l9 |
| NyanCat                                              | 30.45 |             186,170 | atonevaloper1h7xtcxsh356vfcygglrcn67c8jk47mkx40mdda |
| UTSA                                                 | 30.44 |             186,109 | atonevaloper1982jsr4msdppq0azc3qhf80ngkrsjyqmgepkyk |
| Kleomedes                                            | 30.44 |             186,109 | atonevaloper1re7e8n5arf7c69mr75fqp2v5lcl0ftrr56uxkm |
| plantree                                             | 30.07 |             183,834 | atonevaloper1mlxsccj7dmk6dy4qljzusgqyr8f0uyyattkmly |
| Oneiric Stake                                        | 29.83 |             182,388 | atonevaloper14m0n559xdj00qwvp6ck0xesprrq26kgpufexgk |
| LuckyStar                                            | 29.65 |             181,279 | atonevaloper160u4kq3ygau92fumg883tplcretptvk7pynh4v |
| bitszn \| valopers.com                               | 29.55 |             180,667 | atonevaloper1elcgyvv9ym2m523hu88atukd0dmhrjv9fhg4mu |
| Moonkitt - CEASING OPS NOV 10 - REDELEGATE NOW       | 29.54 |             180,606 | atonevaloper17v5lwndhdf7mcv6hgk0tnn90x8gy3shquej2mx |
| Foxinodes                                            | 29.30 |             179,139 | atonevaloper1h7akavny3gx37rc57cth7h7829v6z72j3qmtnq |
| KonsorTech                                           | 29.24 |             178,772 | atonevaloper19zhyxjkxkwh8umftc9q2zw8skvzxs0n3kpun39 |
| Roomit                                               | 29.02 |             177,427 | atonevaloper10szh6uwqx8qy0lsp3fpkvnj99tsf2nf4g9uazc |
| equinoxDAO                                           | 28.77 |             175,898 | atonevaloper1h59eyhvxhhznhhhe7j2l8xdcctkcw76em8hrcr |
| ITRocket                                             | 27.66 |             169,112 | atonevaloper1pucqpsdadfgrvk90tt93slpwwu4vdf24p2yvsq |
| Citizen Web3                                         | 27.49 |             168,072 | atonevaloper1e859xaue4k2jzqw20cv6l7p3tmc378pcclyn60 |
| cunum                                                | 27.34 |             167,155 | atonevaloper159yk55uahpnywd0yht9tm2qr93eegh9gz283cy |
| TaxiStake                                            | 26.58 |             162,509 | atonevaloper1hk38pmr663m5achae0as20zzp27uxj3yyuvuh3 |
| ruangnode                                            | 26.45 |             161,714 | atonevaloper1phwcgsqpscthtuqwz7yfqqkpew2y0hscqygk9m |
| 🔥STAVR🔥 REStake ON✅                                  | 26.30 |             160,797 | atonevaloper13v0v7meel8kdevgcz9t379s0gcl7kldu04vrvh |
| SyaNodes                                             | 26.21 |             160,247 | atonevaloper1prfw7r9s79dlzj8hr5fpp6vlj4yan34hfa5hlp |
| AlxVoy ⚡ ANODE.TEAM                                  | 25.85 |             158,046 | atonevaloper1mxpzhjj6mqam6uuk8e4vcv32rzlpu28je8vakc |
| CroutonDigital                                       | 25.73 |             157,312 | atonevaloper14ekxy6xuamq022ueqq3scgmtkxl8xr7ljuu358 |
| Kynraze                                              | 25.48 |             155,793 | atonevaloper12gpns3u5aguwl8n5n6j7x94tm98nfvljlxhq8l |
| sychonix                                             | 25.47 |             155,722 | atonevaloper16l85m5pasrv0c43ewkfdf0hljx7fnc3d2v8w9l |
| HazenNetworkSolutions                                | 24.94 |             152,482 | atonevaloper1tz6hxmvqqqj6n67usvcwryy6ddl62aw8j7954p |
| Tecnodes                                             | 24.58 |             150,281 | atonevaloper1qru73rflllclslgcxglchvuj2z5pvhzldr6lem |
| StakeUp                                              | 24.56 |             150,159 | atonevaloper1nx4tej0d5f7pnarg56a9ykxmsdlt4e8xwvxazz |
| NexuSecurus                                          | 24.44 |             149,425 | atonevaloper1trmnr6hqu5v50xr0s8e3wu4xqkl68yrsa3tnm4 |
| BonyNode💚                                            | 24.30 |             148,569 | atonevaloper13nwzm5dfd26ue74jr6sc39gyn3qze0rjte8v92 |
| Revonode                                             | 23.84 |             145,757 | atonevaloper10nnweapu0gqyj0zzw45w7vg58yc4aagwkmnx7x |
| CrowdControl                                         | 23.23 |             142,027 | atonevaloper1q4p7fn0wafmt64c23d78k64ggxr34mzaszzxt8 |
| Vinjan.Inc                                           | 22.18 |             135,607 | atonevaloper17x76ltae2x4e93t8hry6fxeynlr29n7h9wzfmf |
| BZE Community                                        | 22.09 |             135,071 | atonevaloper1sa42hn5fuupm5wpgz6msx4nmrpec6az96vjqjw |
| Shazoes                                              | 21.86 |             133,650 | atonevaloper17f2sq92lqjxwztemmy0aeave07xqg4qtdtp73l |
| 🏆OshVanK🏆                                            | 20.81 |             127,231 | atonevaloper186av4ahtc685uarfqnuzp3683y9vypuz8fzn69 |
| linkednode                                           | 20.72 |             126,681 | atonevaloper1r4agrfcandmy7a7hu6wy6nejtavx5h99z5ua0f |
| Cosmostation                                         | 20.00 |             122,279 | atonevaloper1wez3ehdwxfygeeu2lj44swcdpds08t3pgnlwc8 |
| StakeLab.zone                                        | 19.70 |             120,409 | atonevaloper1gpqlu4ml3hqkfqf3vyrvj8040c6jdrt0l8eg34 |
| CosmicNode                                           | 19.35 |             118,279 | atonevaloper1v2srqzaqku25pdndegz3flhez6umfehp503lj6 |
| owlstake                                             | 19.25 |             117,693 | atonevaloper170m5fa0w6pdgsyqhkcp8fyqavl2l66c8t86sfn |
| Apollo                                               | 19.12 |             116,899 | atonevaloper1hrepv77qv6nh7953jrnqpar4c89yxg5hf8w4qr |
| 👋 79anvi 🍀                                           | 19.00 |             116,165 | atonevaloper12fh3e4sj9m3787u4r5zhxx5ghqwf25a8qzatjw |
| 🐶 Nodedog 🐶                                          | 18.99 |             116,106 | atonevaloper1s730pkrq2hxh762thw3als22st5p8jt2y0aw32 |
| SECARD                                               | 18.22 |             111,400 | atonevaloper1p64w6kc8f3le84x4jqytugpqxyrcxfqu26dum6 |
| Shire                                                | 17.84 |             109,073 | atonevaloper1rhspxhk2sdv45wvygm0vgskzc3689jtmnd0n5s |
| Nurturra 🌿                                           | 17.37 |             106,199 | atonevaloper1dqw494nd6u7s4gefht9xqfsy9pzmtcmex30jgz |
| CoinHunters                                          | 17.35 |             106,050 | atonevaloper1ahtj0s232nen0agnrf75uvf94prk2gmtp45epn |
| NodeRuneR                                            | 17.17 |             104,978 | atonevaloper1zktzg639sqfspncww5qxcefpnf33h8p0wnqka6 |
| NosNode🔮                                             | 16.81 |             102,775 | atonevaloper10jm8fvdyqlj78w0j5nawc76wsn4pqmdxkny2gd |
| 🔥 BIERFORGE ⚒ 🔥 REStake                              | 16.00 |              97,823 | atonevaloper1crsm4ds7tgwx6zhea3k3qt0hj82k3k4lq3qj4j |
| Fluxen                                               | 15.13 |              92,504 | atonevaloper10mf53lhx7x2s7vgrulsxq4g2z9n7dm4t472su3 |
| 🐾TRACE™                                              | 15.07 |              92,137 | atonevaloper1vvzwx7kjk9yx27vegp74tqu99k2vlz7treqxfw |
| PrimeStake 🌍🛡️                                       | 15.00 |              91,709 | atonevaloper1n5z25m5paxl2cy0c2g07zx04wnv23s4quyaur8 |
| 0base.vc                                             | 15.00 |              91,709 | atonevaloper1n3mhyp9fvcmuu8l0q8qvjy07x0rql8q4nq63k9 |
| dnsarz                                               | 14.77 |              90,303 | atonevaloper1uuqu7tmepex365vq2pluf25jqvutk8rrq5jvm0 |
| Tanjira                                              | 14.19 |              86,774 | atonevaloper1dh29h674ngeqenmc0d3nuuu8fqvf9u7gwzkdu5 |
| Stella 💜🐾                                            | 13.98 |              85,472 | atonevaloper1rs3vdtdwq8mnnr92zsgugrrs0zue0ejnkh989j |
| Chiter in Cosmos ⚛                                   | 11.00 |              67,253 | atonevaloper1603r7hdvmntnh67rr6gnf3myg5sj0020rdm774 |
| MIPEnode                                             | 10.00 |              61,139 | atonevaloper1e3vld469ekks28mhtd4aqua3mdaz64qgj2f8cj |
| MictoNode                                            |  8.71 |              53,252 | atonevaloper1fg97ymps3jsw8w7m6wtpnhn6faze070jkr9kyu |
| Winnode                                              |  7.87 |              48,117 | atonevaloper1kdxqxpy55tsm6jjeupqhj6spjp8zwz32fyluru |
| Simply Staking                                       |  3.00 |              18,342 | atonevaloper1xgkqle5jzfd3lymrttg8edwux2yz8z0rvxqsdd |
