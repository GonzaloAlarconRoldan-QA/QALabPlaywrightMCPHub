# Image Gallery Validation

Use Playwright browser automation.

Read:
- context/context.md
- context/instructions.md

Goal:
Validate that all image galleries across the application load and behave correctly.

Testing Scope:
- image galleries
- sliders
- carousels
- thumbnails
- fullscreen previews
- lazy-loaded images

Validation Requirements:

## Image Loading
Verify that:
- all images load successfully
- no broken images are displayed
- loading indicators behave properly
- thumbnail images is the same as image displayed
- lazy-loaded images appear when expected
- images maintain correct aspect ratio
- images are not stretched or cropped incorrectly

## Gallery Interaction
Validate:
- next/previous navigation
- swipe functionality (if supported)
- thumbnail navigation
- fullscreen mode
- close/open interactions
- keyboard navigation (if available)

## Visual Validation
Inspect:
- image alignment
- overlapping UI
- image flickering
- incorrect scaling

## Error Detection
Inspect:
- failed network image requests
- console errors
- missing CDN assets
- timeout/loading failures

## Edge Cases
Validate:
- galleries with many images
- galleries with a single image
- empty galleries
- slow-loading scenarios
- navigation after rapid interactions

Requirements:
- capture screenshots on failures
- capture screenshots on suspicious rendering
- monitor console/network errors
- save findings into findings/
- save screenshots into screenshots/

Output:
Generate a markdown validation report including:
- tested galleries
- passed validations
- failed validations
- screenshots
- recommendations

Use timestamped filenames.