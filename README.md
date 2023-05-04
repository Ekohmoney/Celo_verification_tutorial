# Celo Verification Tutorial:

## Introduction:

[Celo](https://celo.org/) is a blockchain platform that provides a built-in identity verification system. This allows users to prove their identity without revealing personal information which makes it an ideal solution for Web3 applications that require identity verification.

In this tutorial, we will walk you through the process of using Celo's identity verification system to implement identity verification in a Web3 application.

## Pre-requisites:

To follow along, you should have a basic understanding of Web3 development and JavaScript programming language. You should also have the following tools installed on your computer:

- [Node.js](https://nodejs.org/en/download)
- The [Celo CLI](https://docs.celo.org/cli)
- [React](https://react-cn.github.io/react/downloads.html)

## Let's Get Started!:

### Step 1: Set up your development environment-

First, you need to set up your development environment. You can install the Celo CLI by running the following command in your terminal:

``npm install -g @celo/cli``  

Once you have the Celo CLI installed, you can create a new project by running the following command:

``
celo init my-project`` 

This command creates a new directory called `my-project` and sets up the basic project structure.

### Step 2: Create a Celo account-

Next, you need to create a [Celo account](https://chrome.google.com/webstore/detail/celoextensionwallet/kkilomkmpmkbdnfelcpgckmpcaemjcdh?hl=en). You can do this by running the following command:

``celo account:create``  

This command generates new private key and public address for your account.

### Step 3: Fund your account-

Before you can use your Celo account, you need to fund it with some testnet tokens. You can do this by visiting the [Celo Faucet](https://faucet.celo.org/alfajores) and entering your Celo address.

### Step 4: Set up your Web3 application-

Now that you have a Celo account and some testnet tokens you can set up your web3 application. For the purpose of this tutorial, we will use React.

You can create a new React project by running the following command:

``
npx create-react-app my-app``  

Once you have your React project set up, you need to install the `@celo/contractkit` and `web3` packages:

``
npm install @celo/contractkit web3``  

### Step 5: Import the ContractKit and initialize it with the Celo network-

Next, you need to import the ```ContractKit``` from ```@celo/contractkit``` and initialize it with the Celo network. You can do this by adding the following code to your ``App.js`` file:

``
import { ContractKit } from '@celo/contractkit'``

``const kit = ContractKit.newKit('https://alfajores-forno.celo-testnet.org')``  

This code creates a new instance of the ``ContractKit`` and initializes it with the Celo testnet.

### Step 6: Implement the Identity Verification System-

Now that you have your Web3 application set up and the ``ContractKit`` initialized, you can implement the identity verification system.

Celo's identity verification system works by using a Smart Contract called ``Attestations``. Users can request attestations from other users which are then stored on the Celo blockchain. These attestations can be used to prove identity without revealing any personal information.

To request an attestation, you can use the ``Attestations`` Smart Contract's ``request()`` method. 
This method takes two parameters: 
1. The phone number of the user requesting the attestation and,
2. The ``requestCID`` which is a unique identifier for the attestation request.

``
async function requestAttestation() {
  const phoneHash = kit.web3.utils.sha3('1234560) ``
  
## Conclusion:

Hence, the Celo verification tutorial provides a step-by-step guide on how to verify a Smart Contract on the Celo blockchain using Remix and the Celo Terminal. The tutorial covers the necessary steps involved in verifying a contract such as compiling the contract, generating the ABI and bytecode and submitting the contract for verification on the Celo Terminal. 
  
