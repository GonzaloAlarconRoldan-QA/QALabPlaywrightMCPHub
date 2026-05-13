# Orbit Reel 3D Interaction Validation

Use Playwright browser automation.

Read:
- context/context.md
- context/instructions.md

Goal:
Validate Orbit Reel 3D experiences and interactive highlighted areas.

Scope:
- 3D building viewers (if exists)
- 3D island viewers (if exists)
- orbit navigation
- highlighted interactive areas
- unit detail interfaces
- media/content panels

Validation Requirements:

## 3D Model Loading
Verify that:
- the 3D model loads correctly
- textures render properly
- highlighted areas are visible (apply filters in navbar if not displayed)
- the scene initializes without visual corruption
- loading indicators disappear correctly

Inspect:
- console errors
- WebGL/rendering issues
- failed asset requests
- FPS/performance issues if visible

## Orbit / Swipe Interaction
Validate:
- swipe/drag rotation works smoothly
- mouse drag interaction works
- touch gestures work (if mobile supported)
- zoom in/out interactions work (if available)
- the model does not freeze during interaction

Inspect:
- jittering
- unexpected camera jumps
- locked rotation states
- interaction delays

## Highlighted Area Interaction
For every highlighted area:
- click/tap the area
- verify the correct unit information appears
- verify associated images load correctly
- verify all subcontent is displayed correctly
- validate text/content formatting
- validate navigation between unit details

Inspect:
- incorrect unit mapping
- missing images
- broken subcontent
- inconsistent UI states
- duplicated overlays
- transitions (if applicable)

## Detail Panel Validation
Validate:
- unit information visibility
- image gallery behavior
- content scrolling
- zoom in/out transitions (if applicable)
- close/back interactions

## Return Navigation
Validate:
- returning to the main 3D interface works correctly
- the 3D scene restores properly
- highlighted areas remain interactive after returning
- navigation state remains stable

## Stress Interaction Testing
Validate:
- rapid clicking between highlighted areas
- repeated open/close actions
- repeated orbit interactions
- navigation after long interaction sessions

Requirements:
- capture screenshots for failures
- capture screenshots for rendering issues
- inspect browser console errors
- inspect failed network requests
- save findings into findings/
- save screenshots into screenshots/
- save traces/videos if severe rendering issues occur

Output:
Generate a detailed markdown validation report including:
- validated interactions
- rendering issues
- failed validations
- screenshots
- console/network findings
- recommendations
- regression candidates

Use timestamped filenames.