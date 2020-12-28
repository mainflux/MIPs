---
mip: <to be assigned>
title: <MIP title>
author: <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s), e.g. (use with the parentheses or triangular brackets): FirstName LastName (@GitHubUsername), FirstName LastName <foo@bar.com>, FirstName (@GitHubUsername) and GitHubUsername (@GitHubUsername)>
discussions-to: <URL>
status: Draft
type: <Standards Track, Meta, or Informational>
category (*only required for Standards Track): <Core, Networking, Interface, or ERC>
created: <date created on, in ISO 8601 (yyyy-mm-dd) format>
requires (*optional): <MIP number(s)>
replaces (*optional): <MIP number(s)>
---

## What is an MIP?
MIP stands for Mainflux Improvement Proposal. It is a concept borrowed from the several open-source projects: Erlang, Python, Ethereum and Rust to facilitate community involvement in developing Mainflux. This document is heavily based on [EEP 1](https://github.com/erlang/eep/blob/master/eeps/eep-0001.md) which in turn is based on [PEP 1](https://www.python.org/dev/peps/pep-0001/). An MIP is a design document providing information to the Mainflux community, or describing a new feature for Mainflux or its processes or environment. The MIP should provide a concise technical specification of the feature and a rationale for the feature.

We intend MIPs to be the primary mechanisms for proposing new features, for collecting community input on an issue, and for documenting the design decisions that have gone into Mainflux. The MIP author is responsible for building consensus within the community and documenting dissenting opinions.

Because the MIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

## MIP Work Flow
The MIP editors assign MIP numbers and change their status. Please send all MIP-related email to mips@mainflux.com.

The MIP process begins with a new idea for Mainflux. It is highly recommended that a single MIP contain a single key proposal or new idea. The more focused the MIP, the more successful it tends to be. The MIP editor reserves the right to reject MIP proposals if they appear too unfocused or too broad. If in doubt, split your MIP into several well-focused ones.

Each MIP must have a champion -- someone who writes the MIP using the style and format described below, shepherds the discussions in the appropriate forums, and attempts to build community consensus around the idea. The MIP champion (a.k.a. Author) should first attempt to ascertain whether the idea is MIP-able. Posting to the erlang-questions@erlang.org mailing list is recommended. Small enhancements or patches often don't need a MIP and can be injected into the Mainflux development work flow by sending a patch to erlang-patches@erlang.org.

The MIP champion writes a rough but fleshed out draft of the MIP, with a proposed title. This draft must be written in MIP style as described below. Then, a following process should be followed:

  - Fork the [MIPs repo]()
  - Copy `mip-template.md` to `mips/0000-my-feature.md` (where "my-feature" is
    descriptive). Don't assign a MIP number yet; This is going to be the PR
    number and we'll rename the file accordingly if the MIP is accepted.
  - Fill in the MIP. Put care into the details: MIPs that do not present
    convincing motivation, demonstrate lack of understanding of the design's
    impact, or are disingenuous about the drawbacks or alternatives tend to
    be poorly-received.
  - Submit a pull request. As a pull request the MIP will receive design
    feedback from the larger community, and the author should be prepared to
    revise it in response.
  - Now that your MIP has an open pull request, use the issue number of the PR
    to update your `0000-` prefix to that number.
  - Each pull request will be labeled with the most relevant sybsystem tag, which
    will lead to its being triaged by the maintainers team in a future meeting and assigned
    to a member of the maintainers team.
  - Build consensus and integrate feedback. MIPs that have broad support are
    much more likely to make progress than those that don't receive any
    comments. Feel free to reach out to the MIP assignee in particular to get
    help identifying stakeholders and obstacles.
  - The team will discuss the MIP pull request, as much as possible in the
    comment thread of the pull request itself. Offline discussion will be
    summarized on the pull request comment thread.
  - MIPs rarely go through this process unchanged, especially as alternatives
    and drawbacks are shown. You can make edits, big and small, to the MIP to
    clarify or change the design, but make changes as new commits to the pull
    request, and leave a comment on the pull request explaining your changes.
    Specifically, do not squash or rebase commits after they are visible on the
    pull request.
  - At some point, a member of the maintainers team will propose a "motion for final
    comment period" (FCP), along with a *disposition* for the MIP (merge, close,
    or postpone).
    - This step is taken when enough of the tradeoffs have been discussed that
    the maintainers team is in a position to make a decision. That does not require
    consensus amongst all participants in the MIP thread (which is usually
    impossible). However, the argument supporting the disposition on the MIP
    needs to have already been clearly articulated, and there should not be a
    strong consensus *against* that position outside of the subteam. Subteam
    members use their best judgment in taking this step, and the FCP itself
    ensures there is ample time and notification for stakeholders to push back
    if it is made prematurely.
    - For MIPs with lengthy discussion, the motion to FCP is usually preceded by
      a *summary comment* trying to lay out the current state of the discussion
      and major tradeoffs/points of disagreement.
    - Before actually entering FCP, *all* members of the subteam must sign off;
    this is often the point at which many maintainers team members first review the MIP
    in full depth.
  - The FCP lasts ten calendar days, so that it is open for at least 5 business
    days. This way all
    stakeholders have a chance to lodge any final objections before a decision
    is reached.
  - In most cases, the FCP period is quiet, and the MIP is either merged or
    closed. However, sometimes substantial new arguments or ideas are raised,
    the FCP is canceled, and the MIP goes back into development mode.

## What belongs in a successful MIP?
Each MIP should have the following parts:

