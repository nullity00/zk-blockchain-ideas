# zk-blockchain-ideas

[delendum ideas](https://delendum.xyz/writings/2022-11-22-what-to-build-next-in-zero-knowledge.html) | [Aayush's Ideas](https://github.com/Divide-By-0/ideas-for-projects-people-would-use#crypto-400-each)

### Circom circuits for higher degree gates 
- Develop a library for operations of with more than two operands.
- Credit : [aayushg.com](https://aayushg.com/)
- Update : [circom-circuits](https://github.com/nullity00/circom-circuits)

### Polygon ZKEVM as rollup on Optimism Bedrock 
- Tweak the polygon ZKEVM in Go with L1 as Optimism Bedrock & deploy the rollup contracts on Optimism to sync it
- Credit : Kevin Flitcher's OP Stack Presentations

### ZK Bridge for L2 – L2 transfer using Proof of Burn 
- User burns tokens in Arbitrum & posts the proof of burn in Scroll for the bridge to mint tokens to the user & vice versa
- Credit : [BTC Mirror](https://bitcoinmirror.org/)
- Ref : [BLS PIL](https://devfolio.co/projects/bls-pil-865f)

### Confidential Token transfers with UTXO on SC level 
- Implement Private transactions using by creating ZK-Vaults & confidential token transfers using a UTXO model.
- state channel inside the pool itself, UTXO pool on smart contracts , exchange signed anonymous messages
- Credit : Justin Glibert's [talk](https://youtu.be/3AOhH0mTmYM?t=2786)

### ECDSA in circom using lookup arguments & custom gates 
- Implement ECDSA with fewer constraints & lesser gates than spartan-ecdsa & circom-ecdsa.
- Update : Personae Labs just implemented this with a lot lesser constraints !!

## Halo2 circuit ideas 

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
7. 





