# Reusable Proof-of-Work

Reusable Proof-of-Work (RPOW) was an invention by Hal Finney intended as a prototype for a digital cash based on Nick Szabo's [theory of collectibles](http://nakamotoinstitute.org/shelling-out/). RPOW was a significant early step in the history of digital cash and was a precursor to Bitcoin. Although never intended to be more than a prototype, RPOW was a very sophisticated piece of software that would have been capable of serving a huge network, had it caught on.

### Historical Context

In the 1990s the Cypherpunks began to play around with the idea of a digital cash whose value would not be dependent on an organization issuing it. Following Nick Szabo, this form of digital cash would be recognizable as being limited in supply, and therefore usable as money, by being provably difficult to create. This could be done by defining units of the digital cash in terms of proof-of-work. Some proposals for digital collectibles circulated on the cypherpunk mailing list, including [b-money](http://nakamotoinstitute.org/b-money/) by Wei Dai and [Bit Gold](http://nakamotoinstitute.org/bit-gold/) by Nick Szabo. RPOW was the only digital collectible to ever function as a piece of software.

### How it Works

An RPOW client creates an RPOW token by providing a proof-of-work string of a given difficulty, signed by his private key. The server then registers that token as belonging to the signing key. The client can then give the token to another key by signing a transfer order to a public key. The server then duly registers the token as belonging to the corresponding private key.

The double spending problem is fundamental to all digital cash. RPOW solves this problem by keeping the ownership of tokens registered on a trusted server. However, RPOW was built with a sophisticated security model intended to make the server managing the registration of all RPOW tokens more trustworthy than an ordinary bank. Servers are intended to run on the IBM 4758 secure cryptographic coprocessor, which is able to securely verify the hash of the software that it is running. RPOW servers are capable of cooperating to serve more requests.

For more information, please see Hal Finney's [original page](http://nakamotoinstitute.org/finney/rpow/index.html), which includes an [overview](http://nakamotoinstitute.org/finney/rpow/what.html), an [FAQ](http://nakamotoinstitute.org/finney/rpow/faqs.html), a [theory page](http://nakamotoinstitute.org/finney/rpow/theory.html), a [presentation](http://nakamotoinstitute.org/finney/rpow/slides/slide001.html), and a very interesting page called [World of RPOW](http://nakamotoinstitute.org/finney/rpow/world.html) which explains how RPOW would have scaled to serve the entire planet.

### Github Repo Organization

This git repo contains two branches, one containing the original RPOW project exactly as Hal Finney wrote it, and another for ongoing development. On the development branch we will accept bug fixes and updates to keep RPOW working as intended on modern computers.

You can download original packages and binaries [here](https://github.com/NakamotoInstitute/RPOW/releases).

### Notice

Although we consider RPOW to be a great invention, the SNI does not recommend it as an investment and does not endorse anyone who runs an RPOW server and attempts to sell it as such.

*Special thanks to Fran and Jason Finney, Hal's wife and son, for sharing the original RPOW code and website files.*