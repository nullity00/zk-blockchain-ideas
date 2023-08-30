# zk-blockchain-ideas

### [Delendum fellowship ideas](https://delendum.xyz/writings/2022-11-22-what-to-build-next-in-zero-knowledge.html)
### [Aayush's Ideas](https://github.com/Divide-By-0/ideas-for-projects-people-would-use#crypto-400-each)

### [0xngmi's ideas](https://github.com/0xngmi/ideas)



## Circom ideas
1. Develop a library for operations of with more than two operands.
   - Credit : [aayushg.com](https://aayushg.com/)
   - Update : [circom-circuits](https://github.com/nullity00/circom-circuits)

## Rollup ideas
1. Polygon ZKEVM as rollup on Optimism Bedrock 
   - Tweak the polygon ZKEVM in Go with L1 as Optimism Bedrock & deploy the rollup contracts on Optimism to sync it
   - Credit : Kevin Flitcher's OP Stack Presentations

## ZK Bridge ideas 

1. L2 – L2 transfer using Proof of Burn 
   - User burns tokens in Arbitrum & posts the proof of burn in Scroll for the bridge to mint tokens to the user & vice versa
   - Credit : [BTC Mirror](https://bitcoinmirror.org/)
   - Ref : [BLS PIL](https://devfolio.co/projects/bls-pil-865f)

## SNARKS in ETH

1. Confidential Token transfers with UTXO on SC level 
   - Implement Private transactions using by creating ZK-Vaults & confidential token transfers using a UTXO model.
   - state channel inside the pool itself, UTXO pool on smart contracts , exchange signed anonymous messages
   - Credit : Justin Glibert's [talk](https://youtu.be/3AOhH0mTmYM?t=2786)

## Halo2 circuit ideas 

Credit : 0xParc

1. DSL: write a language for plonkish that transpiles to halo2 library
   - IR layer for Halo2: format specification of an IR that represent chips / gadgets / halo2 circuit
   - R1CS to Halo2: Using previous IR layer and simple chips for addition & multiplication to set up a R1CS to Halo2 compiler (compiles to IR)
   - Halo2 DSL ecosystem
2. DSL design / comparisons of existing plonkish DSL designs
   - Review existing approaches (e.g. Anoma’s vampIR, Mina’s Kimchi, Orbis) and write a blogpost comparing them.
3. Transpiler from circom to halo2
   - This can be an unoptimised straight-line conversion (i.e. just addition and multiplication gates)
4. Benchmarking circuits in different toolstacks
   - Possible benchmarks: prover speed, proof size, verification time. Possible toolstacks: circom, halo2, plonky2, halo2 with KZG
6. Optimization strategies for {keccak, batch ecdsa, …} used by zkevm teams
7. Go, JS, wasm verifiers for plonkish-ipa, plonkish-kzg
8. Solidity verifier for plonkish-ipa
9. WASM port of halo2 compiler
10. plonkish-fri prover and verifier
    - build off onur’s PCS modularization on the PSE halo2 fork (”abstraction” branch)
11. aggregation of circom-r1cs and circom-plonk proofs
12. plonkish circuit for verification of fri proofs
13. tornadocash with plonkish
14. dark forest with plonkish
15. nightmarket with plonkish
16. explore PIL and think about how it could interface with halo2 / PLONKish arithmetizations
17. Support for dynamic lookup tables
18. Prohibit queries of fixed columns at non-cur rotations
19. Improve halo2 library documentation
20. Circuit fuzzing infrastructure
21. Improve halo2 library dev tooling
22. duplex sponge construction for poseidon

Credit : Axiom

23. Autonomous airdrops: Reward protocol users for previous on-chain activity via smart contract without a centralized authority. 
24. On-chain loyalty: Allow dapps to offer fee discounts or special benefits based on past usage (volume transacted, past ownership of NFTs, or governance participation). You can offer these benefits to your most loyal users... or the most loyal users of your competitors.
25. Fine-grained governance: Weights votes based on past governance participation, longer tenured token holders, or open-source contributors.
26. On-chain EigenTrust: Compute the EigenTrust algorithm for an on-chain social graph like from Lens or Attestation Station.
27. ZK eth_call: Combine Axiom storage reads with one of the Type 2 zkEVMs to prove correct execution of any view function on a state of Ethereum.
28. On-chain Eth Gas Station: Read from block headers and transactions to build a trustless on-chain gas oracle.
29. Transacted NFT floor price: Trustlessly underwrite NFT lending and derivatives with the on-chain price history.
30. Volatility oracles: Estimate on-chain volatility from AMM pools. Make sure not to get rekt by oracle manipulation!
31. Cross-chain oracles: Use Axiom storage proofs and the AxiomV1 block hash cache on L1 to read the state of any rollup from any other. The [axiom-eth](https://github.com/axiom-crypto/axiom-eth) repo will be especially useful here.
32. Proof of Sandwich: A MEV-prevention protocol where builders are slashed if a block they built includes harmful forms of MEV like sandwich attacks, trustlessly established by reading transactions and receipts.
33. Decentralized asset management: Evaluate fund manager performance based on their full portfolio trajectory with measures like Sharpe ratio or max drawdown, not just final PNL.
34. Trustlessly settled on-chain insurance: Determine failures by an objective function run on historic data. [Ante](https://www.ante.finance/) tests are an easy way to get started with this.
35. Dynamic DeFi fees and LTVs: Use historic on-chain data to change fees for AMMs or LTVs for lending protocols. You could even optimize protocol performance using ZK ML.
36. ZK-powered Generative NFTs: Mint generative art NFTs which are accompanied with a ZK proof that they were actually generated from a claimed algorithm.
37. Cairo in halo2: Write a new backend for Cairo in halo2-lib. See the spec we've written here.
38. Bitcoin script: Verify execution of programs written in [Bitcoin script](https://en.bitcoin.it/wiki/Script) in ZK. With combined with something like [Private Market](https://www.privatemarket.dev/), this could enable markets for arbitrary transaction execution on Bitcoin.
39. Data structures: Verify common data structures and serialization algorithms, including maintenance of heaps and tries, parsing JSON, SSZ, or regex, and array manipulation.
40. Virtual machines: Verify execution of different types of virtual machines in ZK.
41. Cryptographic operations: Verify execution of cryptographic primitives such as hash functions (Blake2b), polynomial commitment schemes (IPA), and signature schemes (RSA, Schnorr).
42. Numerical computation and machine learning: Verify operations including floating point arithmetic, Newton's method, linear algebra (eigenvalues/eigenvectors), and machine learning algorithms (PCA, page rank, neural networks).

## Halo2 Tooling ideas

Credit : 0xParc

1. Ecne for halo2(formal verification tool)
2. Debugging and Static Analysis
   - Halo2 needs developer tools which can guide and help developers understand what’s going under the hood.
   - For example, debugging or static analysis tool as a plugin for vscode or CLion might help developers write circuits in a safer and easier manner.
3. Optimizations & Benchmarks
   - Alongside new optimization approaches, we’ll also need benchmarks for each exploration.
   - A report tool with given test cases or tutorials and frameworks about how to write up benchmark code will be helpful for having more benchmark results and optimization explorations.
4. Make a cost.rs Debugger for Proving Speed
   - Formalize the knowledge about the number of FFTs and MSMs for each type of gate/lookup/permutation check etc as Ye explains into the cost.rs file for optimizing proving time (instead of proof size as it is right now), along with the breakdown of the # of FFTs, MSMs, and poly evaluations for each gate/lookup in my code so that developers can optimize that.






