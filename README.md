## NuCypher Protocol: Open Research 

Following mainnet launch, the NuCypher protocol – which governs participation rules, economics/incentives and collateral management (staking) – will continue to evolve. Although certain parameters and design choices are irreversible post-launch, there are a number of critical mechanisms that can be upgraded or augmented in order to improve service quality, security, economic sustainability and the general health of the network. 

The following list introduces open, protocol-related research topics in rough order of priority. **If you intend to make a formal upgrade proposal that pertains to one of these topics, it is strongly recommended that you familiarize yourself with the 'upstream' research, discussion, empirical analysis and context hosted in this repository.** To view and discuss downstream proposals, that typically correspond to an open PR, head to [NuCypher's DAO Forum](https://dao.nucypher.com/).

1. **Pricing development**
_Includes pricing structure, price points, free market dynamics and commercial engagement_.

At launch, the definition of a service unit (users charged per sharing policy, per period) will be universal, while the cost (_price point_) will fall within a global fee range, applied to all engagements between service-provider and user. However, both the service unit and price point may diversify over time through individual service-provider strategies and collective reactions to demand trends (e.g. widening the global fee range through governance). Furthermore, the protocol can facilitate or constrain the network's free market in other ways, for example via mechanisms enabling users to efficiently discover prices, or by providing a choice of service unit definitions to service-providers. 

Official references: 
- [Pricing Protocol & Economics – Overview [WIP]](https://github.com/nucypher/whitepaper/pull/9)
- [Docs: Service Fees (Pricing)](https://docs.nucypher.com/en/latest/architecture/service_fees.html)

Relevant Issues/PRs:
- [NuCypher’s “free market”](https://github.com/nucypher/protocol/issues/14)
- [Default price range in PolicyManager](https://github.com/nucypher/nucypher/issues/1567)
- [https://github.com/nucypher/protocol/issues/7](https://github.com/nucypher/protocol/issues/7)

2. **Slashing conditions and penalty calculation**

Incorrect re-encryptions can be provably detected and punished. However, the exact basis on which a service-provider is penalized (e.g. per incorrect request vs. per policy), the severity of punishment, and the inputs to the penalty calculation itself (for example, computing based on a percentage of locked stake, an absolute/universal figure, or both), are all open research questions. 

Official references:
- [Docs: The Slashing Protocol](https://docs.nucypher.com/en/latest/architecture/slashing.html)

Relevant Issues/PRs: 
- [Calculating the slashing penalty](https://github.com/nucypher/protocol/issues/12)
- [Proposal: set slashing coefficients to almost zero](https://github.com/nucypher/nucypher/pull/1951)

3. **Subsidies and service quality** 

The action required to earn subsidies (inflationary rewards) does not align perfectly with actual work performed on behalf of users, which risks some service-providers configuring their machines to execute the bare minimum required to collect the subsidy, and neglecting real service requests from users (e.g. by being offline). 

Official references:
- [NuCypher Network: Staking Protocol & Economics](https://github.com/nucypher/whitepaper/blob/master/economics/staking_protocol/NuCypher_Staking_Protocol_Economics.pdf)

Relevant Issues/PRs: 
- [Confirm activity: problem definition, threat model, analysis of potential solutions](https://github.com/nucypher/protocol/issues/16)
- [Sybil-resistant subsidies](https://github.com/nucypher/protocol/issues/13)
- [We have built a network which encourages confirmActivityBot](https://github.com/nucypher/nucypher/issues/1272)


4. **Payment tooling** 

This research area refers to upgrading the process through which users settle their bills. This includes the question of _who_ can pay on an end-user's behalf. 

Relevant Issues/PRs: 
- [A skeleton-logic proposal for another economic model of grant (probabilistic micropayments)](https://github.com/nucypher/protocol/issues/15)
- [Proposal: Policy owner <> Policy sponsor separation](https://github.com/nucypher/nucypher/issues/1492)

5. **Service-provider selection conditions**

The probability with which a service-provider is selected for a job can be leveraged as a low-risk nudge towards good behavior. 

Relevant Issues/PRs:
- [Simplify staker sampling](https://github.com/nucypher/nucypher/pull/2056)
- [Advanced worker selection conditions (sampling algorithm)](https://github.com/nucypher/protocol/issues/9)

In addition to perusing the links above, we recommend searching (using keywords) for discussions in our public Discord channels – in particular, to check if a question you have has already been answered. Note that _service-providers_ are referred to as 'Ursulas', 'stakers', 'workers' and 'proxies' in NuCypher repositories and channels.

The [mint paper](https://github.com/nucypher/protocol/tree/master/mint_paper/Mint_Paper_Protocol_Objectives.pdf) is not up to date and serves as a record of historical design objectives.