1. Preamble -- RFC 822 style headers containing meta-data about the MIP, including the MIP number, a short descriptive title (limited to a maximum of 44 characters), the names, and optionally the contact info for each author, etc.

2. Abstract -- a short (~200 word) description of the technical issue being addressed.

3. Copyright/public domain -- Each MIP must either be explicitly labelled as placed in the public domain (see this MIP as an example) or licensed under the Open Publication License, or the Creative Commons Attribution 3.0 License.

4. Specification -- The technical specification should describe the syntax and semantics of any new language feature. The specification should be detailed enough to allow competing, interoperable implementations.

5. Motivation -- The motivation is critical for MIPs that want to change the Mainflux platform. It should clearly explain why the existing platform specification is inadequate to address the problem that the MIP solves. MIP submissions without sufficient motivation may be rejected outright.

6. Rationale -- The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages.

The rationale should provide evidence of consensus within the community and discuss important objections or concerns raised during discussion.

7. Backwards Compatibility -- All MIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The MIP must explain how the author proposes to deal with these incompatibilities. MIP submissions without a sufficient backwards compatibility treatise may be rejected outright.

8. Reference Implementation -- The reference implementation must be completed before any MIP is given status "Final", but it need not be completed before the MIP is accepted. It is better to finish the specification and rationale first and reach consensus on it before writing code.

The final implementation must include test code and documentation appropriate for Mainflux platform reference.

## MIP Format and Template
A MIP is written as an UTF-8-encoded text file in Markdown format. `mip-template.md` is a template and contains an instruction of how to write a MIP.

In the repository there is also a version of the Markdown Perl program and a some Perl scripts for building the EEP index. Just give the command ./build.pl in the toplevel directory.

## MIP Header Preamble
Each MIP must begin with an [RFC 822](https://tools.ietf.org/html/rfc2822) style header preamble all indented four spaces to make them [Markdown](https://daringfireball.net/projects/markdown/) code style. The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required:

```
Author: <list of authors' real names and optionally, email addrs>
* Discussions-To: <email address>
Status: <Draft | Active | Accepted | Deferred | Rejected |
            Final | Replaced>
Type: <Standards Track | Process>
* Content-Type: <text/plain | text/x-rst>
* Requires: <mip numbers>
Created: <date created on, in dd-mmm-yyyy format>
* Mainflux-Version: <version number>
Post-History: <dates of postings to erlang-questions>
* Replaces: <mip number, ...>
* Replaced-By: <mip number, ...>
```

Then follows a Markdown horizontal rule, the MIP number and title as a Markdown header 2, and a blank line, all required: ** MIP : ----

The Author header lists the names, and optionally the email addresses of all the authors/owners of the MIP. The format of the Author header value must be

```
Random J. User <address@dom.ain>
```
if the email address is included, and just

```
Random J. User
```
if the address is not given.

If there are multiple authors, each should be on a separate line following RFC 2822 continuation line conventions. Note that personal email addresses should be obscured as a defense against spam harvesters.

While a MIP is in private discussions (usually during the initial Draft phase), a Discussions-To header will indicate the mailing list or URL where the MIP is being discussed. No Discussions-To header is necessary if the MIP is being discussed privately with the author, or on the erlang mailing list. Remember to obscure email addresses here to.

The Type header specifies the type of MIP: Standards Track or Process.

The Created header records the date that the EEP was assigned a number, while Post-History is used to record the dates of when new versions of the EEP are posted to erlang-questions. Both headers should be in dd-mmm-yyyy format, e.g. 14-Aug-2009.

Standards Track EEPs must have a Erlang-Version header which indicates the version of Erlang that the feature will be released with. Process EEPs do not need a Erlang-Version header.

EEPs may have a Requires header, indicating the EEP numbers that this EEP depends on..

EEPs may also have a Replaced-By header indicating that a EEP has been rendered obsolete by later EEP(s); the value is the number(s) of the EEP(s) that replaces the current document. The newer EEP(s) must have a Replaces header containing the number(s) of the EEP(s) that it rendered obsolete.

## Auxiliary Files
MIPs may include auxiliary files such as diagrams, code listings, diffs, screenshots, shell scripts and so on. Such files must be named should be put under [assets](../assets) folder, in the specific folder named `mip-xxxx`, where "xxxx" is the MIP number. Filenames are arbitrary, but should be slef-documenting.

## Reporting MIP Bugs, or Submitting MIP Updates
How you report a bug, or submit a MIP update depends on several factors, such as the maturity of the MIP, the preferences of the MIP author, and the nature of your comments. For the early draft stages of the MIP, it's probably best to send your comments and changes directly to the MIP author. For more mature, or finished MIPs you may want to submit corrections to the eeps@erlang.org mailing list.

When in doubt about where to send your changes, please check first with the MIP author and/or MIP editor.

MIP authors can update MIPs by submitting new versions to the editors.

## Transferring MIP Ownership
It occasionally becomes necessary to transfer ownership of MIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred MIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the MIP process, or has fallen off the face of the 'net (i.e. is unreachable or not responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the MIP. We try to build consensus around a MIP, but if that's not possible, you can always submit a competing MIP.

If you are interested in assuming ownership of a MIP, send a message asking to take over, addressed to both the original author and the MIP editor eeps@erlang.org. If the original author doesn't respond to email in a timely manner, the MIP editor will make a unilateral decision (it's not like such decisions can't be reversed :).

## Copyright
This document has been placed in the public domain.