Restaking can extend security in different verticals, from network to middleware to application. The commonly known AVS thought experiments are L1/L2 network, Data Availability layer, rollups, shared sequencer, oracles, bridges, game chains, and IoT clusters. There are certain niche areas to build unique Solana-focused AVS. 

_(Note: these are experimental AVSs we propose, but the intention is for it to be the blueprint of how we envision the Solayer ecosystem)_

### MEV Management
Preventing MEV is an extremely difficult problem in all blockchains. Various solutions have emerged to tackle this issue, including Jito Stakenet, which auctions the blockspace on Solana and distributes the rewards to its users. Flashbots have also pushed for efforts to decentralize MEV in the Ethereum ecosystem. Decentralized sequencers are yet to see the light of day because of similar problems. Solutions like BOLD by Arbitrum have been introduced to minimize MEV but not eliminate it. We believe that a solution like Jito Stakenet can be implemented as AVS within Solayer, which means that the Solana main chain will be used for disputes, and any malicious or dishonest validator will get slashed using Solayer's unique super-majority consensus within the SVN.


### Public auctions of block space with restaking security
Within the AVS, multiple validators will be able to bid on the blockspace, and whoever bids the highest will be given the right to create the block with any transactions and order they want. If a malicious validator tries to create a block when they have lost the auction, they will be subject to slashing as all other validators/operators can attest to the fact that the malicious party has lost the auction and they can create a dispute. The dispute will get finalized with attestations from all operators and malicious parties will get slashed.

### Public auctions of MEV opportunities with restakers
Solayer validator clusters would be set up or utilized to identify MEV opportunities, such as arbitrage, liquidation, frontrunning, and sandwich attacks. These opportunities would be listed in a public auction in formats like sealed-bid, Dutch, or English auctions. Participants, likely node operators (could expand beyond) would bid using restaked SOL or network token. The winning bidder would be granted the right to extract MEV, which includes the ability to include certain transactions, reorder them, or execute specific trades. To ensure fair play, participants could be slashed for malicious behavior, and a dispute intervention mechanism would be available among node operators. Finally, the winner would execute and settle the auctioned MEV opportunities.

### MEV-Channel
An MEV-based AVS can build a communication channel between its own native “collators” that capture MEV and validators (node operators within SVN). The collators bundle transactions that capture MEV and send them directly to validators. The collators must acquire AVS’s native tokens to act honestly. Here, there is an introduction to double-sided incentive and slashing. 

### MEV-Boost
MEV-boost originally from Ethereum introduces the separation of block builders and proposers. In this design, the AVS will introduce a relay  network that includes block builders that pledge assets to compete in a marketplace to create the most profitable blocks (that includes transactions that capture MEV). They submit bids to the network indicating payments they are willing to offer for the block proposers. Block proposers (validators) then through MEV-boost get the best-proposed block. The rewards then get relayed back and distributed across all involved parties. 

### Node operator within SVN as transaction sequencer
Instead of validators, a dedicated group of node operators within the SVN network can be responsible for transaction ordering following predefined rules of the AVS, such as first-come-first-serve or gas price, and node operators get slashed if they behave maliciously. 

### Decentralized Mining Pool
Miners register to join the mining pool by connecting hardware to the network (AVS). Miners are required to stake tokens as a form of commitment. Miners contribute computational power to solve cryptographic puzzles, and the network verifies the validity of submitted shares. Miners get rewarded for solving the puzzle and discovering the block and get slashed with any malicious behavior. The rewards can be stake-weighted or computational power contributions. 

### Decentralized Carbon Credits
Within an AVS, third-party data providers can register as a node operator that verifies the true carbon impact of the electricity produced by each solar panel. Validators can also opt-in to the process of minting carbon credits, verifying their status, ownership, and history can be transparent.

### Decentralized Sequencer
Stake-Weighted Randomness of sequencer selection
While selecting validators randomly, the selection process can be weighted by the amount of stake each validator has in the network. This means that validators with a larger stake have a higher probability of being selected for transaction ordering, aligning the selection process with the security principles of PoS. 

### Decentralized GPU cluster
Decentralizing GPU clusters means allowing any entity or individual to contribute their GPUs to compute a result. This can be particularly beneficial for machine learning models, which inherently require a lot of computing power to train. This use case can be implemented as an autonomous vehicle service (AVS), running a decentralized LLM network. Instead of minting new tokens and requiring all GPU suppliers to purchase a sufficient stake before joining the network, participants can pledge their security bonds using SOL, powered by Solayer. The SVN network can then be used to resolve any disputes at a fraction of the cost. The AVS will be responsible for distributing the workload to different entities or individuals and constructing the final result. Any entity that does not perform according to the AVS rules will be subject to slashing.

### Solana as the base Data Availability layer
Solana's high throughput and low latency make it an ideal candidate for the native layer to handle data availability (DAs). The PDA and rent system can be reused as temporary proof slots for the pre-image of data to be uploaded. When the proof is verified, the data can then be erased and the rent released. Solayer aims to provide Solana-powered DA primitives for AVS.

