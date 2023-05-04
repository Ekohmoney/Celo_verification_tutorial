# Celo_verification_tutorial
## Introduction
Celo is a blockchain platform that provides a built-in identity verification system. This system allows users to prove their identity without revealing personal information, making it an ideal solution for web3 applications that require identity verification.

In this tutorial, we will walk through the process of using Celo's identity verification system to implement identity verification in a web3 application.

## Prerequisites
To follow along with this tutorial, you should have a basic understanding of web3 development and the JavaScript programming language. You should also have the following tools installed on your computer:

- Node.js
- The Celo CLI
- React
### Step 1: Set up your development environment
First, you need to set up your development environment. You can install the Celo CLI by running the following command in your terminal:

``npm install -g @celo/cli``  

Once you have the Celo CLI installed, you can create a new project by running the following command:

``
celo init my-project`` 

This command creates a new directory called `my-project` and sets up the basic project structure.

### Step 2: Create a Celo account
Next, you need to create a Celo account. You can do this by running the following command:

``celo account:create``  

This command generates a new private key and public address for your account.

### Step 3: Fund your account
Before you can use your Celo account, you need to fund it with some testnet tokens. You can do this by visiting the [Celo Faucet](https://faucet.celo.org/alfajores) and entering your Celo address.

### Step 4: Set up your web3 application
Now that you have a Celo account and some testnet tokens, you can set up your web3 application. For the purposes of this tutorial, we will use React.

You can create a new React project by running the following command:

``
npx create-react-app my-app``  

Once you have your React project set up, you need to install the `@celo/contractkit` and `web3` packages:

``
npm install @celo/contractkit web3``  

### Step 5: Import the ContractKit and initialize it with the Celo network
Next, you need to import the ```ContractKit``` from ```@celo/contractkit``` and initialize it with the Celo network. You can do this by adding the following code to your ``App.js`` file:

``
import { ContractKit } from '@celo/contractkit'``

``const kit = ContractKit.newKit('https://alfajores-forno.celo-testnet.org')``  

This code creates a new instance of the ``ContractKit`` and initializes it with the Celo testnet.

### Step 6: Implement the identity verification system
Now that you have your web3 application set up and the ``ContractKit`` initialized, you can implement the identity verification system.

Celo's identity verification system works by using a smart contract called ``Attestations``. Users can request attestations from other users, which are then stored on the Celo blockchain. These attestations can be used to prove identity without revealing personal information.

To request an attestation, you can use the ``Attestations`` smart contract's ``request()`` method. This method takes two parameters: the phone number of the user requesting the attestation, and the ``requestCID``, which is a unique identifier for the attestation request.

``
async function requestAttestation() {
  const phoneHash = kit.web3.utils.sha3('123456``
