---
description: A guide to voting on MakerDAO governance.
---

# Essentials

MakerDAO is a decentralized governance community that enables the generation of Dai, the world’s leading decentralized stablecoin. The decentralized governance community of MakerDAO manages the generation of Dai through an embedded governance mechanism within the Maker Protocol.

Voting requires Maker \(MKR\) tokens. MKR holders have the sole authority to enact changes to the system through voting.

Voting takes place on the [Governance Portal](https://vote.makerdao.com/).

## The Voting Contract

To vote, MKR owners must "lock-up" tokens by transferring them into the Voting Contract. Votes are weighted based on the quantity of MKR locked in the contract. "Locked" MKR can be withdrawn at any time.

Voting is weighted by the amount of MKR that votes for a proposal.

### Contract Setup and Voting Costs

Voting requires a single transaction and typically costs a few cents per vote. The total amount varies depending on network congestion.

## Governance Polls and Executive Votes

**How is the voting calculated?**

For example, if 50 stakeholders hold a total of 600 MKR and vote for proposal A, while 100 stakeholders hold a total of 400 MKR and vote for proposal B, then Proposal A would win with 60% of the vote.

Notice that the number of voters is irrelevant, only the amount of MKR tokens voting for each proposal.

**What happens to my MKR when I am voting?**

MKR is locked in the Voting Contract that was set up by the voter. This MKR is only accessible with the wallet used to set up the voting contract. For a single-wallet setup, only that wallet can withdraw MKR out of the system. For a linked-wallet setup, either of the linked wallets can be used to withdraw MKR to the linked cold wallet.

### Governance Polls

Governance Polls occur on-chain and are used to measure the sentiment of MKR voters. They can be accessed through the the [Polling page](https://vote.makerdao.com/polling) in the Maker Foundation's [Governance Portal](https://vote.makerdao.com).

[Polls](https://vote.makerdao.com/polling) often run concurrently, allowing voters to participate in any number of them at the same time and some use \[instant run-off\]\([https://ballotpedia.org/Ranked-choice\_voting\_\(RCV](https://ballotpedia.org/Ranked-choice_voting_%28RCV)\)\) so you can select multiple options.z

The current schedule calls for polls to 'go live' on a weekly basis every Monday at 16:00 UTC.

MKR holders may be asked to:

* Determine governance and DAO processes outside the technical layer of the Maker Protocol.
* Form consensus on important community goals and targets.
* Measure sentiment on potential Executive Vote proposals.
* Ratify governance proposals originating from the MakerDAO forum signal threads.
* Determine which values certain system parameters should be set to before those values are then confirmed in an executive vote.
* Ratify risk parameters for new collateral types as presented by Risk Teams.

Here is an example of voting in action in the Governance Portal:

![An example of Governance Polling](https://github.com/blimpa/maker-operational-manual/tree/0fa13385ea5d0f81640f54a58ba46c759fe926a7/images/voter-58.png)

#### How long is the voting period of a Governance Poll?

The voting period of a given Governance Poll varies. Recurring polls of the same type are usually standardized and have the same duration.

The most common are three and seven day periods. Concurrently running polls do not necessarily have the same voting periods.

#### Where can I find on-chain Governance Polls?

Live polls can be found on the [Polling page](https://vote.makerdao.com/polling) in the [Governance Portal](https://vote.makerdao.com). Historic poll data can be found at the [Maker Governance Analytics Dashboard](https://mkrgov.science/).

User risks can be mitigated by using small test amounts beforehand and by thoroughly checking which addresses one is interacting with.

#### How to create an on-chain Governance Poll?

Anyone can create an on-chain Governance Poll using the polling smart contract, however, there is no UI provided to do this yet.

Currently, only the elected Governance Facilitator\(s\) are able to put up polls that display on the [Governance Portal](https://vote.makerdao.com), polls created by arbitrary Ethereum addresses **are not** displayed.

In the future, the MKR token holders or any third parties may want to develop special UIs or other voting frontends.

### Executive Votes

Executive Votes occur on-chain and can be accessed through the [Executive page](https://vote.makerdao.com/executive) in the Maker Foundation's [Governance Portal](https://vote.makerdao.com).

Executive Votes "execute" technical changes to the Maker Protocol. When active, each Executive Vote has a proposed set of changes being made on the Maker Protocol's smart-contracts.

Unlike the other types of votes, Executive Votes use a 'Continuous Approval Voting' model.

Executive Vote can occur at any time, however the current schedule calls for Executive Votes to go live on Fridays 12pm EST/9am PST/14:00 UTC

Executive Votes can be used to:

* Add or remove collateral types.
* Add or remove Vault types.
* Adjust global system parameters.
* Adjust Vault-specific parameters.
* Replace modular smart contracts.

Anyone can create an on-chain Executive Vote using the MakerDAO governance contracts, however, there is no non-technical UI available to do this.

Users can create proposals, also known as "[Slates](https://docs.makerdao.com/smart-contract-modules/governance-module/chief-detailed-documentation)," through this [experimental portal](https://chief.makerdao.com/), or by interacting directly with the smart contracts.

Here is an example of an executive vote on the Governance Portal:

![An example of Executive Vote](https://github.com/blimpa/maker-operational-manual/tree/0fa13385ea5d0f81640f54a58ba46c759fe926a7/images/voter-59.png)

#### Continuous Approval Voting

Continuous Approval Voting means that competing proposals may be introduced any time.

The Executive Vote represents the current state of the system and is therefore continuously active.

There are three aspects to consider with regard to Continuous Approval Voting:

* A vote creates a barrier for new proposals, since new proposals need to surpass the voting weight of the last successful proposal.
* Votes are meant to remain in the system continuously in order to prevent bad proposals from passing easily.
* The more votes there are on the current state of the system, the more secure the system generally is from any "rogue" proposals.

With Continuous Approval Voting, the continuity of staked votes challenges and reinforces the status quo of the system through movements of the majority of votes between the most recent successful proposal and new proposals.

If MKR token holders do not agree with a new proposal, then they may cast their votes for the current state of the system \(or leave MKR there if they were already voting for the current state\), implying that they do not want to see anything changed.

To revert a change in the system an entirely new proposal must be put forth. It is impossible to reactivate an old proposal.

#### Auditability

**With regard to new votes**

The public is encouraged to self-audit the code for each vote.

There is a guide on how to do so found [here.](https://github.com/blimpa/maker-operational-manual/tree/0fa13385ea5d0f81640f54a58ba46c759fe926a7/learn/governance/audit-exec-spells/README.md)

The team creating these votes has been putting in significant effort to make it easy for non-technical people to audit the code by adding many explanatory notes within the code itself.

**With regard to a user's voting record**

The voter's current vote is displayed on a given proposal page in the [Governance Portal](https://vote.makerdao.com/). Another alternative is to check third-party tools like [mkrgov.science](https://mkrgov.science) that collect voting data and even offer a [voting history lookup tool](https://mkrgov.science/voting-history).

