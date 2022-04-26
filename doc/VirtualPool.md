# VirtualPool

- is ReentrancyGuard, Ownable

## Global variables
- ERC20MintableBurnable tokenA
- ERC20MintableBurnable tokenB
- poolSizeA
- poolSizeB

## priceA - public
- return poolSizeB /  poolSizeA

## setPriceA - public
- only Owner
- increase poolSize A

## priceB - public
- return poolSizeA /  poolSizeB

## setPriceB - public
- only Owner
- increase poolSize B

## scalePools - public
- only Owner
- increase both pool by a multipler 

## previewSwapBA - public
- invoke calcSwapAmount

## previewSwapBA - public
- invoke calcSwapAmount


## swapAB - public
- check is sender has enough balance
- invoke calcSwapAmount to get dAmountB
- invoke swap


## swapBA - public
- check is sender has enough balance
- invoke calcSwapAmount to get dAmountA
- invoke swap


## swap - private
- burn tokens being sent
- mint tokens to be rewarded

## calcSwapAmount - private
- return how much tokens to be swapped