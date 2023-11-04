# NFT-Collection-with-a-whitelist
Build an NFT collection with a whitelist using Hardhat and Solidity. Part of learnweb3.io Ethereum and Solidity Developer Course.

## Getting Started
### Please add .env file and set it up appropriately
PRIVATE_KEY="..."
RPC_URL="..."
ETHERSCAN_API_KEY="..."

For the PRIVATE_KEY variable, export it from MetaMask. Again, make sure to use an account that only has testnet funds in it, no mainnet funds, to not risk accidentally leaking a private key with real money in it. Replace the value of PRIVATE_KEY in the .env file with the key you export.

For the RPC_URL, create an account at QuickNode if you don't have one already. After creating an account, click on Create an endpoint, select Ethereum, and then select the Sepolia testnet. Continue with the process until finished, and then copy the HTTP Provider link from the dashboard there.

Replace the value of the RPC_URL variable in the .env file with the HTTP Provider link you copied.

NOTE: If you have previously set up a Sepolia endpoint on QuickNode during an earlier lesson, you can continue using that. You do not need to create a new one.

Lastly, we need an Etherscan API Key so our contract can be verified on Etherscan. You can grab an Etherscan API Key by creating an account on https://etherscan.io if you don't have one already. Once you have it, replace the value of ETHERSCAN_API_KEY in your .env file.

Now, we will install the dotenv package which will read our .env file and make it available to Node.js as an environment variable when our deployment script runs
### please install the following packages:
npm init --yes
npm install --save-dev hardhat @nomicfoundation/hardhat-toolbox
npx hardhat
npm install dotenv
npm install @openzeppelin/contracts


## Deploying
npx hardhat run scripts/deploy.js --network sepolia
npx hardhat run scripts/deploy-nft.js --network sepolia

Don't forget to edit the deploy-nft.js contract address to your whitelist.sol deployed contact address.