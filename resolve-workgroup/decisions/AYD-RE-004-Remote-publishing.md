# AYD-RE-004 Remote publishing workflow

- **Status:** Proposed
- **Impact:**  Heigh
- **Contributors:**:
  - YNPUT Team <team@ynput.io>,
  - Jakub Jezek <jakub@ynput.io>
  - Tony Dorfmeister  (Bepic) @tweak-wtf
  - Jiri Sindelar (Dazzle Pictures) @jrsndl
- **Approved by:** -

## Background

At this moment we are using a single machine for publishing. This is not ideal for a few reasons. First, it is not scalable. Second, it is not reliable. Since the editorial publishing can be a time-consuming process, it is not ideal to have a single machine doing all the work and blocking the editorial team.

## Options

### Option 1

Publishing process would be divided into two stages. First stage would be done locally and this will contain mainly preparation of hierarchy and intermediate files (AYD-RE-002). Second stage would be done on the farm and this will contain the actual publishing of product versions with its representations. Farm publishing should use universal API which would be used for all DCCs (currently such API is not yet designed).

#### Pros

- faster publishing
- more reliable
- we can control better individual clip jobs on farm in case they crash

#### Cons

- will need to wait for the universal API to be designed

### Option 2

  There is not yet another option.

## Outcome

Needs to be decided.

## Goals

  - [ ] Blocked by AYD-RE-002
  - [ ] Separated publishing processes on local and remote.
  - [ ] Set up the workflow using any universal farm publishing API.

## Action items

  To be added.

## References

  To be added.