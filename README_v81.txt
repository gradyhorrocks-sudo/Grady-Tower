Master Cellular Tower Registry Frontend v81

Band auto-save rule:
- Only an uploaded/pasted screenshot OCR scan may automatically add a newly observed band to an existing tower.
- Manual edits to Band or other scan fields do NOT auto-save bands.
- Missing towers are still NOT auto-created; the Yes/No prompt remains.

Compact scan summary restored:
- Calls
- Video
- Data
Generated automatically from the scan's current RSRP/RSRQ/SNR-SINR quality.

Preserved:
- v80 existing-tower band merge logic
- v79 return to Lookup and highlight just-added tower
- simple Yes/No missing-tower workflow

Backend remains v67.
