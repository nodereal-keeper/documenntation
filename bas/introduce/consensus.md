# Consensus

Although Proof-of-Work (PoW) has been recognized as a practical mechanism to implement a decentralized network, it is not friendly to the environment and also requires a large size of participants to maintain the security. Ethereum and some other blockchain networks, such as MATIC Bor, TOMOChain, GoChain, xDAI, do use Proof-of-Authority(PoA) or its variants in different scenarios, including both testnet and mainnet. PoA provides some defense to 51% attack, with improved efficiency and tolerance to certain levels of Byzantine players (malicious or hacked). It serves as an easy choice to pick as the fundamentals.&#x20;

Meanwhile, the PoA protocol is most criticized for being not as decentralized as PoW, as the validators, i.e. the nodes that take turns to produce blocks, have all the authorities and are prone to corruption and security attacks. Other blockchains, such as EOS and Lisk both, introduce different types of Delegated Proof of Stake (DPoS) to allow the token holders to vote and elect the validator set. It increases decentralization and favors community governance.

&#x20;BNB Sidechain template proposes to combine DPoS and PoA for consensus, so that:&#x20;

1.Blocks are produced by a limited set of validators&#x20;

2.Validators take turns to produce blocks in a PoA manner, similar to Ethereum’s Clique consensus design

3.Validator set are elected in and out based on a staking based governance&#x20;

4\. The implement of the consensus engine is named as Parlia and to clarify some terms:&#x20;

&#x20;        4.1 Epoch block. Consensus engine will update ActiveValidators contract periodically. If now the period is 200 blocks, a block is called epoch block if the height of it is times of 200.&#x20;

&#x20;         4.2 Snapshot. Snapshot is an assistant object that help to store the validators and recent signers of blocks.
