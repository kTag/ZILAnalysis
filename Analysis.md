# ZIL Analysis

Zilliqa had generated a lot of buzz lately and a few people have expressed interest into understanding ZIL better without spending hours chasing for references. Hence I've decided to share my analysis. This is obviously not financial advice and this is a purely technical analysis.

## Overview

Zilliqa website (https://zilliqa.com) at first glance doesn't have much technical information about ZIL. It apparently supports thousand of transactions per seconds (what kind of transactions are we talking about here?) and that was achieved in their testnet setup with thousands of nodes. They also have a nice timeline but that's about it. Nothing technical whatsoever here.
Digging a bit further, the FAQ (https://doc.zilliqa.com/techfaq.pdf) is probably the most interesting next step. We discover that ZIL is a public blockchain focused on scalability with apparently *almost* linear scalability. They keep comparing themselves with ETH, so we can suppose they are in the same category, it's not a simple crypto currency blockchain it's a more complete smart contracts blockchain. We can also discover it's PoW based, but only to establish mining identities (!?) and to perform network sharding (which explains their high transaction volume), this is not yet in ETH but will be in ETH2.0. But PoW is not used for consensus, it's a different method that is used: optimized practical Byzantine Fault Tolerant (used by NEO and Hyperledger also). The only reference to security on the overview section is about their smart contract language called Scilla that allows for more secure smart contracts to be written. In summary Zilliqa is a public blockchain focused on dApps requiring high throughput. There is already serious contenders in the sector like EOS and TRON but they are not as decentralised as ZIL.

## Whitepaper

Whitepapers are not the most relevant reference for technical analysis. They usually represent a vision that the team is aiming for without much implementation details. Fot Zilliqa we notice the confirmation of the use of sharding, some precise details on cryptographic algorithm. It also explains the notion of leader nodes. This combined with sharding makes verifiable ownership of coins very difficult to achieve. Overall the whitepaper doesn't give much relevant information for a technical analysis of the coin.

## Launch

Unfortunately like a lot of recent project the coin was launched for trading in March 2018 before the blockchain was actually working on Mainnet. Obviously it mooned pretty quickly and crashed as quickly. Mainnet was only launched in January 2019. See an interesting analysis from September 2018 here: https://cryptovest.com/news/zilliqa-zil-technical-analysis-why-zil-is-the-quiet-coin-to-watch-in-q4/

## Block Explorer

Next I like to focus on exploring the blockchain. You can find a ZIL block explorer here: https://explorer.zilliqa.com/home. It's hosted on the mail domain of ZIL so I consider it can be trusted. With sharding you get 2 types of blocks, DS and transaction blocks. Looking at the blocks created in the past there is basically no transaction in the vast majority of them, that is really worrying. From the explorer view it seems that blockchain is not used. You can also notice each block has a miner public key, that's confirming the concept of miner identity. This fact alone shows that the creators didn't take into account the fact that miners could be traced and shutdown from this information. At this stage the blockchain is not really used by anybody

## Code

### Development

Zilliqa repository is available here: 
There is about 8 active contributors in the past month which is inline with the expectations from a small project like ZIL. Code commit is still quite active even in the past month. Some projects just stop all developments after cashing in on the token sale. This is not the case here. Looking at branches we can see interesting developments being, hopefully, worked on offline. Overall the development of Zilliqa is churning along nicely which is always sign of a serious project. I noticed also a bug bounty program which is rare for projects of this size. 

### Mining Software

The smart contract library of Zilliqa (Scilla) is based on Ocaml. This is a famously complicated environment for development. Following the installation instructions from a basic Ubuntu (this is the distribution mentioned in the system requirements) machine just fails. Either the instructions are outdated or there is some temporary glitch. To be noted: I spent well over 20h trying to get this to work and was stuck with an issue related to opam (the package manager of Ocaml). Opam official maintainer for Ubuntu was basically unreachable and other users faced the same issue before me without answers. Instructions are here: https://github.com/Zilliqa/Zilliqa/wiki/Mining.

## What's Missing?

Smart contract analysis (Scilla) => time consuming and not significant
What is implement vs vision => talk to the team
Communication and marketing strategy: no interest to me

## Foreword

No buying decision shared here
Verify make your own opinion
PR welcome (or change requests by email)
Information is correct as of June 2019, use links to see if anything has changed


