# Lottery Smart Contract (Solidity)

## Overview

This project is a decentralized Lottery Smart Contract built using Solidity.

Players can enter the lottery by sending ETH, and the manager selects a random winner who receives the entire contract balance.

## Features

* Only manager can pick winner
* Minimum entry fee (1 ETH)
* Prevents duplicate entries
* Uses pseudo-random selection
* Secure ETH transfer using `call`
* Event logging for transparency

##  Concepts Used
* `require` (validation)
* `payable` (ETH handling)
* `call` (ETH transfer)
* `keccak256` (randomness logic)

## Workflow

1. Manager deploys contract
2. Players enter by sending ≥ 1 Ether
3. Each player can enter only once
4. Manager calls `pickWinner()`
5. Random winner receives total balance
6. Contract resets for next round

##  Limitations

* Randomness is not secure (uses block data)
* Not suitable for production use
* Can be improved using Chainlink VRF

##  How to Test

* Deploy contract in Remix
* Use multiple accounts to call `enter()`
* Send ≥ 1 ETH
* Call `pickWinner()` from manager account

##  Future Improvements

* Integrate Chainlink VRF for secure randomness
* Add frontend (React + Ethers.js)
* Deploy to testnet (Sepolia)

## Author

Built as part of my Web3 learning journey 

