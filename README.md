# **Decentralized Git-Style Storage on Blockchain**

**Estimated Time:** 3 hours

## **Overview**

In this challenge, you'll build a decentralized git-like storage system using smart contracts. The goal is to enable users to write, edit, and retrieve a YAML file stored on-chain. You may use **any EVM-based blockchain** of your choice (Ethereum, Optimism, Avalanche C-Chain, etc.) and the corresponding smart contract language should be **Solidity**.


### **Key Features**

1. **Write arbitrary data on-chain**
   - Create a smart contract that allows users to store arbitrary data (or just text, if easier).
2. **Use the smart contract as a Git backend to upload a ~10-line YAML file**
   - Implement functionality that lets an “owner” user commit a YAML file on-chain.
   - a useful example file can be found at [[example.yaml]]
3. **Allow users to fetch the YAML file**
   - Implement a way for users to retrieve the latest version of their stored YAML file. This can be a public function.
4. **Allow users to edit and push updates to the YAML file**
   - Provide a way for the "owner" user to 'commit' modifications to the file and push updates on-chain.
5. **(Bonus: Extra Credit)**
   - Optimize storage by allowing users to only store diffs instead of full YAML files.
   - Implement cryptographic signing to verify commits.
   - Like Git, use the owner's GPG key to sign/verify commits - so their default git-commit workflow remains mostly unchanged

## **Requirements**

- **Smart Contracts:**
  - Your smart contract should be deployed on a real or testnet blockchain (see below if you need a public testnet to use).
  - The contract should support storing, retrieving, and modifying the YAML file.
- **CLI or Web Interface:**
  - Implement a command-line tool or web UI that interacts with the smart contract.
  - The interface should allow users to perform the fundamental git actions: commit (owner), push (public), clone (public)
- **Code Quality:**
  - Write clean, modular, and well-documented code.
  - Include tests to verify functionality.
- **Security Considerations:**
  - Address common security concerns, such as reentrancy and gas efficiency.
  - Validate inputs to prevent invalid or malicious data from being stored.

## **Deliverables**

1. **Code Repository (GitHub)**
   - Smart contract code.
   - CLI/Web tool code (keep it simple, no need to build a full frontend, we just want some way of calling the contract functions).
   - Tests and deployment scripts.
     - we should be able to clone your repo and run `make test` without errors
2. **README.md**
   - Instructions for running and testing your solution.
   - Explanation of architectural choices.
3. **Demo (Optional)**
   - A short video showcasing your solution in action.
   - just commit and push the demo video to your submission repo in github or gitlab.

## **Evaluation Criteria**

| Category                         | Description                                                                   |
| -------------------------------- | ----------------------------------------------------------------------------- |
| **Smart Contract Design**        | Is the contract well-structured and efficient? Does it follow best practices? |
| **Functionality**                | Does the solution meet all the feature requirements?                          |
| **Security & Gas Efficiency**    | Has the candidate considered gas costs and security vulnerabilities?          |
| **Code Quality & Documentation** | Is the code clean, well-documented, and easy to understand?                   |
| **Bonus Features**               | Is diff-based storage implemented?                                            |

# Useful Info

If you need, here is a public chain RPC that you can use:

- Chain: Avalanche C-Chain (Testnet)
- ChainID: 43113
- Public RPC: <https://api.avax-test.network/ext/bc/C/rpc>
- Testnet Faucet: <https://core.app/tools/testnet-faucet/?subnet=c&token=c>
  - Note - this faucet requires that you own some (even 0.00000001) mainnet AVAX on the wallet to use it. If you need, you may provide us with your wallet address and we will send you a small amount of tokens so that you may use the faucet.

## **How to Submit**

- just send us your git repo and we will take a look! Be sure to include the demo video in the repo.
- if you would like your repo to be private, please use github and you can add the following users to the repo for review:

  - connorch
  - condaatje
  - meppsilon
  - hyperbolic-viktor
  - yquansah
  - Kaihuang724
