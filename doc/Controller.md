# Controller

- is RewardsManager, ErrorTracker

## Global Variables

- _icePool (H2O <-> ICE)
- _stmPool (H2O <-> STM.)
- _dInitialSTMSupply (supply)
- _dLastTotalH2O (amount of H20 added)
- _dTargetICEPrice(ice price in H20)

## Constructor

- create pools and init variables


## initTokenRoles - public

- Grant MINTER_BURNER_ROLE to tokens
- STM contract can mint/burn STM & H20 token
- ICE contract can mint/burn  ICE & H20 Token
- Controller Contract can mint/ burn only H20 tokens

## getTargetICEPrice - public
- Returns _dTargetICEPrice

## getICEPrice - public
## getSTMPrice - public
- Returns price of token

## getICEPoolH2OSize - public
## getSTMPoolSTMSize - public
## getSTMPoolH2OSize - publuc
- Returns pool size

## previewSwapH2OForICE - public
## previewSwapICEForH2O - public
## previewSwapH2OForSTM - public 
## previewSwapSTMForH2O - public
- invoke previewSwapAB / previewSwapBA


# swapH2OForICE - public
# swapICEForH2O - public
# swapH2OForSTM - public
# swapSTMForH2O - public
- invoke swap against Pool
- emit SwapAmount

## onRewardsClaimed - internal override

## calculateError - internal override

## applyError -  internal override


_updatePoolSize

## _totalH2O - private
return sum of H20 in both pools 

## _scaleChangeWithTime

## _updateTargetICEPrice

## _updateSTMPrice

## _updateCondensationRate