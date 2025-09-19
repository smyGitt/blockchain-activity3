### Project output

vboxuser@BlockchainVM:~/didlab-activity3$ npx hardhat compile
Compiling your Solidity contracts...

Nothing to compile
vboxuser@BlockchainVM:~/didlab-activity3$ npm run deploy

> didlab-activity3@1.0.0 deploy
> hardhat run scripts/deploy.ts --network didlab

Compiling your Solidity contracts...

Nothing to compile

Deploying CampusCreditV2...
Deploy tx: 0x6068ac21782cde617ef3ad8e43aecd063a6c286570be781d597c4f7a6198ae6b
Deployed at: 0x5fbdb2315678afecb367f032d93f642f64180aa3
Block: 1n

Add this to .env:
TOKEN_ADDRESS=0x5fbdb2315678afecb367f032d93f642f64180aa3

vboxuser@BlockchainVM:~/didlab-activity3$ npm run xfer

> didlab-activity3@1.0.0 xfer
> hardhat run scripts/transfer-approve.ts --network didlab

Compiling your Solidity contracts...

Nothing to compile

Before | Me: 1000000 CAMP | You: 1000000
CAMP
transfer tx: 0xdf88b194313605159c26e48faa6ce7508b7df12d1fbc2bfd29ff3743b45d678e gasUsed: 29224
approve tx: 0xaac67aa7c65abcfaf2151427355a6a1f08924e6805ced025ec374e396066b522 gasUsed: 46409
allowance: 50 CAMP
After | Me: 1000000 CAMP | You: 1000000
CAMP
vboxuser@BlockchainVM:~/didlab-activity3$ npm run airdrop

> didlab-activity3@1.0.0 airdrop
> hardhat run scripts/airdrop.ts --network didlab

Compiling your Solidity contracts...

Nothing to compile

Airdrop: 0xaf3ee370fea0b1fe36d9306eef428fde5ff47cb8b5cb9cc8dfb0184103b2b3b4 gasUsed: 40795 fee(wei): 105783139088740
Singles total gasUsed: 29212 fee(wei): 73588333629920
Batch saved ≈ -39.65% gas vs singles
vboxuser@BlockchainVM:~/didlab-activity3$ npm run logs

> didlab-activity3@1.0.0 logs
> hardhat run scripts/logs-query.ts --network didlab

Compiling your Solidity contracts...

Nothing to compile


### Gas aware airdrop
The airdrop.ts is gas aware as it is able to measure the gas costs for distribution.
