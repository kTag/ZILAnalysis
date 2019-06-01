# ZIL Analysis

Zilliqa had generated a lot of buzz lately and a few people have expressed interest into understanding ZIL better without spending hours chasing for references. Hence I've decided to share my analysis. This is obviously not financial advice and this is a purely technical analysis.

## Overview

ZIL website (https://zilliqa.com) at first glance doesn't have much technical information about ZIL. It apparently supports thousand of transactions per seconds (what kind of transactions are we talking about here?) and that was achieved in their testnet setup with thousands of nodes. They also have a nice timeline but that's about it. Nothing technical whatsoever here.
Digging a bit further, the FAQ (https://doc.zilliqa.com/techfaq.pdf) is probably the most interesting next step. We discover that ZIL is a public blockchain focused on scalability with apparently *almost* linear scalability. They keep comparing themselves with ETH, so we can suppose they are in the same category, it's not a simple crypto currency blockchain it's a more complete smart contracts blockchain. We can also discover it's PoW based, but only to establish mining identities (!?) and to perform network sharding (which explains their high transaction volume), this is not yet in ETH but will be in ETH2.0. But PoW is not used for consensus, it's a different method that is used: optimized practical Byzantine Fault Tolerant (used by NEO and Hyperledger also). The only reference to security on the overview section is about their smart contract language called Scilla that allows for more secure smart contracts to be written. In summary Zilliqa is a public blockchain focused on dApps requiring high throughput. There is already serious contenders in the sector like EOS and TRON but they are not as decentralised as ZIL.

## Whitepaper

## Launch

Unfortunately like a lot of recent project the coin was launched for trading in March 2018 before the blockchain was actually working on Mainnet. Obviously it mooned pretty quickly and crashed as quickly. Mainnet was only launched in January 2019. See an interesting analysis from September 2018 here: https://cryptovest.com/news/zilliqa-zil-technical-analysis-why-zil-is-the-quiet-coin-to-watch-in-q4/

## Explorer

Next I like to focus on exploring the blockchain before the last and most important step, the code. You can find a ZIL block explorer here: https://explorer.zilliqa.com/home. It's hosted on the mail domain of ZIL so I suppose it can be trusted. With sharding you get 2 types of blocks, DS and transaction blocks. With a 0.00 TPS it looks like not much is happening on that blockchain. Looking at the last 10 blocks there is basically no transaction in any of them that is really worrying. From the explorer view it seems that blockchain is dead. You can also notice each block has a miner public key, that's confirming the concept of miner identity.

## Code

### Repo

### Mining




