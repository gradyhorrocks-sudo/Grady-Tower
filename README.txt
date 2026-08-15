Master Cellular Tower Registry — OFFICIAL v64

Changes:
- Unknown scanned towers now expose an Add to Carrier List button whenever the selected carrier + radio + eNB/gNB is not already in the registry.
- Existing carrier + radio + eNB/gNB records are treated as existing towers instead of new records.
- Save All Changes is now a one-shot commit.
- After Save All succeeds:
  * pending changes are cleared
  * pending-change bar is hidden
  * Add/Edit and Scan stale data are cleared
  * CellMapper background preview is cleared
  * registry is re-rendered
  * a green checkmark appears with "Everything Saved"
- Pressing Save All again with no changes reports that everything is already saved instead of re-saving stale data.
- v63 Backup behavior remains intact: compact Backup page and PIN 159357 required each time Backup is opened.
- Production CellMapper green=verified autofill behavior is preserved.
