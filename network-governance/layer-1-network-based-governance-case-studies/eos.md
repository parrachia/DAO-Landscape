# EOS

![](../../.gitbook/assets/image%20%2810%29.png)

### Purpose

Business platform for distributed apps with reliable governance, optimized for scaling and cheap/instant transactions.

### History & key events

* Mar 2018 – Technical Whitepaper
* As a result of scams and theft, leaving 7 individuals without access to their EOS on the mainnet. [The top 21 block producers at the time unanimously voted to freeze the accounts the affected accounts, without an official order from ECAF.](https://medium.com/coinmonks/a-deep-dive-into-eos-governance-49e892eeb4a2)
* After the freeze of the accounts the block producers filed a dispute against themselves, in order to have their actions reviewed by ECAF. [The actions were deemed just by an \(emergency\) arbitrator, and the freeze of 20 more accounts was ordered, sparking even more controversy, as no evidence that these accounts were in any way compromised was presented to the community.](https://medium.com/coinmonks/a-deep-dive-into-eos-governance-49e892eeb4a2)
* Sep 2018 – a Twitter account [named “Maple Leaf Capital”](https://twitter.com/MapleLeafCap/status/1046849762547372032) produced screenshots from a leaked Excel spreadsheet that supposedly show the China-based exchange Huobi, one of the world’s oldest and largest, accepting money for its support of certain entities in the charge of ensuring the network’s distributed decision-making. EOS and Huobi disproved but initiated an investigation.

{% hint style="info" %}
But one thing I saw in the paper is that you are saying that multisig \(15/21\) needs to be for 30 days. That’s wrong. It’s referendum that needs 30 days. And that’s the old constitution. We have updated our current C with a User agreement instead.
{% endhint %}

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
* [https://cryptodaily.co.uk/2019/04/eos-constitution-changed-voting-impasse](https://cryptodaily.co.uk/2019/04/eos-constitution-changed-voting-impasse), check new constitution

