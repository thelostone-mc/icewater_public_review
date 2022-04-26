### Description


I've added TODO within the contracts to explain small tweaks which I feel makes sense to make. This should be visible when a PR is raised from this branch to the main branch


I've gone ahead and documented most what I've understood about the contracts within this `docs/` folder

- [Controller.md](./Controller.md)
- [ErrorTracker.md](./ErrorTracker.md)
- [RewardManager.md](./RewardManager.md)
- [Token.md](./Token.md)
- [VirtualPool.md](./VirtualPool.md)



**Function which I still need to explore**

- [Controller.md](./Controller.md)
    - onRewardsClaimed
    - calculateError
    - applyError 
    - _scaleChangeWithTime
    - _updateTargetICEPrice
    - _updateSTMPrice
    - _updateCondensationRate



Currently to test if 
- contracts compile sucessfully 
- can be deployed on test network 

I've used 
- ganache + truffle (config proivided)
![Deploy](https://user-images.githubusercontent.com/5358146/165262253-81438f34-2d45-4141-ad38-4c150306f68d.gif)

- TODO : ganache + hardhat 