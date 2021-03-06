---
title: Key concepts
description: Overview of some of the key concepts leveraged by CryptoGlacier to make
  sure your crypto keys are kept safe.
---

## Private Key

Your currency balances are effectively stored in crypto
blockchains -- global decentralized ledgers. You can imagine a locked box
with all of your funds sitting inside of it. This box is unlocked with
a piece of information known as "private key". (The boxes we'll be creating
require multiple private keys to unlock; see the section "Multisignature
Security" below.)

Unlike a password, a private key is not meant for you to remember.
It's a long string of gibberish. The private key is what you need to keep
secure. If anyone gets it, they can take your money. Unlike traditional
financial instruments, there is no recourse. There is no company that is
liable, because blockchains are decentralized systems not run by any person or
entity. And no law enforcement agency is likely to investigate your
case.

The protocol makes use of [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)
and [BIP32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki).
This will allow us to deterministically derive keys across blockchains from
a 24-word phrase. This 24-word phrase is more commonly known as a mnemonic phrase,
mnemonic recovery phrase or mnemonic seed. It's a list of words which stores all the
information needed to recover your private keys across protocols.

## Offline Key Storage ("Cold Storage")

You don't want to store your
private key on any computer that's connected to the Internet ("hot
storage"), because that exposes it to more hacking attempts. There are
viruses out there that search computers for private keys and steal them
(thereby stealing your money).

One way to protect against this is by
encrypting your private key, so even if a thief steals it, they can't read
it. This helps, but is not foolproof. For example, a thief might install
[keylogger malware](https://en.wikipedia.org/wiki/Keystroke_logging)
so that they steal your password too.

Online keys are
inherently exposed to hackers. You therefore need to make sure your private
key stays offline ("cold storage") at all times.

## Paper Key Storage

Because the mnemonic phrase is a relatively small piece of information, it can
be stored on paper as easily as it can be stored on a computer. And when it
comes to key storage, paper has various advantages compared to computers: It's
always offline (no chance of accidentally connecting it to the Internet!), it's
easy & cheap to make multiple copies for backups, and it's not susceptible to
mechanical failure.
