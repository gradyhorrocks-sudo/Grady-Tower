Master Cellular Tower Registry Frontend v74

v73 filtering logic is preserved.

New fix:
Search Towers now refreshes immediately when registry state changes.

Why:
A tower could be changed to Confirmed and correctly become green, but the
already-rendered Search Towers results stayed on screen until the user manually
searched/refreshed again.

v74 automatically re-runs the active Search Towers filter after:
- Save Tower / Add/Edit
- staging an edit to an existing tower
- Save All Changes
- Discard All Changes
- deletion staging
- supported individual pending-change actions

Result:
If the Verification filter is "Unverified / Provisional / Unknown status" and
a tower becomes Confirmed, its card disappears from that list immediately.

Backend unchanged.
