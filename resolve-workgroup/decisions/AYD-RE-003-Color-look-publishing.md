# AYD-RE-003 Colorspace and look publishing

- **Status:** Proposed
- **Impact:**  Medium
- **Contributors:**:
  - YNPUT Team <team@ynput.io>,
  - Jakub Jezek <jakub@ynput.io>
  - Tony Dorfmeister  (Bepic) @tweak-wtf
  - Jiri Sindelar (Dazzle Pictures) @jrsndl
- **Approved by:** -

## Background

Currently any grading work done in Resolve's Color Tab is not easily transferable into Nuke as a LUT. This is a problem because the color grading is an important part of the look of the final image. We need to find a way to transfer the color grading from Resolve to Nuke.

## Options

### Option 1

Creating a LUT File from **Primary Color Grading** Nodes. The new effect type would improve existing workflows. This method takes cues from Hiero's soft effects publishing. Users can add the LUTs to their Nuke scripts either as Viewer Process Nodes or in a linkable form.

#### Pros

- Grading can be shared with compositors for review without having to embed it directly into the images.

#### Cons

- Not yet available Resolve API for this

### Option 2

No other option yet.

## Outcome

What option (if) was chosen and why.


## Goals

  - [ ] Find a way to Generate Lut from Resolve Color Grading with any available APIs (Lua, Python)

## Action items

  To be added.

## References

  - [Black magic forum topic for missing API](https://forum.blackmagicdesign.com/viewtopic.php?uid=16&f=21&t=156596&start=0)
  - [Discord Davinci Resolve Plig-in Developers post](https://discord.com/channels/793508729785155594/793508730276282439/1207364324759306382)