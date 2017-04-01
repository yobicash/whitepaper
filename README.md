# Yobicash #
<br>
## A cryptocurrency for storing and sending encrypted data ##
<br>
Christian Nyumbayire
revised by Amelia Tomasicchio
March, 30, 2017
<br><br>
### Abstract ###
<br>
Yobicash is a cryptocurrency for storing, managing and sending encrypted
data. Data ownership and user’s privacy are secured thanks to
cryptography. Data replication and a memory hard proof-of-work ensure
data availability and consistency in the presence of untrustable nodes.
A new way to build blocks that makes it possible to register more than
ten thousand transactions per second.
<br><br><br>
## 1. Introduction ##
<br>
Yobicash is a cryptocurrency that let users store, transfer and delete
data in a verified and confidential way through a Bitcoin-like
blockchain.
<br>
Thanks to encryption, only data signers can read a document, ensuring
privacy of the owners.
<br>
Data can be co-owned and managed by groups of users with different
permission levels and rights. Some users may be just allowed to read,
others may have the right to write, delete and transfer contents, others
may have to win weighted elections with their peers in order to receive
permission to do any action.
<br>
To ensure its use value, Yobicash prioritize throughput and scalability,
processing 10 thousand transactions per second for megabyte per block.
<br><br>
### 1.1. Historical background ###
<br>
Everything started back in 1988, when Mark S. Miller and K. Eric Drexler
published three revolutionary papers appeared in “The Ecology of
Computation” \[1\]. They envisioned trustless computer networks that
were able to share data and computation in exchange of economical
returns. The security - which any common distributed system could not
achieve - would have been granted by decentralization and market
process. They called it the *agoric system*, from the ancient Greek for
market, *agorà.*
<br>
In 2008 Satoshi Nakamoto, the pseudonymous user or group, published the
paper of a cryptographically enforced digital currency called Bitcoin
\[2\]. From then on, this currency tokens are produced through a shared
computation effort called *mining* and transferred through a public
shared ledger of transactions: the *blockchain*.
<br>
Bitcoin was the first successful embodiment of an agoric system thanks
to its strength to provide a cryptographic and transparent environment.
<br>
Since its development Bitcoin has been the most successful
cryptocurrency, reaching a market capitalization of 12 billion dollars.
<br>
After Bitcoin, new cryptocurrencies have been created, each one with a
different market proposition.
<br>
This ecosystem of agoric systems based on the blockchain (from now on
we’ll call them "blockchains") is maturing and giving more and more
returns.
<br>
Hopes are that the blockchain will change the face of every market and
government function by reducing verification and network costs \[3\].
<br>
Although the high hopes, the blockchains we daily experience are still
too specific in use, centralized and cannot scale to reach global usage.
<br><br>
#### 1.2. Generality ####
<br>
Factom \[4\] and Ethereum \[5\] made attempts of generality and they
could exemplify the way the above issues have been addressed so far:
generalizing data or generalizing computation.
<br>
Factom incentivizes nodes to store files whose *checksum* – a
cryptographic proof of existence – is shared on a blockchain. To address
scalability issues, Factom does not compel nodes to host all the files,
which are declared in its blockchain. This means that data access and
ownership may not be ensured. Its blockchain guarantees only the
checksum existence, ownership and transfer.
<br>
To increase data availability, this kind of currencies try to
incentivize hosting. They gain a greater partition tolerance, but they
loose maintainability.
<br>
Although this drawback, the approach of generalizing data – blockchains
for data – letscomputation be done offline and verified through a
proof-of-process. In a proof-of-process system for code execution the
blockchain takes care only of recording code, inputs, mid-steps and
outputs, so to make everyone interested in verifying the whole
computation process.
<br>
On the other hand, Ethereum attempts to generalize computation, so it
has a blockchain for computation. The data stored on Ethereum are only
those that are needed in order to the define its computation – the
so-called " smart contracts" - so the Ethereum blockchain has a specific
semantics and it is limited in scope and size.
<br>
These contracts are written in a specific programming language,
Solidity, and each node in the network runs the contracts when they are
called and it checks nodes' results by comparing them with its owns. The
burden of computation is shared among all the nodes. Data that exceeds
the size and semantics of Ethereum have to be put offline, and
referenced by the system some way.
<br>
Many have attempted to use Ethereum as a generic programming
environment, building on it token systems and complex contracts. Because
of its limitations and the lack of safety of its programming language,
Ethereum is more famous for its hacks \[6\] and missed chances \[7, 8\].
<br><br>
### 1.3 The Yobicash Answer ###
<br>
Differently from Factom and similar systems, Yobicash is a blockchain
for data that allows users to put raw data directly on the blockchain,
ensuring partition tolerance in a simple way. Data is treated as value
and can be converted back to currency at any time, so it is not just a
cost for nodes, but also an economic value.
<br>
Yobicash currency corresponds to what we commonly define a byte, in
fact, it’s called a Yobicash byte. The multiples of a Yobicash byte are
called as the “data” equivalent: Yobicash kilobyte, megabyte, gigabyte
and so on.
<br>
Miners create Yobicash bytes, so then users can exchange them.
<br>
Users have the right to convert all or part of their Yobicash bytes into
actual data, whose size has to be equal to the value of the converted
bytes.
<br>
After the conversion, data gets automatically encrypted.
<br>
On the other hand, if a user wants to get its currency back, she/he can
just convert the data back to Yobicash bytes. Then the converted data
will be deleted from the blockchain, but some metadata remains, like the
data checksum, in order to recognize the data when it’s found in the
blockchain or outside it.
<br>
This way, if a user wants to store some data on the blockchain, he/she
needs to send the data to him/herself, by executing a transaction with
the equivalent amount of the data bytes in Yobicash.
<br>
The same thing happens if he/she wants to send a data to another user.
In this case, he/she will have to do the same but sending the Yobicash
transaction to the other user and not to him/herself.
<br>
Confidentiality is ensured through encryption while different
scalability measures - the market for fees and the incentive of every
node owner to invest in storage - make its usage sustainable over time.
<br>
Data can be co-owned by different signers having different voting
weights. Signers with no voting weight will have no voice in the matter
of data management, but will be able to see the decrypted data. Signers
with the majority of the vote weights will have a major weight on
management issues, if not the last word.
<br><br>
### 1.4 Decentralization ###
<br>
Decentralization assures resilience to the network and it is a guarantee
of fault tolerance in case of geographically localized malicious actors
interested in taking over the network or particular mistrusts among
actors of different regions.
<br>
Although cryptocurrencies should be decentralized by nature, the
increasing difficulty of a mining algorithm can favor geographically
localized nodes and disfavor others. This kind of concerns has been
moved against Bitcoin which ended to be prevalently mined in China. This
centralization has increased the mistrust of many actors on the system.
<br>
Many cryptocurrencies addressed this problem by using mining algorithms
which do not slightly favor anyone. Memory hard hashing algorithms are
the most famous class from this group of alternative mining algorithms.
Yobicash uses a modified version of randmemohash, by Damian Lerner
\[9\].
<br><br>
### 1.5 Scalability ###
<br>
Scalability is paramount for a blockchain in order to reach global
usage. Related to blockchains, it means the capacity of the network to
increase the number of transactions per second when needed. VISANet can
process 56,000 tps (transactions per second) \[10\], while Bitcoin a
theoretical maximum of 7 tps \[11\] and a real maximum of 3 tps.
<br>
This feature is very important even for some applications to be viable,
e.g. blockchain embedded financial markets and IOT applications.
<br>
Scalability was not a priority in the times of Satoshi, but he expressed
the need to increase the size of transactions and blocks in future times
\[12\]. Bitcoin, stacked to a limit of 1Mb for blocks and transactions,
so it confirms 3 tps on average.
<br>
In order to address scalability issues, Yobicash blocks have a size
limit, but it changes according to the usage.
<br>
Yobicash achieves 10 thousand transactions per megabyte of a block,
which means that for a 4 MB block it can confirm 40 thousand
transactions. The real limit on the real number of transactions per
second is given by the actual average time for the execution of a single
transaction.
<br>
This feature could open up to new applications in need of fast responses
times.
<br><br><br>
## 2. Use cases ##
<br>
Yobicash is a means for securing data hosting, ownership and transfer in
an unsafe channel – the cloud. Thanks to its generality and focus on
scalability, privacy and decentralization, Yobicash allows for many use
cases.
<br><br>
#### 2.1. Safe hosting ####
<br>
Yobicash allows users to host data and co-own it with different voting
weights. Some users may be allowed to be only readers, some may be
considered as the editors while others may be defined administrators
holding the majority of voting weights.
<br>
Data can be copied to other users by sending copies to them, while
deletion are just conversions back to value.
<br><br>
#### 2.2. Safe messaging ####
<br>
Messaging is just transferring data. Thanks to encryption, messaging is
confidential by default.
<br><br>
#### 2.3. Proof of existence ####
<br>
A proof of existence is an hosted checksum of a digital artifact or the
artifact itself. While putting the entire data on the blockchain may be
expensive, resorting it to its checksum may be a possible alternative
when the host of the raw data is trusted. The transaction timestamp
containing the proof may be considered as the timestamp of the digital
artifact itself.
<br><br>
#### 2.4. Proof of ownership ####
<br>
A proof of ownership or smart property is a signed proof of existence.
By signing the proof, signer(s) declare to own the underlined digital
artifact and, if present, its offline referee.
<br>
Trusted signers can co-sign the proof to reinforce the claim. The proof
transfer from an user or group of users to another one represents a
transfer of ownership.
<br><br>
#### 2.5. Proof of authorship ####
<br>
A proof of authorship is a signed proof of existence. Differently from
the proof of ownership, it is not transferable. This difference is
neither enforced nor enforceable by the Yobicash protocol, but making it
clear is a responsibility of the parties (e.g. by using particular
semantics).
<br>
Proofs of authorship can be used to enforce intellectual property of
digital products.
<br><br>
#### 2.6. Proof of process ####
<br>
A proof of process is a series of chained proofs of existence or
authorship, witnessing different phases of a continuous or discrete
process. The process may range from the execution of an offline task by
some human beings or robots to the execution of some code by some remote
servers to the market data of a financial ticket.
<br>
The signer(s) of a step of a process are considered witnesses, verifiers
or executors of that process.
<br>
A proof of process can be used for distributed crowd-sourcing,
crowd-funding and task management. Multi-party computations can store
their steps on the Yobicash blockchain using it as a safe channel.
<br><br>
#### 2.7. Smart oracles ####
<br>
Smart oracles are proofs of existence or authorship made by trusted
sources on raw data or checksums, dealing with particular events or
general facts.
<br>
Financial and IOT applications can read time series data from smart
oracles writing on the Yobicash blockchain.
<br><br>
#### 2.8. Smart contracts ####
<br>
Smart contracts are proof of processes where the process is the
execution of some code involving changes of rights, properties or
balances of the parties involved. They are the coded version of offline
contracts, run by servers online.
<br>
This contracts can reference as inputs data already present in the
blockchain, or even future steps of some proven process. That data could
it be registered by generally trusted parties like in smart oracles or
be trusted just by the parties involved.
<br>
The executed code can be in any language the parties agree on, from
JavaScript to Julia to Haskell. It is a responsibility of the parties
choosing the language that fits more their needs.
<br><br><br>
## 3. Design ##
<br>
Yobicash design is similar to the Bitcoin’s one, with some key
differences to ensure simplicity, easy and confidential data management
and scalability.
<br><br>
### 3.1 Overview ###
<br>
Yobicash is a Bitcoin-like peer-to-peer network. The network is composed
by nodes, clients and wallets sharing transactions and blocks.
<br>
Nodes store and broadcast transactions and blocks. The data stored is
used to build the blockchain, a verified chain of confirmed blocks. The
blockchain has a predefined first block, the genesis block. Every block
after the genesis one is selected according to a block selection
algorithm, prioritizing blocks with more transactions and more data.
<br>
Nodes can choose to consume CPU and memory in the mining process, in
return of a given amount of
<br>
Yobicash, the *coinbase*. This coinbase can be consumed only after an
epoch, or 100 confirmed blocks. The coinbase amount decreases over time
until the total amount of Yobicash produced reaches 2.1 \* 2^80^, 2.1
yobibytes.
<br>
The mining algorithm used is a hardened version of randmemohash \[9\], a
memory strict hashing algorithm. The consumed memory helps
decentralization allowing common devices to be competitive in the mining
process.
<br>
The algorithm has a varying difficulty to assure that the average block
confirmation time is 17 seconds.
<br>
Users transfer value and data between themselves through transactions.
They store transactions in personal wallets and send them to nodes in
order to validate and include them in the blockchain.
<br>
Data can be converted back and forth to the value (the size of the
data), which is denominated in bytes.
<br><br>
#### 3.2. Cryptography ####
<br>
Yobicash relies on 4 cryptographic primitives: cryptographic hashes,
public key signature, symmetric encryption and public key encryption.
The following is not a complete specification of Yobicash, but delines
its main features.
<br><br>
#### 3.2.1. Cryptographic hashes ####
<br>
Cryptographic hashes are functions that map binary data of any size to
equally sized collision-resistant (unique) short binary strings. Digests
- the outputs of these functions - are used by Yobicash as checksums and
IDs.
<br>
The cryptographic hashes used by Yobicash are SHA512 (also SHA3 or
Keccak) and randmemohash \[9\].
<br>
Yobicash uses SHA512 to identify transactions, blocks and data in a
certifiable way.
<br>
Digests obtained by hashing data are called *checksums*, while IDs are
digest resulted from hashing entire transactions or blocks.
<br>
Randmemohash is used by miners to build the proof-of-work. This
algorithm has the advantage of being memory hard, which means that it
requires less CPU, so that even a common machine can compete in the
mining process.
<br><br>
#### 3.2.2 Public Key Signatures ####
<br>
A public key signature is a scheme for cryptographically signature of a
binary data message. This scheme generates a couple of keys, the private
and public keys, used accordingly for signing and verifying a signature.
The private key (sk) must be kept in secret by its user, while the
public key (pk) is publicly used to reference to its user and verify his
signatures (sig).
<br>
The phases of a public key signature are: the keys generation (keygen)
through a security parameter 1^λ^, the actual signing process (sign) and
the signature verification (verify).
<br>
keygen(1^λ^) = (sk, pk)
<br>
sign(sk, msg) = sig
<br>
verify(msg, sig, pk) = 0/1
<br>
This scheme is used to sign and verify Yobicash wire messages and as a
base for transaction weighted multisignatures.
<br>
Weighted multisignatures allow more users to sign a single message, and
on Yobicash this is used to sign transactions.
<br>
According to this scheme, when the sum of the weights of the actual
signers is greater than a user-defined threshold, the signed message is
considered valid.
<br>
The scheme used by Yobicash is ed25519 \[13\], which is based on Schnorr
signatures and on curve25519. This scheme is more efficient and safer
than secp256k1 \[14\] used by Bitcoin and Ethereum, and produces smaller
signatures.
<br>
Yobicash uses this scheme to define the users and/or groups addresses
and to sign transactions and blocks.
<br><br>
#### 3.2.3. Symmetric Encryption ####
<br>
A symmetric encryption is a cryptographic scheme for encrypting binary
data. This scheme generates a secret key which is used to encrypt and
decrypt data.
<br>
This scheme has 3 phases: generation of a secret key sk (keygen) through
a security parameter 1^λ^, encryption (encrypt) of a plaintext message
msg and decryption (decrypt) of the resulting ciphertext ciph.
<br>
keygen(1^λ^) = sk
<br>
encrypt(msg, sk) = ciph
<br>
decrypt(ciph, sk) = msg
<br>
Yobicash uses XSalsa20 as symmetric encryption scheme. This scheme is
used to encrypt the data stored and sent by groups.
<br><br>
#### 3.2.4. Public Key Encryption ####
<br>
A public key encryption is a cryptographic scheme for encrypting binary
data. The schemes generates a pair of keys, a secret key and a public
key, used to encrypt and decrypt data. Data is encrypted through the
encryptor secret key and the decryptor public key; and it is decrypted
through the decryptor secret key and the encryptor public key.
<br>
In this way communication confidentiality is ensured. In some cases, a
public label may be used by both the parties to authenticate the data.
<br>
From a single user point of view, the scheme is composed by four phases:
key generation (keygen) through a security parameter 1^λ^, encryption
(encrypt) of the plaintext message msg and decryption (decrypt) of the
resulted ciphertext ciph.
<br>
keygen(1^λ^) = (sk, pk)
<br>
encrypt(msg, \[label,\] sk, pk’) = ciph
<br>
decrypt(ciph, \[label,\] sk’, pk) = msg
<br>
Yobicash uses curve25519XSalsaPoly1305 \[15\] as its public key
encryption scheme.
<br>
Users encrypt the symmetric encryption key used to encrypt data by using
this algorithm. Each user has different public key encryption keys for
each of their own wallets.
<br><br>
### 3.3 Transactions ###
<br>
A transaction is a data structure used to register the transfer of value
and encrypted data between groups of users.
<br>
Groups are sets of ed25519 public keys associated with a
curve25519XSalsaPoly1305 encrypted XSalsa20 private key common to all
group members and created by the transaction creator, a weight and a
threshold for the signing process. Only if the sum of the signing
members reaches the threshold the transaction is considered signed.
<br>
Money in Yobicash is denominated in bytes, so one byte in Yobicash money
is convertible to one byte of encrypted data.
<br>
A transaction has a fee, which is collected by miners. Fees are defined
per byte of a transaction. Miners add first the transactions with the
higher fees, increasing their revenues. When the costs of maintaining a
node are higher than their revenues, the fees value accepted by miners
increases. Competition to win the rush for the coinbase drives miners to
increase the number of transactions confirmed and the total amount of
data registered (see “blocks”).
<br>
In order to do that, miners have to decrease their storage costs and
increase their capacity, lowering the required fees. The result is that
the fee market incentivizes the increase of the available storage and
intend to keep fees low.
<br><br>
### 3.4 Blocks ###
<br>
Blocks are bundles of IDs of confirmed transactions plus a proof-of-work
and an associated coinbase.
<br>
The use of IDs - instead of full transactions - increases scalability,
ensuring that in 17 seconds (the time required for the confirmation of
two blocks) and with 1 Mb block size, Yobicash can confirm up to 10000
transactions per second. Nodes won’t accept blocks having transaction
IDs they can’t find in their store or by querying other nodes.
<br>
The proof-of-work system is built on the checksum of the serialized
signed block (a binary representation of the block) in order to make the
proof strictly linked to that block and to its signer. The coinbase is
the mined value, and it depends on the height of the block and the
amount planned to be produced at that height by a programmed money
supply function.
<br>
Every block defines the size limit of blocks and transactions. This
limit can grow by 10% if the sum of the previous block transactions is
over 90% of the size of the previous block itself.
<br>
Blocks are selected according to their *activity*, or the product of the
sum of their transactions and of the sum of their transactions size. The
result is that miners are incentivized to: 1) increase the number of
transactions, 2) increase the transaction sizes they register, 3)
decrease storage costs and fees.
<br>
This, together with the increase of the working memory in order to be
competitive in the mining process, has the effect of increasing
scalability.
<br><br><br>
## 4. Future work ##
<br>
Yobicash is designed to be simple and to be used as a platform for more
complex services. Security and scalability will remain the main areas of
improvement to guarantee its value proposition.
<br><br>
#### 4.1. More scalability ####
<br>
The current scalability measures may do a lot for some time, but
throughput is never too high. The more can be made to raise throughput
in order to maintain the trustless and Bitcoin-like structure, the
better the users will be served. A lot could be done just through
network simulations, fastening the development. Increasing scalability
and sustainability will open to new applications, improving benefits for
both users and the network.
<br><br>
#### 4.2. Quantum Cryptography ####
<br>
Quantum computers threaten all the value stored by current
cryptocurrencies. From public key signatures to currently used zero
knowledge proofs to public key encryption, everything used so far except
for Keccak hashes (sha3 hashes) will be easily broken \[16\].
<br>
Current research on post-quantum cryptography is still immature. A few
attempts to suggest already usable algorithms \[17\] have been made, but
a little bit of research will make it clear that many of the reported
algorithms are far from being safe.
<br>
Nonetheless — when needed — switching to post-quantum cryptographic
algorithms will be important. Supersingular isogeny elliptic curve
cryptography and lattice based cryptography seem the more promising
solutions so far.
<br><br><br>
## 5. Conclusions ##
<br>
Yobicash is currently the first attempt to make data a first class
citizen within blockchains and to embody the idea of the blockchain as a
general purpose technology. This is achieved by making data a value,
ensuring its confidentiality, letting users co-own it and taking care of
potential scalability issues.
<br>
This kind of blockchain – blockchain for data – enables a number of
applications that ranges from simple notaries to complex multi-party
computations.
<br>
More will have to be done in order to track and increase scalability and
to ensure new alternatives to the current cryptography when quantum
computers will be available. But right now the post-quantum cryptography
we quoted above is still immature.
<br><br><br>
## References ##
<br>
\[1\] M. S. Miller, K. E. Drexler, *The Ecology of Computation*, 1988
<br>
\[2\] S. Namamoto, *Bitcoin: A peer-to-peer electronic cash system*,
https://www.bitcoin.org/bitcoin.pdf, 2008
<br>
\[3\] C. Catalini, J. S. Gans, *Some Simple Economics of the
Blockchain*, 2016
<br>
\[4\] P. Snow, B. Deery, J. Lu, D. Johnston, P. Kirby, *Factom: Business
Processes Secured by Immutable Audit Trails on the Blockchain*, 2014
<br>
\[5\] https://github.com/ethereum/wiki/wiki/White-Paper
<br>
\[6\] N. Atzei, M. Bartoletti, and T. Cimoli, *A survey of attacks on
Ethereum smart contracts*, 2016
<br>
\[7\] http://blog.velocity.technology/velocity-is-shutting-downs
<br>
\[8\] G. Greenspan, *Why many smart contract use cases are simply
impossible*,
http://www.coindesk.com/three-smart-contract-misconceptions, 2016
<br>
\[9\] S. D. Lerner, *Strict Memory Hard Hashing Functions*,
http://www.hashcash.org/papers/memohash.pdf, 2014
<br>
\[10\]
https://usa.visa.com/dam/VCOM/download/corporate/media/visa-fact-sheet-Jun2015.pdf
<br>
\[11\] https://en.bitcoin.it/wiki/Scalability
<br>
\[12\] https://bitcointalk.org/index.php?topic=1347.msg15139\#msg15139
<br>
\[13\] D. J. Bernstein, N. Duif, T. Lange, P. Schwabe, B. Yang,
*High-speed high-security signatures*, 2011
<br>
\[14\] H. Mayer, *ECDSA Security in Bitcoin and Ethereum: a Research
Survey*, 2016
<br>
\[15\] D. J. Bernstein, *Cryptography in NaCl*, 2009
<br>
\[16\] M. S. Brown, *Classical cryptosystems in a quantum setting*, 2004
<br>
\[17\] PQCrypto, *Post-Quantum Cryptography for Long-Term Security*,
2016
<br>