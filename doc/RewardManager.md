=================
## RewardsManager
=================

### Global variables

- `meltRate` // ICE Reward Rate
- `condensationRate` // STM Reward Rate


### annualMeltRate
returns the reward rate of ICE over time

### annualCondensationRate
returns the reward rate of STM over time

### claimableH2OFromICE
returns amount of H2O from ICEToken which can be claimable by sender

### claimableH2OFromSTM
returns amount of H2O from STM Token which can be claimable by sender

### claimRewards

- checks if claims can be made from ICE/STM
- gets total amount to be claimed based on flag
- invokes mint on H2O token of calculated amount
- invoke `onRewardsClaimed`

### onRewardsClaimed
 