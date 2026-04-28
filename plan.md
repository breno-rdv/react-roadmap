# Implementation Plan

## Goal
Implement Create useEffect vs use example in breno-rdv/react-roadmap using the existing project structure discovered during research.

## Repository Context
- Repository: breno-rdv/react-roadmap
- Default branch: main
- Task: Create useEffect vs use example

## Relevant Areas to Inspect
- dir: 01-create-element-js
- dir: 02-create-element-react
- dir: 13-side-effects
- file: README.md
- file: start.sh
- dir: 03-small-app-js

## Implementation Steps
- Inspect breno-rdv/react-roadmap to confirm where examples matching this topic belong.
- Review the most relevant existing areas first:  
  - dir: 01-create-element-js  
  - dir: 02-create-element-react  
  - dir: 13-side-effects  
  - file: README.md  
  - file: start.sh  
  - dir: 03-small-app-js
- Implement the new example using the repository's existing naming, numbering, and teaching style.
- Add or update the companion explanation so the example includes both code and documentation.
- Update README or related documentation only if it is used to index or explain the example set.
- Confirm the existing startup flow still exposes the new example if routing or navigation is driven from the project shell.

## Risks
- The research snapshot only shows the repository root, so exact files still need confirmation before editing.
- The new example should match the style and sequencing of the existing teaching material.
- There may be project-level documentation or navigation wiring beyond the example folder itself.

## Research Notes
Research indicates each topic in this repository is typically represented by both a code example and accompanying documentation. README is present at the repository root and may need to stay aligned with the example set. A root start.sh script exists, so navigation or startup wiring may need confirmation after the example is added.

## Current Trigger
/plan