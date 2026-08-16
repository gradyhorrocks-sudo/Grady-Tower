Frontend v82

FIX:
- The compact Expected experience box is now rendered directly inside every Scan result,
  immediately below RSRP / RSRQ / SNR-SINR and before Math.
- It contains exactly three compact experience lines:
  Calls, Video, Data.
- The wording is generated from the actual available signal-quality statistics.

PRESERVED:
- Automatic band enrichment occurs only from an uploaded/pasted image OCR scan.
- Manual scan-field edits do not automatically add bands to Registry records.
- Missing towers are not automatically created; the Yes/No prompt remains.
- Existing v79/v80/v81 Registry behavior is preserved.
- Backend remains v67.
