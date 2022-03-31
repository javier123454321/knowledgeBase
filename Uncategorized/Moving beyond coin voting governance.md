---
Title: Moving beyond coin voting governance
Source: 
---
Type:  [[Article]]
Author: [Vitalik Buterin](Vitalik%20Buterin.md)
Subject: [[Governance]] [[Tokenization]] [[Incentives]]
Status: [[finished]]
Abstract:
Summary:
> There are two key problems inherent to such an environment that need to be solved:
> -  **Funding public goods**: how do projects that are valuable to a wide and unselective group of people in the community, but which often do not have a business model (eg. layer-1 and layer-2 protocol research, client development, documentation...), get funded?
> -   **Protocol maintenance and upgrades**: how are upgrades to the protocol, and regular maintenance and adjustment operations on parts of the protocol that are not long-term stable (eg. lists of safe assets, price oracle sources, multi-party computation keyholders), agreed upon?
### The need for DeGov for funding public goods
Blockchains like Ethereum create 40m in value per day, yet the entire research budget of the Ethereum Foundation is around 30million per year. This is unsustainable for projects like ZCash which are one of the main drivers of public goods funding towards ZK-Proofs.
With off-chain governance, you can coordinate, but with on-chain governance, the rules are codified that a disagreement cannot create a proper 'fork', therefore a dispute and fork of  MakerDAO will lead to a loss of funds even if the most valuable players in the space go to the new direction.
## DeGov is dangerous
There are multiple attack vectors in the decentralized governance space, as outlined here:
> -   **Small groups of wealthy participants ("whales") are better at successfully executing decisions than large groups of small-holders**. This is because of the tragedy of the commons among small-holders: each small-holder has only an insignificant influence on the outcome, and so they have little incentive to not be lazy and actually vote. Even if there are rewards for voting, there is little incentive to research and think carefully about what they are voting for.
> -   **Coin voting governance empowers coin holders and coin holder interests at the expense of other parts of the community**: protocol communities are made up of diverse constituencies that have many different values, visions and goals. Coin voting, however, only gives power to one constituency (coin holders, and especially wealthy ones), and leads to over-valuing the goal of making the coin price go up even if that involves harmful rent extraction.
> -   **Conflict of interest issues**: giving voting power to one constituency (coin holders), and especially over-empowering wealthy actors in that constituency, risks over-exposure to the conflicts-of-interest within that particular elite (eg. investment funds or holders that _also_ hold tokens of other DeFi platforms that interact with the platform in question)
### Coin voting's deep fundamental vulnerability to attackers: vote buying
> **A token in a protocol with coin voting is a bundle of two rights that are combined into a single asset: (i) some kind of economic interest in the protocol's revenue and (ii) the right to participate in governance. This combination is deliberate: the goal is to align power and responsibility. But in fact, these two rights are very easy to unbundle from each other**.

Bribing makes holders of a small amount of a token to gain the benefit of a bribe attack (There is little benefit to the individual voter to vote their conscience). Explicit bribe attacks are not necessary either. You can look at Compund's ability to get the wrapped Curve token and participate in the governance of the underlying protocol.


Grokked: