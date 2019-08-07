---
description: Betoken has 2 governance systems for their decentralized hedge fund
---

# Betoken

Betoken is a decentralized hedge fund.

### **Purpose of governance system:**

**2 DAO systems are implemented**

* Management: Investments for a decentralized hedge fund based on meritocracy \(reputation\)
* Upgrade: Decisions on smartcontract code changes

### **Technology used**

*  Communication: Telegram
* Voting: Proprietary
* Reputation: Proprietary

### **Reason we chose that technology**

We had specific needs and wanted to include a very specific definition of reputation and create our own mechanisms for the specific attack vectors we might encounter in our specific app.

### **Governed objects and mechanisms:**

**Management of funds.**

* Every fund manager managed a percentage of the funds based on their percentage of the reputation.
* Maximum reputation per user is 10%.
* No identification method is used currently, so feasibly someone could have multiple accounts, but nobody has near 10%.
*  You can become a manager at any time by purchasing tokens, and investing those funds you invest. Maximum start is 1% of pool.
* Reputation goes up and down according to how your investments perform relative to other investment managers. Reputation is managed qualitatively by the system smartcontracts based on actual performance.
*  Fund managers are rewarded 20% of profit, plus 0.1% management fee.

**Management of code upgrades**

*  Upgrades are pushed in a 30-day cycle, divided into 10 3-day blocks.
* In the first block, the fund Manager with the highest reputation is called upon to propose an upgrade. The upgrade candidate could be from the core team or from a different team.
* Anyone can propose an upgrade candidate, but the one that will be voted on first is based on the reputation of the manager making the proposal. If someone proposes a candidate and nobody of a higher rank makes an alternative proposal, that is the proposal voted on.
* During those 3 days, the proposal must get a majority vote of a quorum of 10% of the managers to be approved as the proposed candidate.
* If the proposal doesn’t pass, the \#2 fund manager is requested to propose an upgrade candidate, and the same process repeats, and so on. 0
*  During the voting period, everyone has the chance to review the release candidate and vote. This is important because an approved candidate automatically executes in code at the end of the voting period.
* 9 days before the end of the voting period, the voting ends and all participants in the fund can check the decision and if they want, withdraw their funds. This allows anyone who thinks the code is not in their interest to get out of the pool, so decisions are never forced on tokenholders. They have time to get out.
* During the last 3 days of the 30-day period, managers can push code to release, based on a majority vote.
* Anti Sybil-attack feature: For voting, the manager’s reputations from 90 days prior to the vote is the relevant reputation used, so new users can’t suddenly game the system.
* Reputation for proposing releases is from the active manager with the top reputation, meaning this is someone who has made proposals in the past. If someone is silent for a long period, they do not get considered as someone who is relevant for proposing a candidate.

