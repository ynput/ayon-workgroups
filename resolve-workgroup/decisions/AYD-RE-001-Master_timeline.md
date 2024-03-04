# AYD-RE-001 Generating master timeline from multiple timeline variants

- **Status:** Proposed
- **Impact:**  Medium
- **Contributors:**:
  - YNPUT Team <team@ynput.io>
  - Jakub Jezek <jakub@ynput.io>
  - Tony Dorfmeister  (Bepic) @tweak-wtf
  - Jiri Sindelar (Dazzle Pictures) @jrsndl
- **Approved by:** -

## Background

NLE projects are usually producing multiple version of the same timeline. Either they need to produce different lengths or different resolution. Resources for these versions are usually shared. We need to be able to generate a master timeline from multiple timeline variants. This master timeline should contain shared clips in the longest durations. Clips in the master timeline are then ideal for publishing into the VFX pipeline.

## Options

### Option 1

Using OpenTimelineIO to generate master timeline from multiple timeline variants.

#### Pros

- Abstraction layer for multiple NLEs
- Resolve already has OTIO support in the latest version

#### Cons

- OTIO is not yet production ready in Resolve in regards of re-timing and speed changes

### Option 2

Using Resolve's native API to generate master timeline from multiple timeline variants.

#### Pros

- Faster processing

#### Cons

- Not using OTIO will resolve in more work in the future when we want to support other NLEs


## Outcome

Needs to be decided.

## Goals

  - [ ] OpenTimelineIO used as abstraction layer for multiple NLEs
  - [ ] Universally done for all editorial DCCs

## Action items

To be added.

## References

- [Resolve Merge timelines script](https://github.com/jrsndl/resolve-merge-timelines) - Resolve script for merging timelines. Customm script made by Jiri for merging timelines in Resolve. It is not production ready and it is not using OTIO.

- [OpenPype #5904](https://github.com/ynput/OpenPype/pull/5904) - Draft PR as solution proposal from Tony Dorfmeister. This PR had been creating one more layer for wrapping Resolve API with object-oriented abstraction, but since has already api wrapped within OTIO implementation this solution is decided to be only used as Proof of Concept. Idea was inherited from the Jiri's script. The Discussion on the PR is valuable source of feedback from community.

- [We Suck Less on time remaps ](https://www.steakunderwater.com/wesuckless/viewtopic.php?t=6292)
Tony's Post on We Suck Less forum about time remaps in Resolve. This post is a good source of information about the current state of OTIO in Resolve.
