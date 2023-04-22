# Project Title

ETH Proof Assessment - this code program runs the smart contract for the token NFTs.

## Description

This Assessment aims to create a newly created smart contracts and edit your own token NFTs inside it, it is written on Solidity Language using the online Remix - Ethereum IDE (website link: https://remix.ethereum.org/) This code are simple and easy to learn even the beginner can use or study this for future purposes. Especially, for the future of the web3.


## Getting Started

### Executing program

The first requirement to run this program is to use Remix Ethereum IDE (https://remix.ethereum.org/) and create a new files and take note that ".sol" is the correct file format for running a Solidity Program

This code consists of creating a new token for smart contracts. It is named as FLIPCOIN and labeled as FLP as an example for the created currency name. It has 3 Functions (Mapping, Mint and Burn) Mapping means a set of hash tables/parameters to store a type of data collection and key value pairs. Next is the Mint function which is a process where you can transact and create your own set of amount for your own NFT, it is validated on the blockchain to create a new asset and store your own data and last is the Burn Function same as you will delete or remove a selected type of data and amount it can effectively removes your tokens from the available supply.

``` pragma solidity 0.8.18;

contract TokenAssessment {
    // public variables here
        string public title = "FLIPCOINS";
        string public label = "FLP";
        uint public TotalTokens = 0;

    // mapping variable here
        mapping(address => uint) public balance;

    // mint function here
        function mint (address adrs, uint value) public {
        TotalTokens += value;
        balance[adrs] += value;
        }

    // burn function here
        function burn(address adrs, uint value) public {
            if(balance[adrs] >= value){
                TotalTokens -= value;
                balance[adrs] -= value;
            }
        }
}

```

## Additional Information

Student Info and Email address

Flores, John Nico M.
National Teachers College - BSIT 2.3
422003560@ntc.edu.ph
