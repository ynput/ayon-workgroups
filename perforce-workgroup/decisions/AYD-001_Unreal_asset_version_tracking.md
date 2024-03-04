# AYD-001 Unreal asset version tracking

- **Status:** Proposed
- **Impact:**  Medium
- **Contributors:** Ondrej Samohel <ondrej@ynput.io>
- **Approved by:** -

## Background

We need to associate particular Perforce change list with all asset
versions loaded by AYON. Since containers defining loaded versions are
already part of the project as Unreal Assets, the information is
available inside the project itself, but that might not be sufficient
because to get that information you need to start Unreal Editor itself
and that can be time consuming.

## Options

### Option 1

Parse needed information from the Unreal project iself.

#### Pros
 
	- Up-to-date data directly connected to assets inside.
    - We already have this information in the project
  
#### Cons
 
	- Accessing the project can be done more or less only by executing UE on it and that can take a lot of time - direct access to the project files is also needed
	
### Option 2

Hook into Unreal Editor itself, track instantiation of assets
handled by AYON using Unreal Editor API. Whenever asset instance in map is created, link is registered.

#### Pros
 
	- Links are created on the fly
    - They are accessible outside the project and UE context
  
#### Cons
 
	- There might be limits of available Unreal API to make
    it unrealiable


### Option 3

Depend on publishing system to submit change lists. All links will be collected and created during the publishing stage.

#### Pros
 
	- Everything is collected and integrity of change list
    submission is validated just before change list is submitted.
    - Creating perforce change list is basically equivalent
    of publishing workfile in other DCCs so it somewhat matches existing logic.
  
#### Cons
    - Generated links won't reflect current project state
	- It might be very difficult to hook in Unreal perforce
    submission action to run AYON publishing instead.

## Outcome

TBD


## Action items

TBD	
