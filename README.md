# ZIL Analysis

Zilliqa had generated a lot of buzz lately and a few people have expressed interest into understanding ZIL better without spending hours chasing for references. Hence I've decided to share my analysis. This is obviously not financial advice and this is a purely technical analysis. I've also added paragraphs to describe what kind of steps you should take for each section if you want to research another coin.

## Overview

> ### Goal
> First step is to have a general feeling about a project, try to triage as much as you can at this level. Anything that looks unprofessional or full of lies or mistakes should just be dropped at this step. You usually start from the official web site and official blog if any. You can dig further in their social media presence but I usually don't (see "What's Missing?" section)

Zilliqa website (https://zilliqa.com) at first glance doesn't have much technical information about ZIL. It apparently supports thousand of transactions per seconds (what kind of transactions are we talking about here?) and that was achieved in their testnet setup with thousands of nodes. They also have a nice timeline but that's about it. Nothing technical whatsoever here. It doesn't tell us much about the project technical merit but it also doesn't mean it's a scam. A lot of projects are tailored for non-technical audience and so the main web site can seem poor in technical information at a first glance.

Digging a bit further, the FAQ (https://doc.zilliqa.com/techfaq.pdf) is probably the most interesting next step. We discover that ZIL is a public blockchain focused on scalability with apparently *almost* linear scalability. They keep comparing themselves with ETH, so we can suppose it's not a simple crypto currency blockchain it's a more complete smart contracts blockchain. We can also discover it's PoW based, but only to establish mining identities (!?) and to perform network sharding (which explains their high transaction volume). But PoW is not used for consensus, it's a different method that is used: optimized practical Byzantine Fault Tolerant (used by NEO and Hyperledger also). The only reference to security on the overview section is about their smart contract language called Scilla that allows for more secure smart contracts to be written. In summary Zilliqa is a public blockchain focused on dApps requiring high throughput. There is already serious contenders in the sector like EOS and TRON but they are not as decentralised as ZIL.

![FAQ]

## Whitepaper

> ### Goal
> Whitepapers are not the most relevant reference for technical analysis. They usually represent a vision that the team is aiming for without much implementation details. There is sometimes good surprises but very often it's a quick way to filter very low quality projects because of plagia or obvious lack of content

For Zilliqa (https://docs.zilliqa.com/whitepaper.pdf) we noticed the confirmation of the use of sharding, some extra details on cryptographic algorithm. It also explains the notion of leader nodes. This combined with sharding makes verifiable ownership of coins very difficult to achieve. Overall the whitepaper doesn't give much relevant information for a technical analysis of the coin but it's a serious document and clearly some effort has been made to describe an interesting vision.

![Whitepaper]

## Launch

> ### Goal
> Launch analysis are possible only if the coin has already been launched. A lot of empty scam will disappear just after the launch. Some not serious projects will slowly fade away in inactivity. And the serious ones will just start to show what they are worth. Launch analysis is I think one of the most important step. It's the first evidence of execution talent from the team behind the coin.

Unfortunately like a lot of recent project the coin was launched for trading in March 2018 before the blockchain was actually working on Mainnet. Obviously it mooned pretty quickly and crashed as quickly. Mainnet was only launched in January 2019. See an interesting analysis from September 2018 here: https://cryptovest.com/news/zilliqa-zil-technical-analysis-why-zil-is-the-quiet-coin-to-watch-in-q4/. Again nothing too bad about the launch, no major catastrophe but the trading of the coin before having a running blockchain is always controversial.

## Block Explorer

> ### Goal
> Blockchain review (I wouldn't call it analysis, it takes too long) is great when the project is already running their main chain. There is more risks in investing in a coin that doesn't have a running blockchain yet.

You can find a ZIL block explorer here: https://explorer.zilliqa.com/home. It's referenced from Zilliqa web site so I consider it can be trusted. With sharding you get 2 types of blocks, DS and transaction blocks. Looking at the blocks created in the past there is basically no transaction in the vast majority of them, that is really worrying. From the explorer view it seems that blockchain is not used. You can also notice each block has a miner public key, that's confirming the concept of miner identity. This fact alone shows that the creators didn't take into account that miners could be traced and shutdown from this information. At this stage the blockchain is not really used by anybody. **Update**: this week the actual smart contract part of the blockchain has been launched (see code review confirming this was missing). Activity might pick up so it's important to check the blockchain regularly and look for sign of activities.

![Explorer]

## Code

> ### Goal
> Code is the heart of a project. Crypto currencies are controlled 100% via software and the code is the software. You do not need to understand code to do basic analysis of the code. I'll show you metrics you can use to see how the coding is progressing. It's also possible to find very technical analysis of a project code by Googling "code review" and the name of the coin (or "code analysis")

### Development

> ### Goal
> Finding out if the coin is actively being developed, if important new features are progressing and the size and effort of the development team behind the coin.

Zilliqa repository is available here: https://github.com/Zilliqa
There is about 8 active contributors in the past month which is inline with the expectations from a small project like ZIL. Code commit is still quite active even in the past month. Some projects just stop all developments after cashing in on the token sale. This is not the case here. Looking at branches we can see interesting developments being, hopefully, worked on offline. Overall the development of Zilliqa is churning along nicely which is always sign of a serious project. I noticed also a bug bounty program which is rare for projects of this size. 

![Code]

### Mining Software

> ### Goal
> See if the software running the coin network is working properly, producing blocks as expected. It also allows to check the block explorer is not tweaked to make the coin look better. This is not only a important source of information for the analysis it also allows to verify a lot of the previous information we gathered.

The smart contract library of Zilliqa (Scilla) is based on Ocaml. This is a famously complicated environment for development. Following the installation instructions from a basic Ubuntu (this is the distribution mentioned in the system requirements) machine just fails. Either the instructions are outdated or there is some temporary glitch. To be noted: I spent well over 20h trying to get this to work and was stuck with an issue related to opam (the package manager of Ocaml). Opam official maintainer for Ubuntu was basically unreachable and other users faced the same issue before me without answers. Instructions are here: https://github.com/Zilliqa/Zilliqa/wiki/Mining. I've noticed there isn't much about Scilla in the main code, maybe it's using external libraries (not hosted in this repo) to do so. **Update**: well the smart contract part of the blockchain was not released at the time I looked at the code so that explains. It looks very different since the last release.

## What's Missing?

Smart contract analysis (Scilla): for coins with smart contract, to be done properly it's very time consuming and so I won't describe it here. Just ping me on Telegram if you really want help on this

What is implement vs vision: the best source for a quick feedback on what has been done and what remains to be done to reach the vision is usually the team behind the coin. I'll complete the analysis if I hear back from the team

Communication and marketing strategy: no interest to me, it's too easy to cheat the system

## Foreword

I won't share buying decision here, if you really think it's important I might consider. Please send me feedback through Telegram. I do not want people to just jump to the buying decision and not read anything. That's against the principle of crypto (do your research, always verify).

Information is correct as of June 2019

If you found this useful don't hesitate to tip me: 1BqQpu5x5BgzU4gc65ThRhtmsxP8va63T2 (that's BTC only)

[FAQ]: FAQ.png "FAQ Image"
[Whitepaper]: Whitepaper.png "Whitepaper image"
[Code]: Code.png "Code image"
[Explorer]: Explorer.png "Explorer image"
