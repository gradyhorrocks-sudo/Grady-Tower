Frontend v75

Simplified missing-tower behavior:
- A scanned tower that is not already in the Registry is NOT automatically added.
- The app shows one simple prompt: "This tower is not in your Registry. Add it?"
- Yes: opens Add/Edit and fills the scanned information for review. It is still NOT saved until Save Tower is tapped.
- No: does nothing.
- Removed the Automatic CellMapper Lookup selector from the scan workflow.
- Manual CellMapper lookup remains available in Lookup.
- v74 current-state verification filtering and live result refresh are preserved.

Backend unchanged: v67.
