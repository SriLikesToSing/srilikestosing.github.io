---
layout: post
title: The Cryptocurrency Rabbit Hole
---

I really wanted to create my own cryptocurrency completely from scratch (releasing soon). So I had to reason from first principles in order to create a 
knowledge tree about everything from Ledgers, cryptographic hash functions to P2P architecure. 


- Want to build a currency without a central authority or a middle man processing and regulating
- What is a currency?
     - a medium of change of value
         - hypothetically a goat thats priced at $300 will likely be bought with the amount of currency if a peron
            values it to be worth >= $300
         - it is a concrete way of showing you have value with you to everyone without fraud(well if majority are good actors)
- What is the difference between paypal and bitcoin?
     - Both are similar in that both can send payments digitally
     - One is a central figure while one is decentralized
        - Bitcoin lets you do whatever you want basically
-  How does paypal and banks avoid double spending?
    - once the money is spent you dont have the money to replicate and spend the same money again.
         -ex1: giving a 15 dollar bill to buy pasta
             - you cant duplicate it because of the fact that you dont have a copy of it or anything similar
                with you.
         - The central authority keeps track of the first transaction with that certain coin and determines
- how does a cryptocurrency avoid double spending?
    - you need to keep track of all the transactions to see which coin has been spent where
         - A ledger of sorts
             - Since you cant depend on a central authority you must publicise the transaction it to everyone
                 - We need the "majority" of the CPU holders to agree this was the history of the order of the transaction of the coin
                 - add a time component?
                     - Timestamp Server (https://en.wikipedia.org/wiki/Trusted_timestamping)
                         - takes a hash of a ledger or "block" and publicises the hash so that people know
                             - How do people know? Which hash should they trust? Which block should they add as the final official transaction?
                                 - proof of work
                                     - solve a computational math problem and if you can you are given approval
                                        to add a block (list of transactions at a given time) to the blockchain
                                these n transactions took place during this time
                                     - the hash also includes the hash of the previous time stamp to it forms a sort of
                                        chain of blocks
                    - How a new block is added to the chain
                         - New transaction is brodcasted to all nodes
                         - Each node collects new transactions into a block
                         - Each node wokrs on finding a difficult proof-of-work for its block.
                         - When a node find a proof-of-work, it brodcasts the block to all nodes
                         - Nodes accept the block only if all transactions in it is valid
                             - valid means checking the double spending problem since now we have the time metric
                         - Nodes accept this block if people build off of this block
                            - You cannot go back if you build off



- How does paypal or banks determine scams such as someone claiming someone needs to pay them $50 when in reality they havent?
    - they have internal accounts and systems in place
        - some signature system whether its accounted by a credit card or debit card

- How does a cryptocurrency determine scams? (especially on a ledger)
     - You need a really secure approval that says you approve a transaction of you sending the payment.
         - This gets rid of the risk of someone saying you need to pay someone without your approval
         - Also only allow payments which your input is still reamins a value greater than 0
        - Can't someone copy the digital signature because of its inheriant properties?
             - cryptography to the rescue

- How can someone hack a central transaction system such as paypal or a bank or get more money then there should?
     - You can hack its systems and take money
     - You can divert payments to yourself
     - Social engineering
     - Fake money/Black money

- How can someone hack a cryptocurrency?
     - know a private key of a certain user
     - know the wallet account for a certain person

     - If Nodes are immune to false info and generation of coins from thin air is there any other way?
         - the only other way is to take back money he recently spent getting value for free

         - You can double spend by spending coins before you have above 51% cpu and then once u have 51% cpu
            add a new fork to the time when u didnt spend those coins and then u can easily spend coins again
                - can other people also benefit from this?
                     - they possibly can if they coincidentally have the same situation as him

- What architecture does a cryptocurrency use?
     - A P2P (peer to peer network)
        - each node in the network has its own private copy of the blockchain
             - Unless you are SVP which only has the top of the merkel tree (assuming)
        - A bitcoin network node consists of
          - Wallet component
          - Miner
          - Copy of blockchain im assuming?
          - Network Routing
          - There is also a thing called a "Full Node"


        - Simplified Payment Verification Nodes
          - Do not use the full blockchain with every single transaction in each block but rather
                hash a merkel tree header for each block and then can use other nodes which ahve a specific
                transaction it is looking for and can pinpoint it traversing the merkel tree

        - What infrastructure can we use to impliment this network?
             - libp2p seems to be as of 11/28/2020 the choice
             - Our cryptocurreny is going to be implimented in go a/f 11/28/2020

