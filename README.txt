Master Cellular Tower Registry — OFFICIAL v65

Save All:
- Uses pendingTowerChanges, the same object that drives the Pending changes counter.
- Commits every staged change.
- After saving, clears pendingTowerChanges, hides the pending panel, clears stale forms/scan/CellMapper result, refreshes registry/map, and shows the green Everything Saved check.

CellMapper:
- Exactly three final statuses in the official UI:
  * Verified = green
  * Unverified = red
  * Not in CellMapper = no matching tower
- No CellMapper Unknown/white status.
- Green verified towers can autofill eNB/gNB and CellMapper coordinates.
- Red towers do not receive verified autofill.
- Not in CellMapper towers can still be added manually to the carrier list.

Backup:
- Compact Backup retained.
- PIN 159357 required every time Backup is opened.
