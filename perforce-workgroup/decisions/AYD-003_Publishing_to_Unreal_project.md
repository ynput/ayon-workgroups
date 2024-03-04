# AYD-003 Publishing to Unreal project

- **Status:** Proposed
- **Impact:**  Medium
- **Contributors:** Ondrej Samohel <ondrej@ynput.io>
- **Approved by:** -

## Background

AYON can provide extractors to publish assets directly to Unreal project from other DCCs. This can speed up injest of asset into Unreal a lot. Publishing model from Maya can directly import the asset to Unreal and perhaps even submit new change list to Perforce.
With Hero versioning schema this can auto-update project just by publishing new data - that by itself can be rather dangerous within
running production, but there might be use cases. Without Hero version, it can load new version of the asset to the project with predefined settings making it available for artist use.

## Options

### Option 1

During the publishing, check if assets is checked out from Perforce to prevent conflicts. Run UE in headless mode to import FBX and create new version container. Submit to Perforce to make that version available.

#### Pros
 
	- New data is available in Unreal project as soon as they are published
    - With proper automation using hero versions it can speed up roundtrip for animatics, previews, etc.
    - Helps Unreal artist with repetitive task
    - Action to import to Unreal project can be bound to some approval status to save resources.
    
  
#### Cons
 
	- Unreal project must be available for validation and publishing even for artist not working in Unreal
    - This might be very time consuming process so offloading to farm is probably necessary
    - It can bloat Unreal project with unwanted versions
    - With Hero version it can be very dangerous if not configured
    properly.
	

## Outcome

TBD


## Action items

TBD	
