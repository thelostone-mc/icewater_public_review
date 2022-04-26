
==================================
# ERC20MintableBurnable
==================================

- inherits ERC20.sol
- inherits AccessControlEnumerable.sol

## Constructor
- set default admin role

## decimals
- returns 18

## mint
- invoked only by minter
- mints value to the account

## burn
- invoked only by minter
- burns value from account


=================
# ERC20Reward
=================

- inherits ERC20MintableBurnable

## Global Variable 
- _iLastRewardTimes (timestamp of last invacation of _Reward)
- _dClaimableReward (stores claimable amount)



## Constructor
- set default admin role


## _newReward - internal view
- how much new reward is due since last update for an address

## _reward - internal
- set _iLastRewardTimes[address] to block.timestamp
- invoke _newReward to know how much to reward address
- set that value to _dClaimableReward[address]
- emit Reward event


## _beforeTokenTransfer
- decides which address should the _reward be invoked


## claimableReward - public
- detemines amount of reward + new reward  for an address


## claimReward - public
- invokes _reward
- get claimable reward
- reset claimable reward in _dClaimableReward
- emit ClaimReward


=================
## IceWaterTokens
=================

- Comprises of 3 token 
    - Ice token     (Stable)
    - H2O token     (Liquid currency)
    - Steam token   (Speculative Asset)

=================
### IceToken
=================

- is ERC20Reward
- On deploy , the deployer address is set as admin of the ICE Token

### _afterTokenTransfer

- charges a burn tax on ICT tokens after transfer


=================
### H2O Token
=================

- is ERC20MintableBurnable
- On deploy , the deployer address is set as admin of the ICE Token



=================
### SteamToken
=================

- is ERC20Reward
- On deploy , the deployer address is set as admin of the ICE Token