Master Cellular Tower Registry Frontend v83

FIX:
The Calls / Video / Data description is now generated DIRECTLY inside
identifyFromScan and inserted directly into the scan card HTML.

It no longer relies on a helper function that could fail to render.

Visible placement:
Signal readings
Expected experience
  Calls
  Video
  Data
Math

Preserved:
- Automatic band saving only from uploaded/pasted image OCR scans.
- Manual changes to scan fields do not auto-save bands.
- Missing tower Yes/No behavior remains.
- Return-to-Lookup and just-added-tower highlighting remain.
- Backend remains v67.
