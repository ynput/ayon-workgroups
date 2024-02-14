# AYD-RE-002 Generating intermediate files for reviewable representations

- **Status:** Proposed
- **Impact:**  Medium
- **Contributors:**:
  - YNPUT Team <team@ynput.io>,
  - Jakub Jezek <jakub@ynput.io>
  - Tony Dorfmeister  (Bepic) @tweak-wtf
  - Jiri Sindelar (Dazzle Pictures) @jrsndl
- **Approved by:** -

## Background

To streamline our editorial workflow, we need to automate the creation of video files (used for reviewable/reference representation) that align with our publishing timeline. Currently, this task is manually handled by artists. Automating it will enhance efficiency.


## Options

### Option 1

Suppose we were to mirror a similar process to Nuke's Bake stream video, this would mean leveraging Resolve to generate an intermediate video file seamlessly on-the-fly. This newly created intermediate file would then serve as the input for transcoding options such as OIIO and FFMPEG.

Notably, this process should also incorporate baked color grading aesthetics for a more streamlined look, as well as facilitate the display & view.

Additionally, the inclusion of the display and view space ensures that the transcoded video is not restricted and maintains the highest quality, from color to clarity. This arranged method allows us to harness the full potential of transcoding with Resolve, OIIO, and FFMPEG.

This process would mean following steps would need to be (done with current Resolve API and OTIO:
1. Creating rendering settings `Project.SetRenderSettings()` with predefined temporary file path
2. Adding job to render queue `Project.AddRenderJob()` and capture return job id
3. Starting rendering only for job with given id `Project.StartRendering([job_id], isInteractiveMode=False)`
4. Getting the file from path and using it as source for reviewable representation which will need to be trimmed by clips' lengths
5. Deleting the temporary file
6. using trimmed intermediate files as source for OIIO or FFMPEG transcoding


#### Pros

- reducing manual work
- baking color grading look into reference files
- rendering via GPU will be faster than CPU

#### Cons

- this could be slowing down the workflow
- more complex publish workflow, since the rendering will need to be done asynchronously

### Option 2

Convert OTIO timeline to video files the same way as audio layers are converted for audio products. For more information look into [extract_otio_audio_tracks.py](https://github.com/ynput/OpenPype/blob/develop/openpype/plugins/publish/extract_otio_audio_tracks.py)

#### Pros

- This could be better streamlined with current OTIO implementation and universally done for all editorial DCCs

#### Cons

- slowing down the publishing workflow
- not possible to include color grading look into reference files


## Outcome

Needs to be decided.

## Goals

  - [ ] Rendering via Resolve API with GPU support
  - [ ] On demand baking color grading look into reference files


## Action items

  To be added.

## References

  #### Code inspiration:
- [bryanrandell/DaVinci-Resolve-Timeline-Utility](https://github.com/bryanrandell/DaVinci-Resolve-Timeline-Utility)
- [bryanrandell/DaVinci-Resolve-Timeline-Utility > all_utils_davinci](https://github.com/bryanrandell/DaVinci-Resolve-Timeline-Utility/blob/b1991b409d93511cbe6287f9a686b3ed826d2ac2/Workflow%20Integration%20Plugins/python_utils/all_utils_davinci.py#L149)