# Tezos

![](https://picresize.com/images/rsz_0_ax8cvuwqvjl8_1zv_1.png)

### Purpose

Tezos is a self-amending blockchain network which incorporates a formal, on-chain mechanism for proposing, selecting, testing, and activating protocol upgrades without the need to hard fork. Operates under [liquid PoS consensus](https://medium.com/tezos/liquid-proof-of-stake-aec2f7ef1da7).

### History & Key Events

* 2014 – Arthur Breitman and Kathleen Breitman, started developing Tezos with a core group of developers
* 2017 – $232 million ICO
* Feb 2018 – [Dispute and Board reshuffle](https://www.coindesk.com/tezos-board-reshuffled-johann-gevers-steps)
* Jun 2018 – Testnet launch
* Sep 2018 – Mainnet Launch
* Apr 2019 – [First Exploration Vote](https://www.tezos.help/votes/)

## Objects of Governance & Used Mechanics

![](../.gitbook/assets/image%20%285%29.png)

### The Four Stages of Tezos Governance <a id="the-four-stages-of-tezos-governance"></a>

The amendment process can be broken into four discrete periods: the Proposal Period, the Exploration Period, the Testing Period, and the Promotion Period. Each of these four periods lasts eight baking cycles \(i.e. 32,768 blocks or roughly 22 days, 18 hours\), comprising almost exactly three months from proposal to activation.

As summarized in the flowchart diagram below, any failure to proceed to the subsequent period reverts the network back to a Proposal Period. In other words, failure to proceed restarts the entire amendment process.

#### Proposal Period <a id="proposal-period"></a>

The Tezos amendment process begins with the Proposal Period, during which bakers can submit proposals on-chain using the _proposals_ operation, which involves specifying one or multiple protocol hashes, each one representing a tarball of concatenated .ml/.mli source files.

Bakers may submit up to 20 proposals in each Proposal Period. When submitting a proposal, the baker is also submitting a vote for that proposal, equivalent to the number of rolls in its staking balance at the start of the period.

For those wanting to follow along, Tezos Agora and other Tezos block explorers such as [TzStats](https://tzstats.com/) allow you to watch incoming proposals.

Other bakers can then vote on proposals by submitting _proposals_ operations of their own. As described in the [whitepaper](https://tezos.com/static/white_paper-2dc8c02267a8fb86bd67a108199441bf.pdf), the Proposal Period vote is done via approval voting, meaning each baker may vote once on up to 20 proposals. Think of it as a form of “upvoting.”

At the end of the Proposal Period, the network counts the proposal votes. For any proposal to be considered valid, it must have enough upvotes to meet a 5% quorum. If the most upvoted proposal has at least 5% of the number of possible votes supporting it, the proposal proceeds to the Exploration Period. If the 5% quorum is not met, no proposals have been submitted, or there is a tie between proposals, the amendment process resets to a new Proposal Period.

#### Exploration Period <a id="exploration-period"></a>

In the Exploration Period, bakers may vote on the top-ranked proposal from the previous Proposal Period using the _ballot_ operation. Bakers get to vote either "Yay", "Nay", or "Pass" on a specific proposal. "Pass" just means to abstain from voting for or against a proposal. As in the Proposal Period, a baker's vote is based on the number of rolls in its staking balance at the start of the period.

At the end of the Exploration Period, the network counts the votes. If voting participation meets the quorum, and an 80% supermajority of non-abstaining bakers approves, the proposal proceeds to the Testing Period.

If the voting participation fails to achieve the quorum or the 80% supermajority is not met, the amendment process restarts to the beginning of the Proposal Period.

Regardless of the outcome of the vote, the quorum is updated based on past participation rates.

#### Testing Period <a id="testing-period"></a>

If the proposal is approved in the Exploration Period, the Testing Period begins with a testnet fork that runs in parallel to the main network for 48 hours.

This Testing Period is used to determine whether a proposal is a worthy amendment to the protocol. The testnet fork ensures the upgrade does not corrupt the blockchain network; should the upgrade be adopted, the network would continue making valid state transitions.

#### Promotion Period <a id="promotion-period"></a>

At the end of the Testing Period, the Promotion Period begins. In this period, the network decides whether to adopt the amendment based on off-chain discussions and its behavior during the Testing Period. As in the Exploration Period, bakers submit their votes using the _ballot_ operation, with their votes weighted proportionally to the number of rolls in their staking balance.

At the end of the Promotion Period, the network counts the number of votes. If the participation rate reaches the quorum and an 80% supermajority of non-abstaining bakers votes “Yay,” then the proposal is activated as the new mainnet.

Regardless of the outcome of the vote, the process reverts back to the Proposal Period and the quorum is updated based on past participation rates

### The Supermajority and Quorum Requirements <a id="the-supermajority-and-quorum-requirements"></a>

#### Proposal Period <a id="proposal-period-1"></a>

A proposal submitted during a Proposal Period needs to reach a quorum \(minimum participation rate\) in order to advance to the Exploration Period.

**Quorum requirement:** The number of votes for the most upvoted proposal divided by the number of possible votes must be greater than or equal to 5%.

#### Exploration & Promotion Periods <a id="exploration--promotion-periods"></a>

A vote during a voting period \(Exploration & Promotion\) needs to reach both a supermajority and a quorum \(minimum participation rate\) in order to succeed.

**Supermajority requirement:** The number of "Yay" votes divided by the number of "Yay" and "Nay" votes must be greater than or equal to 80%.

**Quorum requirement:** The number of "Yay", "Nay", and "Pass" votes divided by the number of possible votes must be greater than or equal to the current quorum.

Unlike the supermajority requirement which is fixed at 80%, the quorum requirement is updated at the end of each voting period using the following formula, where Q is the quorum in the voting period and q is the participation rate in the voting period:

![the quorum tries to match the exponential moving average of the past participation rate](../.gitbook/assets/image%20%2822%29.png)

{% embed url="https://www.youtube.com/watch?v=enYGSsfj\_Aw" %}

### Network Stats \(on May 2020\)

* Market Cap: $2,372,087,986
* 513 bakers \(analogue of block validators\)
* 106 public delegates \(who you can delegate your XTZ tokens if you have less then 10k\)

### Links

* [Tezos Whitepaper](https://tezos.com/static/white_paper-2dc8c02267a8fb86bd67a108199441bf.pdf)
* [Tezos Wiki](https://tqgroup.gitlab.io/tezos-wiki/files/self-amendment.html)
* [Amending Tezos](https://medium.com/tezos/amending-tezos-b77949d97e1e) by Jacob Arluck
  * [Chinese translation](https://tezos.org.cn/amendingtezos/)
* [The Voting Process](https://tezos.gitlab.io/whitedoc/voting.html) from Nomadic Labs
* [https://learn.tqgroup.io/](https://learn.tqgroup.io/)
* [https://tzscan.io](https://tzscan.io/charts_bakers)
* [https://tezos.gitlab.io/master/whitedoc/voting.html](https://tezos.gitlab.io/master/whitedoc/voting.html)
* [https://www.reddit.com/r/tezos/](https://www.reddit.com/r/tezos/)
* [https://kukai.app/bakers-list](https://kukai.app/bakers-list)
* [https://mytezosbaker.com/](https://mytezosbaker.com/)
* [https://blockgeeks.com/guides/what-is-tezos/](https://blockgeeks.com/guides/what-is-tezos/)
* Arthur Breitman explained [baking on a high-level in the following blog post](https://medium.com/tezos/its-a-baker-s-life-for-me-c214971201e1) very coherently
* Implemented DApps: [https://tezosprojects.com/](https://tezosprojects.com/)



