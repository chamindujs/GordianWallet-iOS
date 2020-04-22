# FullyNoded 2

FullyNoded 2 is an open source iOS Bitcoin wallet that connects via Tor V3 authenticated service to the full node of your choice, including: a bitcoind installed using either Bitcoin Standup [MacOS](https://github.com/BlockchainCommons/Bitcoin-StandUp-MacOS) or [Linux Scripts](https://github.com/BlockchainCommons/Bitcoin-StandUp-Scripts); a full-node box such as [Nodl](https://www.nodl.it/) or [Rasbiblitz](https://github.com/rootzoll/raspiblitz); or a full-node service such as [BTCpay](https://btcpayserver.org/]). FullyNoded 2 is a self-sovereign wallet, and self-sovereignty means that you get to decide.

FullyNoded 2 allows for multiple wallet templates, including: legacy, SegWit-compatible, and SegWit-native hot wallets using a single signature (seed on iOS device); a warm wallet using multisig (seed on iOS device, keys on full node, offline seed, etc.); or a number of cold wallet templates that leverage PSBTs (Partially Signed Bitcoin Transactions), such as cold offline seeds, third-party collaborative custody services, and various air-gapped hardware solutions using QR codes. FullyNoded 2 can potentially support almost anything that can be described by a [bitcoind descriptor](https://github.com/bitcoin/bitcoin/blob/master/doc/descriptors.md).

<img src="./Images/home_screen_collapsed.PNG" alt="FullyNoded 2 app Home Screen" width="250"/> <img src="./Images/home_screen_expanded.PNG" alt="FullyNoded 2 app Home Screen" width="250"/>

## Status — Early Beta

*FullyNoded 2* is currently under active development and in early beta testing phase. It should be used on Bitcoin testnet to gain familiarity with how the wallet works, and most importantly to practice deleting and recovering wallet. For a detailed checklist to test critical functionality please see our [Checklist.md](./Docs/Checklist.md)

## Installing FullyNoded 2

FullyNoded 2 can be easily installed using Testflight, but if you prefer you can also install from source.

Please only use the app on testnet!

To help us improve FullyNoded 2, *please*  share crash reports and give us feedback. Want a feature added? Tell us about it.

### Requirements

- iOS 13
- A Bitcoin Core full node v0.19.0.1 (at minimum) which is running on Tor with `rpcport` exposed to a Tor V3 hidden service. Your node does not need to be an archive node, thus you can save space by being setup as a pruned full node.

### Installing FullyNoded 2 from Testflight

We have a public Testflight link available for beta testing [here](https://testflight.apple.com/join/OQHyL0a8). 

Click through, and you'll be able to install the app immediately (and will be instructed how to install Testflight if you need to do so first).

### Installing FullyNoded 2 from Source

Full instruction on installing from source are available [here](Docs/install-from-source.md).

### Linking to a Full Node

When you install FullyNoded 2, you will need to link it to the full node of your choice.

*FullyNoded 2*  has been tested with Blockchain Commons' [MacOS StandUp.app](https://github.com/BlockchainCommons/Bitcoin-StandUp-MacOS) and with our [Linux scripts](https://github.com/BlockchainCommons/Bitcoin-StandUp-Scripts), which install your own personal bitcoin-core and Tor services.

*FullyNoded2* should also work with any properly configured Bitcoin Core 0.19.0.1 node with a hidden service controlling `rpcport` via localhost, including full node devices such as [Nodl](https://www.nodl.it/) or [RaspiBlitz](https://github.com/rootzoll/raspiblitz), or full nodes installed by other services such as [BTCPayServer](https://btcpayserver.org). These full nodes can be connected by clicking a link or scanning a QR code. 

Please refer to their telegram groups for simple instructions on linking to these servers or services:

- [Nodl Telegram](https://t.me/nodl_support)
- [RaspiBlitz Telegram](https://t.me/raspiblitz)
- [BTCPayServer](https://t.me/btcpayserver)

## Using FullyNoded 2

Please see our [features](Docs/Features.md) document for full information on how to use FullyNoded 2 once it's installed.

## The Philosophy Behind FullyNoded 2

FullyNoded 2 is a professional mobile wallet built using the most up-to-date technologies for Bitcoin. It's focused on three goals that together demonstrate some of the best practices for modern mobile-wallet design:

1. **Self-sovereign Interactions.** Classic mobile wallets usually talked to a full node chosen by the wallet developer and owned/controlled by someone else. FullyNoded 2 instead allows you to choose a full node, either one created using a setup process such as #BitcoinStandup and run by yourself, or a service offered by a provider that you select: self-sovereign means you get to decide. (You can use Blockchain Commons' full-node server for beta testing, but you should migrate to a protected server for real money transactions.)

2. **Protected Communications.** All of the communications in FullyNoded 2 are protected by the latest version of Tor, which provides two-way authentication of both the server and your wallet. Unlike traditional use of the soon to be deprecated SPV protocol, which reveals that you're accessing the Bitcoin network, Tor simply shows that you're engaging in private onion communications. It's safer when you're in a hostile state, and it's safer in your local coffee shop.

3. **Multi-sig Protections.** Finally, FullyNoded 2 ensures that your private keys are protected from the most common adversary: loss. Its 2-of-3 multi-sig system leaves one key on the server, one on your mobile wallet, and one in safe off-line storage. If you lose your phone or your server, you can still rebuild from the other two. (The Blockchain Commons #SmartCustody system talks more about how to protect off-line keys.)

FullyNoded 2 is intended for a sophisticated power user. It's a leading-edge platform that experiments with modern Bitcoin technologies to create a powerful new architecture with features not found in other mobile wallets. It's intended as a professional wallet for your use and also as a demonstration of functionality that other companies can integrate into their own apps as an open source reference implementation of functionality.

Even more cutting-edge technology is planned for the future, including collaborative custody models, airgapped technologies such as Blockchain Commons' #LetheKit for offline signing using QR codes, and methodologies for social-key recovery.

## Financial Support

*FullyNoded 2* is a project by [Blockchain Commons](https://www.blockchaincommons.com/). We are proudly a social benefit "not-for-profit" committed to open source & open development. Our work is funded entirely by donations and collaborative partnerships with people like you. Every contribution will be spent on building open tools, technologies & techniques for blockchain and internet security infrastructure.
Please consider becoming a sponsor by supporting the project via GitHub's sponsorship program where they will match up to $5,000 USD in donations, more info [here](https://github.com/sponsors/BlockchainCommons). See our [Sponsors](./Docs/Sponsors.md) page for more info.

To financially support further development of `FullyNoded 2` and other projects, please consider becoming a Patron of Blockchain Commons through ongoing monthly patronage by becoming a [Sponsor](https://github.com/sponsors/BlockchainCommons) through GitHub; currently they are matching the first $5k so please do consider this option. You can also offer support with Bitcoin via our [BTCPay Server](https://btcpay.blockchaincommons.com/).

## Copyright & License

Unless otherwise noted (either in this [/README.md](./README.md) or in the file's header comments) the contents of this repository are Copyright © 2020 by Blockchain Commons, LLC, and are [licensed](./LICENSE) under the [spdx:BSD-2-Clause Plus Patent License](https://spdx.org/licenses/BSD-2-Clause-Patent.html).

In most cases, the authors, copyright, and license for each file reside in header comments in the source code. When it does not we have attempted to attribute it accurately in the table below.

This table below also establishes provenance (repository of origin, permalink, and commit id) for files included from repositories that are outside of this repository. Contributors to these files are listed in the commit history for each repository, first with changes found in the commit history of this repo, then in changes in the commit history of their repo of their origin.

| File                                        | From                                                         | Commit                                                       | Authors & Copyright (c) | License                              |
| ------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------- | ------------------------------------ |
| TBW                                         | TBW                                                          | TBW                                                          | TBW                     | TBW                                  |
| exception-to-the-rule.c or exception-folder | [https://github.com/community/repo-name/PERMALINK](https://github.com/community/repo-name/PERMALINK) | [https://github.com/community/repo-name/commit/COMMITHASH]() | 2020 Exception Author   | [MIT](https://spdx.org/licenses/MIT) |

### Dependencies

- [Tor.framework](https://github.com/iCepa/Tor.framework) by the [iCepa project](https://github.com/iCepa) - for communicating with your nodes hidden service
- [LibWally-Swift](https://github.com/blockchain/libwally-swift) built by [@Sjors](https://github.com/Sjors) - for BIP39 mnemonic creation and HD key derivation
- [Base32](https://github.com/norio-nomura/Base32/blob/master/Sources/Base32) built by [@norio-nomura](https://github.com/norio-nomura) - for Tor V3 authentication key encoding

## Contributing

We encourage public contributions through issues and pull-requests! Please review [CONTRIBUTING.md](./Docs/CONTRIBUTING.md) for details on our development process. All contributions to this repository require a GPG signed [Contributor License Agreement](./Docs/CLA.md).

### Credits

FullyNoded 2 is a professional mobile wallet that can be used by you for your cryptocurrency needs, but it's also an example that shows the latest in wallet technology and that can be used to inspire your own wallet designs, per the license above.

The team responsible for designing and developing this app are:

**Christopher Allen, Principal Architect.** Christopher has been working on open web architectures since the early ’90s, with a focus on security, privacy, cryptography, and standards. He is the founder of [Blockchain Commons](https://www.blockchaincommons.com/) and [Rebooting the Web of Trust](https://www.weboftrust.info/) and a member of the [W3 Credentials Community Group](https://w3c-ccg.github.io/). His recent focus is on engines of trust, specifically blockchains, digital assets, smart contracts, smart signatures, and decentralized self-sovereign identity.. 

**Peter Denton, Project Lead.** [need a few sentences here]

You can contact them at:

| Name              | Role                | Github                                            | Email                                 | GPG Fingerprint                                    |
| ----------------- | ------------------- | ------------------------------------------------- | ------------------------------------- | -------------------------------------------------- |
| Christopher Allen | Principal Architect | [@ChristopherA](https://github.com/@ChristopherA) | \<ChristopherA@LifeWithAlacrity.com\> | FDFE 14A5 4ECB 30FC 5D22  74EF F8D3 6C91 3574 05ED |
| Peter Denton      | Project Lead        | @Fonta1n3                                         | \<fontainedenton@googlemail.com\>     | 3B37 97FA 0AE8 4BE5 B440  6591 8564 01D7 121C 32FC |

You can add your name here by getting involved — the first step is to learn how to contribute from our [CONTRIBUTING.md](./Docs/CONTRIBUTING.md) documentation.

## Responsible Disclosure

We want to keep all our software safe for everyone. If you have discovered a security vulnerability, we appreciate your help in disclosing it to us in a responsible manner. We are unfortunately not able to offer bug bounties at this time.

We do ask that you offer us good faith and use best efforts not to leak information or harm any user, their data, or our developer community. Please give us a reasonable amount of time to fix the issue before you publish it. Do not defraud our users or us in the process of discovery. We promise not to bring legal action against researchers who point out a problem provided they do their best to follow the these guidelines.

### Reporting a Vulnerability

Please report suspected security vulnerabilities in private via email to ChristopherA@LifeWithAlacrity.com (do not use this email for support). Please do NOT create publicly viewable issues for suspected security vulnerabilities.

The following keys may be used to communicate sensitive information to developers:

| Name              | Fingerprint                                        |
| ----------------- | -------------------------------------------------- |
| Christopher Allen | FDFE 14A5 4ECB 30FC 5D22  74EF F8D3 6C91 3574 05ED |

You can import a key by running the following command with that individual’s fingerprint: `gpg --recv-keys "<fingerprint>"` Ensure that you put quotes around fingerprints that contain spaces.
