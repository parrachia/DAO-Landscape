# Layer 1: Network-based Governance Case Studies

## Introduction

We need to make a lot of experiments and thoroughly document them in order to find a working formula for the on-chain governance. This research is dedicated to collect, categorize and compare different attempts in governance automation and scaling with blockchain systems.

Work is in progress with no final state – to be constantly updated and changed \(feel free to do pull requests\). [Discussion](https://daotalk.org/t/case-studies-decentralized-orgs-with-on-chain-governance/395) happens on the forum.

## Methodology

Structure of the report:

* Purpose
* History & key events
* Objects of governance \(e.g. repo, funds distribution\) & Used mechanics \(on-chain, off-chain\)
* Risk Management
* Network Stats
* Links



## Tezos \(XTZ\)

![](../.gitbook/assets/image%20%285%29.png)

### Purpose

Tezos is a self-amending blockchain network which incorporates a formal, on-chain mechanism for proposing, selecting, testing, and activating protocol upgrades without the need to hard fork. Operates under liquid PoS consensus.

### History & key events

* 2014 – Arthur Breitman and Kathleen Breitman, started developing Tezos with a core group of developers
* 2017 – $232 million ICO
* Feb 2018 – [Dispute and Board reshuffle](https://www.coindesk.com/tezos-board-reshuffled-johann-gevers-steps)
* Jun 2018 – Testnet launch
* Sep 2018 – Mainnet Launch
* Apr 2019 – [First Exploration Vote](https://www.tezos.help/votes/)

### Objects of governance & Used mechanics

![](../.gitbook/assets/image%20%282%29.png)

Upgrades to the protocol through proposal & voting process. Uses min quorum adapted to the average participation and and 80% of supermajority support level to pass.

* Developers independently submit proposals for protocol upgrades and request for compensation for their work.
* The request for compensation makes sure that the developers have a strong economic incentive to contribute to the ecosystem
* The proposal goes through a testing period wherein the community tests the protocol and criticizes it for possible improvements.
* After repeated testing, the Tezos token holders can then vote on whether the proposal should be approved or not.
* Once a legitimate upgrade is decided on, a “hot swap” occurs on the protocol, which initiates the new version of the protocol.

### Network Stats \(on April 2019\)

* [Market cap $0.79B](https://messari.io/asset/tezos)
* 460 bakers \(analogue of block validators\)
* 106 public delegates \(who you can delegate your XTZ tokens if you have less then 10k\)

### Links

* [Tezos Whitepaper](https://tezos.com/static/white_paper-2dc8c02267a8fb86bd67a108199441bf.pdf)
* [Tezos Wiki](https://tqgroup.gitlab.io/tezos-wiki/files/self-amendment.html)
* [Amending Tezos](https://medium.com/tezos/amending-tezos-b77949d97e1e) by Jacob Arluck
* [https://tzscan.io](https://tzscan.io/charts_bakers)
* [https://tezos.gitlab.io/master/whitedoc/voting.html](https://tezos.gitlab.io/master/whitedoc/voting.html)
* [https://www.reddit.com/r/tezos/](https://www.reddit.com/r/tezos/)
* [https://kukai.app/bakers-list](https://kukai.app/bakers-list)
* [https://mytezosbaker.com/](https://mytezosbaker.com/)
* [https://blockgeeks.com/guides/what-is-tezos/](https://blockgeeks.com/guides/what-is-tezos/)

## EOS \(EOS\)

![](../.gitbook/assets/image%20%286%29.png)

### Purpose

Business platform for distributed apps with reliable governance, optimized for scaling and cheap/instant transactions.

### History & key events

* Mar 2018 – Technical Whitepaper
* As a result of scams and theft, leaving 7 individuals without access to their EOS on the mainnet. [The top 21 block producers at the time unanimously voted to freeze the accounts the affected accounts, without an official order from ECAF.](https://medium.com/coinmonks/a-deep-dive-into-eos-governance-49e892eeb4a2)
* After the freeze of the accounts the block producers filed a dispute against themselves, in order to have their actions reviewed by ECAF. [The actions were deemed just by an \(emergency\) arbitrator, and the freeze of 20 more accounts was ordered, sparking even more controversy, as no evidence that these accounts were in any way compromised was presented to the community.](https://medium.com/coinmonks/a-deep-dive-into-eos-governance-49e892eeb4a2)
* Sep 2018 – a Twitter account [named “Maple Leaf Capital”](https://twitter.com/MapleLeafCap/status/1046849762547372032) produced screenshots from a leaked Excel spreadsheet that supposedly show the China-based exchange Huobi, one of the world’s oldest and largest, accepting money for its support of certain entities in the charge of ensuring the network’s distributed decision-making. EOS and Huobi disproved but initiated an investigation.

### Objects of governance & Used mechanics 

#### Consitution and voting

[EOS has a constitution with governance features baked into the smart contract](https://github.com/EOS-Mainnet/governance/blob/master/eosio.system/eosio.system-clause-constitution-rc.md). In order to alter the constitution, the following process will have to take place:

> 1. Block producers propose a change to the constitution and obtains 15/21 approval.  
> 2. Block producers maintain 15/21 approval of the new constitution for 30 consecutive days.  
> 3. All users are required to indicate acceptance of the new constitution as a condition of future transactions being processed.  
> 4. Block producers adopt changes to the source code to reflect the change in the constitution and propose it to the blockchain using the hash of the new constitution.  
> 5. Block producers maintain 15/21 approval of the new code for 30 consecutive days.  
> 6. Changes to the code take effect 7 days later, giving all non-producing full nodes 1 week to upgrade after ratification of the source code.  
> 7. All nodes that do not upgrade to the new code shut down automatically.

The creation of an exact replica of an official \(off-chain\) ECAF order, resulting in a lot of confusion, has shown the flaws in the way official ECAF orders are given. ECAF has acknowledged this flaw and has created a way to verify orders on-chain. This method works for now, but a new, on-chain system to verify and receive official ECAF orders could help a lot.

#### ECAF

At the launch of the EOS mainnet all parties agreed on a constitution, naming ECAF \(EOS Core Arbitration Forum\). Block producers execute all of ECAF’s rulings. [Unlike Block Producers which the community chooses by voting, ECAF members are self-appointed.](https://www.reddit.com/r/eos/comments/9vo3rz/pitfalls_of_eos_governance/) 24 Block Producers have produced 64 blocks containing transactions that broke 10 ECAF Orders of Emergency Protection.

[Any EOS token holder who violates the constitution is in breach of contract, and could theoretically be subject to civil action.](https://medium.com/coinmonks/possible-improvements-to-eos-governance-7432b7afea1b)

ECAF blacklisted a number of EOS accounts that were identified as associated with fraudulent activity. [Blacklists are issued by ECAF and are delivered to block producer meetings.](https://cryptoslate.com/eos-governance-divides-crypto-community/) Block producer EosStore was not compliant with an ECAF blacklist issuance, and as a result, an account lost funds. An official [statement](https://steemit.com/statement/@eos.store/statement-of-updating-the-blacklist-from-ecaf?sort=votes) released by EosStore on June 26, 2018, confirmed the block producer did indeed neglect to update blacklist data.

#### Vote buying

> **Article IV — No Vote Buying**  
> No Member shall offer nor accept anything of value in exchange for a vote of any type, nor shall any Member unduly influence the vote of another.

Token holders can file claims against bad and/or non-complying block producers, get help with stolen accounts, and much more. Holders of capital are always looking for return. This is why people bought EOS tokens in the first place. What inevitably happens is that large token holders are able to make verbal back-room deals to commit their stake to certain block producers for certain benefits, but small token holders are not able to do this.

[Some argue it seems natural that they would \(and must\) use those tokens to support other block producers they have collaborated with and believe to be good stewards of the network.](https://medium.com/coinmonks/possible-improvements-to-eos-governance-7432b7afea1b)

> “As EOS grows and supports more use cases, those invested in the long-term success of the network will combat the forces, like vote manipulation, that degrade the long-term security of the network.” from [Aurora EOS](https://www.auroraeos.com/blog/combatting-vote-manipulation-on-eos/)

Even if Huobi isn’t buying votes now, eventually someone almost certainly will unless rules are put in place that the whole community views as legitimate.

Block.one [CEO Brendan Blumer made waves in the EOS community with a tweet](https://twitter.com/BrendanBlumer/status/1080164179091193857) suggesting that the EOS constitution be modified to allow block producers to pay dividends to users who contribute to their stake. Prosed change:

1. BPs may offer rebates.
2. Rebates will be paid to all tokens who voted, regardless of which BP they voted for, via some kind of mechanism built into the EOS blockchain.
3. Non-voting tokens will not receive rebates.

#### Participation level

[EOS voter participation is low.](https://www.auroraeos.com/blog/combatting-vote-manipulation-on-eos/) EOS governance as written does not work well with exchanges, which have custody over a vast amount of user cryptocurrency. [Perhaps more importantly, there’s no way to prevent exchanges from voting the tokens of their users who don’t care to vote.](https://www.coindesk.com/vitalik-called-it-vote-buying-scandal-stokes-fears-of-eos-failure) 

Bitfinex has written open source software [to enfranchise its users](https://support.bitfinex.com/hc/en-us/articles/360005324573-Bitfinex-Ballot-EOS-Block-Producer-Voting), but it has limitations. We do not know of any other exchanges that have implemented it or anything similar.

### Network Stats \(on April 2019\)

* [Market cap $4.8B](https://coinmarketcap.com/currencies/eos/)
* [25M blocks generated](https://www.reddit.com/r/eos/comments/9vo3rz/pitfalls_of_eos_governance/)
* [17 Orders issued by ECAF](https://www.reddit.com/r/eos/comments/9vo3rz/pitfalls_of_eos_governance/)
* [62k EOS lost by misbehavior ](https://www.reddit.com/r/eos/comments/9vo3rz/pitfalls_of_eos_governance/)\(~$300k\)

### Links

* [EOS Technical White Paper v2](https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md)
* [A Deep Dive Into EOS Governance](https://medium.com/coinmonks/a-deep-dive-into-eos-governance-49e892eeb4a2)
* [An Alternative EOS Staking Algorithm](https://medium.com/@kengriffith_54628/an-alternative-eos-staking-algorithm-4f3519cc7157)
* [Risk-Reward Based Governance for EOS](https://medium.com/coinmonks/possible-improvements-to-eos-governance-7432b7afea1b)

## DASH

![](../.gitbook/assets/008-dash-icon.png)

### Purpose

[Digital Cash, peer-to-peer digital currency.](https://www.dash.org/learning-resources/)

### History & key events

* January 2014 launched as "Xcoin"
* Rebranded to Darkcoin \(2015\) and then Dash \(2016\)
* February 2018, [a legal entity was formed which represents the DAO, and this entity took ownership of Dash Core](https://www.dashforcenews.com/dash-core-group-becomes-first-legally-dao-owned-entity/)

### Objects of governance & Used mechanics 

#### Masternodes

[Masternode Operators \(MNOs\) are key actors in the Dash network. ](https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4)Dash Masternodes \(MNs\) provide certain services \(InstantSend and PrivateSend\) to users, receive 45% of the block reward, and collectively control the project’s development fund through voting. A MNO can operate multiple MNs.

#### Treasury

Each month, DASH dispenses 10% of the block rewards for that month in a superblock. This DASH is distributed to the wallets associated with treasury budget proposals which have scored highly enough to receive a payout. MNOs vote Yes, No or Abstain to proposals, on the basis of one vote per MN. Money is available by default, not allocated budget coins are not minted.

#### Funds distribution

There is a [voting threshold which determines whether a proposal will be funded](https://docs.dash.org/en/latest/governance.html#budgets-and-masternode-voting): a net Yes vote greater than 10% of all MNs. The threshold formula is: \(YES votes — NO votes\) &gt; \(Total Number of Masternodes / 10\). Formal submission of a proposal costs a fee of 5 DASH.

![https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4](../.gitbook/assets/image%20%2810%29.png)

![https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4](../.gitbook/assets/image.png)

![https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4](../.gitbook/assets/image%20%289%29.png)

### Network Stats \(on April 2019\)

* 6,176 DASH distributed on April \(~$730k\), around that amount is distributed on monthly basis
* 4,769 masternode
* 295 proposals approved out of 474
* 18.7% – median amount of masternode participation

### Links

* [Dash Governance](https://www.dash.org/governance/%20)
* [Observations of the Dash Treasury DAO](https://medium.com/@richardred/observations-of-the-dash-treasury-dao-c94231b2b5c4)
* [Dash Central](https://www.dashcentral.org/)

## Grin

![](../.gitbook/assets/image%20%283%29.png)

### Purpose

[Grin is a new Mimblewimble-based cryptocurrency that offers privacy and scalability improvements.](https://medium.com/blockchain-capital-blog/grin-governance-a-novel-approach-154aca07291b)

### History & key events

* launched on January 15th, 2019

### Objects of governance & Used mechanics

#### Foundation

There are [no current or future plans](https://github.com/mimblewimble/docs/wiki/Regarding-Foundations) to create an official Grin Foundation or legal entity.  Grin has [bi-weekly governance meetings](https://github.com/mimblewimble/grin-pm/tree/master/notes) that anyone can participate in. The[ Governance forum](https://www.grin-forum.org/c/governance) is quite active, with [many threads](https://www.grin-forum.org/t/governance-plan/461/7) around governance [norms and frameworks.](https://www.grin-forum.org/t/governance-consensus-baby-step-1-20180807-meeting/615) 

#### Technical Council

The Grin Technical Council is currently composed of 8 members:

* [Antioch Peverell](https://github.com/antiochp)
* [hashmap](https://github.com/hashmap)
* [Ignotus Peverell](https://github.com/ignopeverell)
* [Jaspervdm](https://github.com/jaspervdm)
* [lehnberg](https://github.com/lehnberg)
* [Quentin le Sceller](https://github.com/quentinlesceller)
* [John Tromp](https://github.com/tromp)
* [Yeastplume](https://github.com/yeastplume)

The Council’s main responsibility includes management of the Grin General Fund, as well as stewardship of the protocol through the open development and governance meetings.

**Funding**

As mentioned previously, Grin launched in a fair manner, and project founders and developers don’t receive any funding directly from the protocol, or from investors.

As such, Grin relies primarily on two different means of funding.

1. Individual project based fundraising — in which individual campaigns are proposed and funded by donors. Examples include [Yeastplume’s funding campaigns](https://grin-tech.org/yeastplume), as well as the [Security Audit Funding](https://grin-tech.org/sec_audit). The money raised goes directly into an account controlled by the person making the request. This is a similar model to Monero’s [Forum Funding System](https://ww.getmonero.org/forum-funding-system/), where anyone in the community can propose a project and request funding.
2. General Funding for Grin’s Development — Grin has a [General Fund](https://grin-tech.org/general_funding) that’s always open for donations, and goes towards a miscellaneous set of costs related to Grin development, including service fees, marketing materials, travel, developer funding, or legal support.

Many early ecosystem participants \(miners, funds, pools\) have [chosen to contribute to Grin](https://grin-tech.org/friends). [Grinmint has chosen to donate](https://blog.blockcypher.com/grin-mining-pool-47286f5e0b8d) a percentage of pool proceeds to the Grin developer team. Additionally, Obelisk has [committed to donating](https://medium.com/obelisk-blog/the-obelisk-grn1-an-asic-for-grin-1d1ff580a19d) a portion of their revenue from their Grin ASIC to supporting Grin development.

**Grin Risk Management**

Blockchain governance is most relevant in times of disaster, distress, or conflict. Bitcoin Governance demonstrated its strength during the Segwit2x hard fork. Ethereum demonstrated its governance system during the DAO event.

Grin developers have written a lot about their [risk management system](https://github.com/mimblewimble/docs/wiki/Introduction-to-Risk-Management-for-Grin), and have brainstormed the [specific downside scenarios](https://docs.google.com/spreadsheets/d/1zTtlMIgJFzmyedKD07dA0jn3eP4HD7eZqLjD8cVd_4c/edit#gid=287721861), and ways to respond. It’s generally good practice to brainstorm various scenarios, and think about contingency plans and potential responses. Many of the scenarios they’ve outlined, such as the possibility of a critical bug, secret ASICs, or a 51% attack are very real scenarios that have happened to many other blockchains.

### Network Stats \(on April 2019\)

* not much info now

### Links

* [https://medium.com/blockchain-capital-blog/grin-governance-a-novel-approach-154aca07291b](https://medium.com/blockchain-capital-blog/grin-governance-a-novel-approach-154aca07291b)

## Bitcoin

...

## Ethereum

...

## Decred

* [https://proposals.decred.org/](https://proposals.decred.org/)

## Polkadot

Time-lock Voting + Delayed Enactment

![](../.gitbook/assets/image%20%288%29.png)

* [https://github.com/paritytech/polkadot/wiki/Governance](https://github.com/paritytech/polkadot/wiki/Governance)

## Cardano

* [https://cryptovest.com/news/cardano-ada-hit-by-governance-woes-as-iohk-emurgo-chairs-split-with-cardano-foundation/](https://cryptovest.com/news/cardano-ada-hit-by-governance-woes-as-iohk-emurgo-chairs-split-with-cardano-foundation/)

## Summary

...

Thanks to Jacob Arluck, Andriy Khavryuchenko, Vahid Toosi for the feedback and improvements.



## To Do's

* Decred
* Ethereum
* Bitcoin
* Cardano
* Polkadot
* Define questions to be answered with the research
* [https://github.com/RichardRed0x/crypto-governance-research](https://github.com/RichardRed0x/crypto-governance-research)
* [https://medium.com/coinmonks/ethereum-classic-the-ungoverned-blockchain-b9ae8986a60a](https://medium.com/coinmonks/ethereum-classic-the-ungoverned-blockchain-b9ae8986a60a)

