## Background

After waiting for years and passing several tests, the Martian Aerospace Agency selected you to become part of the first human colony on Mars. As a prominent fintech professional, they chose you to lead a project developing a monetary system for the new Mars colony. You decided to base this new system on blockchain technology and to define a new cryptocurrency named **KaseiCoin**. (Kasei means Mars in Japanese.)

KaseiCoin will be a fungible token that’s ERC-20 compliant. You’ll launch a crowdsale that will allow people who are moving to Mars to convert their earthling money to KaseiCoin.

## Files

Download the following files to help you get started:

[KaseiCoin.sol](./Starter_Code/KaseiCoin.sol)

[KaseiCoinCrowdsale.sol](./Starter_Code/KaseiCoinCrowdsale.com)

## Instructions

The steps for this assignment are divided into the following subsections:

1. Create the KaseiCoin Token Contract

2. Create the KaseiCoin Crowdsale Contract

3. Create the KaseiCoin Deployer Contract

4. Deploy and Test the Crowdsale on a Local Blockchain

5. Optional: Extend the Crowdsale Contract by Using OpenZeppelin

    > **Note:** You can choose whether to complete the optional section. It’s designed to further your professional growth and development but won’t be graded as part of this assignment. If you choose to complete this section, you’ll use OpenZeppelin to extend the functionality of your crowdsale contract by adding time restrictions, refund capabilities, and a cap for the number of tokens that can be created. If you have any questions about how to complete the optional section, please reach out to your instructional team.

Note that the provided starter files for this homework assignment contain a `pragma` statement for Solidity version 0.5.0. You’ll use the starter files to complete the steps in the subsections.

In the subsections, you’ll create a fungible token that’s ERC-20 compliant. This token will be minted by using a `Crowdsale` contract from the OpenZeppelin Solidity library.

The crowdsale contract that you create will manage the entire crowdsale process. This process will allow users to send ether to the contract and receive KaseiCoin tokens, or **KAI**, in return. Your contract will automatically mint the tokens and distribute them to a buyer in one transaction.

Note that you’ll record a short video or animated GIF or take several screenshots that show the deployed contract in action.

In the `README.md` file of your GitHub repository for this homework assignment, you’ll create a section named Evaluation Evidence. In this section, you’ll share screenshots of your work from each subsection of the assignment.

# Martian Token Crowdsale
This prototype project involves three Solidity smart contracts that would allow people moving to Mars to convert their earthling money to a proposed new cryptocurrency named KaseiCoin. The KaseiCoin would be an ERC-20 compliant fungible token, and the currency conversion would be accomplished through a crowdsale.  

## Technologies
The technologies required to use this project are: 


[Remix IDE](https://remix.ethereum.org/) - Remix IDE is an open source web and desktop application. It fosters a fast development cycle and has a rich set of plugins with intuitive GUIs. Remix is used for the entire journey of contract development as well as act as a playground for learning and teaching Ethereum.

[MetaMask](https://metamask.io) - MetaMask is a free web and mobile crypto wallet that allows users to store and swap cryptocurrencies, interact with the Ethereum blockchain ecosystem, and host a growing array of decentralized applications (dApps). 

[Ganache](https://https://trufflesuite.com/ganache) - Ganache is a personal blockchain for rapid Ethereum and Corda distributed application development. You can use Ganache across the entire development cycle; enabling you to develop, deploy, and test your dApps in a safe and deterministic environment.

## Examples
Upon deploying the KaseiCoinCrowdsaleDeployer contract, the other two contracts are also created and can be loaded using their contract addresses. 

Details of how to deploy and load the smart contracts are shown in the "Deployment" section below. 

Once the KaseiCoin and KaseiCoinCrowdsale smart contracts are loaded, users can buy new tokens for recipient addresses and check the balances of the accounts. They can also view the total supply of minted tokens, and how much wei the crowdsale contract has raised.   

**Deployment:**

In the "Deploy and Run Transactions" pane, the Injected Web3 environment rather than the JavaScript VM must be selected. Next, from the "Contract" dropdown list, the KaseiCoinCrowdsaleDeployer contract should be selected as the contract to deploy. There are three fields: Name, Symbol, and Wallet that need to be filled in before clicking the transact button to deploy the contract.

![KaseiCoinCrowdsaleDeployer_PreDeploying](Evaluation_Evidence/KaseiCoinCrowdsaleDeployer_PreDeploying.png)

Once the contract is deployed, it can be opened and the kasei_crowdsale_address and kasei_token_address can be obtained.

![KaseiCoinCrowdsaleDeployer_Deployed_2](Evaluation_Evidence/KaseiCoinCrowdsaleDeployer_Deployed_2.png)

Next, the KaseiCoin contract should be loaded by selecting the KaseiCoin contract from the "Contract" dropdown list. Then, copying and pasting the kasei_token_address into the "Load contract from Address" field, and clicking the "At Address" button.

![KaseiCoin_PreDeploying](Evaluation_Evidence/KaseiCoin_PreDeploying.png)

This screenshot shows part of the loaded KasieCoin contract.

![KaseiCoin_Deployed](Evaluation_Evidence/KaseiCoin_Deployed.png)

The KaseiCoinCrowdsale contract should be loaded similarly, by selecting the KaseiCoinCrowdsale contract from the "Contract" dropdown list, and using the kasei_crowdsale_address as shown below.

![KaseiCoinCrowdsale_PreDeploying](Evaluation_Evidence/KaseiCoinCrowdsale_PreDeploying.png)

This screenshot shows the loaded KaseiCoinCrowdsale contract.

![KaseiCoinCrowdsale_Deployed](Evaluation_Evidence/KaseiCoinCrowdsale_Deployed.png)

**Buying New Tokens:**

The KaseiCoinCrowdsale contract is used for buying new tokens. First, the user needs to enter an ether denomination amount in the "Value" field (of the Deploy and Run module), then they must enter the recipient address beside the "buyTokens" button prior to clicking the buyTokens button.

![KaseiCoinCrowdsale_Test1_Setup](Evaluation_Evidence/KaseiCoinCrowdsale_Test1_Setup.png)

Once the tokens have been purchased, the KaseiCoin contract can be used to check the balance of the account. The account address can be entered beside the "balanceOf" button, and when the button is clicked the balance is shown, as in the test example below.

![SetAccouKaseiCoinCrowdsale_Test1_Balancents](Evaluation_Evidence/KaseiCoinCrowdsale_Test1_Balance.png)

**Checking Total Supply and Amount Raised:**

In addition to checking the balance of an account, users can also view the total supply of minted tokens. To do so, the KaseiCoin smart contract must be accessed. There the "totalSupply" button can be found at the very bottom, which upon clicking will show the updated total.

The amount of wei that the crowdsale contract raised can be viewed using the KaseiCoinCrowdsale contract. The "weiRaised" button is found at the bottom. Following is a screenshot that shows the bottom of the KaseiCoin contract and the KaseiCoinCrowdsale contract. Since zero was the initial totalSupply upon deploying the contracts, the totalSupply and weiRaised will be the same after each buyTokens transaction. 

![KaseiCoinCrowdsale_Test1_TotalSupply](Evaluation_Evidence/KaseiCoinCrowdsale_Test1_TotalSupply.png)

## Contributors

Contributed by: Gregg R. Saldutti

Email: greggnyc1@gmail.com

[![Linkedin](https://i.stack.imgur.com/gVE0j.png) LinkedIn](https://www.linkedin.com/in/greggsaldutti-1701501)


---

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Copyright © 2022 #Martian Token Crowdsale

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
