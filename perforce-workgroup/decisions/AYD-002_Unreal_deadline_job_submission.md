# AYD-002 Unreal Deadline Job Submission

- **Status:** Proposed
- **Impact:**  Medium
- **Contributors:** Ondrej Samohel <ondrej@ynput.io>
- **Approved by:** -

## Background

AYON needs to create render and publishing job on Deadline
using specified change list. Doing this from AYON has advantages like
ability to run validators before job is processed on farm taking
precious resources, etc. In case of perforce, validators would need to
do some integrity checks probably.

## Options

### Option 1

Create Deadline job based on render publishing instances created by AYON inside Unreal. Pass perforce change list to the job if perforce is available. 

#### Pros
 
	- Similar to current Deadline support in other DCC
    - Provides feedback to artist about any error and automates issue resolution using Repair action
    - Validates if everything is submitted to Perforce correctly before render job is created
  
#### Cons
 
	- Takes control of the job creation so it hard to customize.
    - Depends on the specific Deadline plugin needed for job processing on the farm
	
### Option 2

Use "vanilla" Deadline plugin for job submission and publish only renders. 

#### Pros
 
	- No additional code needed, less complexity.
  
#### Cons
 
	- No validation before submission
    - Any customization must be done outside AYON
    - No support for Perforce
    - Render publishing has less information available and might guess on infer some from the rendered data itself


## Outcome

TBD


## Action items

TBD	
