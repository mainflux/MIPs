# Mainflux Improvement Proposals (MIPs)

Mainflux Improvement Proposals (MIPs) describe standards for the Mainflux platform, including core protocol specifications, client APIs, and contract standards.

**Before you initiate a pull request**, please read the [MIP-1](mips/0001-process.md) process document. Ideas should be thoroughly discussed prior to opening a pull request, such as on the [Mainflux Gitter](https://Mainflux-magicians.org) or in a GitHub issue in this repository.

This repository tracks the ongoing status of MIPs. It contains:

- **Draft** proposals which intend to complete the MIP review process
- **Last Call** for proposals that may become final (also called FCP - Final Comment Period)
- **Accepted** proposals which are awaiting implementation or deployment
- **Final** and **Active** (similar to Final, but denotes an EIP which may be updated without changing its MIP number or never be completed) proposals that are recorded

Achieving "Final" status in this repository only represents that a proposal has been reviewed for technical accuracy. It is solely the responsibility of the reader to decide whether a proposal will be useful to them.

## Motivation

The Mainflux Improvement Proposals repository exists as a place to share concrete proposals with potential users of the proposal and the Mainflux community at large.

## Process

Mainflux MIP admission process is a mix of [Erlang](https://github.com/erlang/eep), [Ethereum](https://github.com/ethereum/EIPs) and [Rust](https://github.com/rust-lang/rfcs) processes.

In short, to get a major feature added to Mainflux, one must first get the MIP
merged into the MIPs repository as a markdown file. At that point the MIP is
"Accepted" and may be implemented with the goal of eventual inclusion into Mainflux.
Once implementation has been done, and PRs that implement the MIP are merged to Mainflux core,
MIP changes status to "Final" (or in some cases "Active", denoting a MIP wich can be updated even without changing it number).

[MIP-1](mips/0001-process.md) explains MIP creation process in details.

A short digest would be:
- Fork the MIPs repo https://github.com/mainflux/MIPs
- Copy [mip-template.md](mips/0001-process.md) to `mips/0000-my-feature.md` (where 'my-feature' is descriptive. don't assign an RFC number yet).
- Fill in the MIP
- Submit a pull request. The pull request is the time to get review of the design from the larger community.
- Build consensus and integrate feedback. MIPs that have broad support are much more likely to make progress than those that don't receive any comments.

## License

[Apache-2.0](LICENSE)