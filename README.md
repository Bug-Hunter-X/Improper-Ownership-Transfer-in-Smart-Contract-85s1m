# Improper Ownership Transfer in Smart Contract
This repository demonstrates a common bug in Solidity smart contracts related to ownership transfer.  The `transferOwnership` function is implemented incorrectly, leading to potential vulnerabilities and unexpected behavior.  The solution demonstrates the correct implementation, highlighting the importance of proper state variable updates.

## Bug Description
The `_transferOwnership` function updates the `owner` state variable directly, without leveraging storage updates or mechanisms that guarantee state changes are properly recorded on-chain. This can lead to various issues such as unexpected behavior, reentrancy vulnerabilities, and potential loss of funds. 

## Solution
The solution demonstrates the proper method to update the `owner` variable.  We use `owner = newOwner` to properly set the new owner of the contract. 

## How to Reproduce the Bug
1. Compile the buggy contract (bug.sol).
2. Deploy the contract to a test network.
3. Attempt to transfer ownership. Observe unexpected behavior.

## How to Use the Solution
1. Compile the corrected contract (bugSolution.sol).
2. Deploy the contract to a test network.
3. Attempt to transfer ownership. Observe the expected behavior.
