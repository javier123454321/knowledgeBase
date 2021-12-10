- [[Gratitude List]]
- [[Quick Capture]]
    - [[Rollups]] [[Ethereum]]
        - **Rollups move computation (and state storage) off-chain, but keep some data per transaction on-chain**
        - How it works
            - You have a merkle state tree, and you store a hash of the current state root R0. 
            - Anyone publishes a batch of transactions R1 along with the previous state root R0
                - the contract ensures that R0 === R0,  then the stored hash in the contract moves to R1
                - Now how to prove that the hash is legitimate
                    - Optimistic and Zero Knowledge rollups
                        - Optimistic rollups rely on someone challenging a validator that procesed a malicious transaction. Once a transaction is posted, it is assumed benevolent until challenged, it gets rolled up, then posted after x amount of time. 
                    - 
- [[Habits]]
    - {{[[table]]}}
        - Habit::
            - Notes::
        - [ ] Meditate
        - [ ] Exercise
        - [ ] Read a book
        - [ ] Write
- [[Reflection]]
    - [[Do [[DSRP]] model on two distinct objects]]
    - [[What did I learn]]
    - [[What could be better?]]