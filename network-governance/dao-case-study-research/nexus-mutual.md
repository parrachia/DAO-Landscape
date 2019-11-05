---
description: Nexus Mutual governance for mutual coverage pool
---

# Nexus Mutual

Mutual coverage pool \(insurance pool against crypto losses\). Initial implementation covers risks of bugs in smartcontracts.

### Purpose of governance system:

Changes and upgrades to the systems, new products, pricing of the cover of the pools, rules about claims payments.

### Technology used

Communication: Discord

Identity: KYC whitelist, proprietary

Voting: GovBlocks

Legal entity: offchain

### Reason we chose that technology

* Key requirement was that nobody would have access to the smartcontracts. Smartcontracts execute automatically upon passing.
* When we started, none of the DAOtech platforms were running and viable. GovBlocks was our development house, and they were able to put together a DAOtech system that worked according to our requirements. We didn’t need something cool, just a working voting mechanism.

### Governed objects and mechanisms:

* Approximately 100 people are in the pool, voting is delegated to the but only 5 people have voting power.
* 1-person-1-vote.
* If a board member is not showing up to vote, the board member is replaced by the people in the pool. Most people don’t care about the governance, and nobody can take the money or power from the pool, so it’s fine to delegate to representatives.
* Anyone can make a proposal.
* Only board members can whitelist a proposal.
* Board whitelists and categorizes proposals.
* Devs and board check that proposals are impeccable because the code executes smartcontract and parameter changes automatically upon passing a vote.
* Anyone can propose. The intention is to whitelist everyone but there’s a veto power through the board. It’s centralized, but technically you need to categorize them, because they do automatically execute. It has to be set up correctly.
* Anyone can propose to replace a board member. Proposal must specify the person to be removed and the person to replace them. 

