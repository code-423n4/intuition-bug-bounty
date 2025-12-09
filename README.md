# Welcome to your bounty repo

This file contains information around how to set-up your README.md and prepare for our collaboration.

**Bug Bounties use two repos**:

- a bug bounty repo (this one), which is used for scoping your bug bounty and for providing information to wardens
- a submissions repo, where issues are submitted

Ultimately, when we launch the bug bounty, this repo will be made public and will contain links to the in-scope files to be reviewed and all the information needed for bounty participants.

**Action item for sponsors:**

- [ ] Modify the contents of this README.md file. Describe how your code is supposed to work with links to any relevent documentation and any other criteria/details that the C4 Wardens should keep in mind when reviewing.

# Intuition Bug Bounty

## Award levels
| Risk Score |  Payout |
|------------|---------|
| Critical | Up to $100,000 in USDC (depending upon severity and amount of funds at risk, at discretion of Intuition team) |
| High| $3,000 - $5,000 in USDC |
| Medium| $1,000 - $2,500 in USDC |
| Low | $250 - $500 in USDC |

## Background on Intuition

### What is Intuition?

Intuition is an Ethereum-based attestation protocol that makes it easy to create, explore, and incentivize verifiable information. It focuses on a flexible data layer for Web3 where many-to-one relationships between identities and claims are supported and token-based incentive mechanics encourage high-quality data creation. Intuition's flagship app, Portal, enables users to create, navigate, aggregate, and curate attestations about people and entities in the Web3 ecosystem.

### How does it work (high-level)?

- Intuition creates unique identifiers for people/organizations/concepts/etc (known as "atoms"), and semantic triple claims constructred from those identifiers (known as "triples") on-chain.
- Users can deposit into the "MultiVault" contract to support or oppose atoms and triples. The value of the user's deposit increases or decreases when subsequent users deposit or withdraw from the same vaults, according to various bonding curves.
- Users can stake TRUST to receive protocol emissions each epoch, depending upon their personal utilitzation of the Multivault and the system utilization of all users combined.
- All smart contracts are deployed to the Intuition Network, an EVM-compatible L3, manage the attestation and incentive logic, using $TRUST token as the native currency

### Further technical resources & links

- **Website:** https://intuition.systems
- **Documentation:** https://www.docs.intuition.systems/
- **Whitepaper:** https://cdn.prod.website-files.com/65cdf366e68587fd384547f0/66ccda1f1b3bbf2d30c4f522_intuition_whitepaper.pdf
- **Discord Community:** https://discord.gg/0xintuition
- **X:** https://x.com/0xIntuition

# Scope & Severity Criteria

## Severity matrix:

| Severity level | Description / Examples |
|---|---|
| **Critical** |  Systemic user fund loss or freezing; unauthorized manipulation of critical contract parameters (timelock, pausability); mass-scale unauthorized mint/burn of multivault shares; protocol insolvency. |
| **High** | Direct theft of individual user funds; long-term freezing of individual user funds; ways to avoid expected fees. |
| **Medium** | Economic loss not involving direct on-chain asset theft (short-term freezing, gas griefing, unbounded gas, essential functionality temporarily unusable); theft of unclaimed rewards/yield. |
| **Low** | Behavioral differences from intended behavior or documentation where no funds are at risk; technical issues that lead to impersonation of Intuition team communications; minor logic/documentation mismatches; non-critical edge cases. |

## Smart Contracts and Repos in Scope

- **Smart Contract Sources:** https://www.docs.intuition.systems/docs/developer-tools/contracts/deployments
- **Mainnet Deployed Contract Commit:** `20181c162502da226ca25c31aef47872369212c9`
- **Repos:**
  - https://github.com/0xIntuition/intuition-rs
  - https://github.com/0xIntuition/intuition-ts

## Out-of-Scope

[⚡️ **Project Name**] Any OOS issues? 

### Known Issues

- Any issues already documented in previously opened issues, previous audits, or otherwise publicly-known vulnerabilities are **out-of-scope** for bounty rewards (reports duplicating those issues will not be paid).
- This includes issues intentionally left as design choices or mitigated operationally by the team.

### Previous audits

Any findings already reported in previous audits are not eligible for new rewards.
- https://www.docs.intuition.systems/docs/developer-tools/audit-reports

[⚡️ **Project Name**] previous audits can be found below: [Please insert a link to your previous audits.]

### Specific types of issues excluded

- Informational findings (no economic or security impact)
- Design choices documented and accepted by the protocol (e.g., permissioned/centralized upgradeability) unless they lead to a concrete exploit scenario
- Front-end only user errors or UX mistakes that do not lead to contract-level risk
- Rounding differences that have no economic impact
- Known gas consumption characteristics (unless they enable an exploit)

# Additional Context

### Trusted Roles

[⚡️ **Project**: Please explain your protocol's trusted roles.]

### Miscellaneous
Employees of Intuition and their family members are ineligible for bounties.
