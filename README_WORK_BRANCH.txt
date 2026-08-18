Master Cellular Tower Registry - Work Branch

Derived from the current full v91 frontend.

Removed from this branch:
- CellMapper Lookup UI
- CellMapper background/verified autofill UI
- Backup tab
- Backup page UI
- Direct CellMapper/Backup entry points are disabled

Preserved:
- Lookup
- Scan and OCR
- Registry
- Map
- Add/Edit
- Current signal grading/experience behavior
- Existing registry data/assets

The full v91 frontend remains the authoritative full build.
Backend remains v67.

Added: Add/Edit now has a Back button that returns to the tab the user came from.

Added: Save Tower now locks after the first tap, shows ✓ Saving… then ✓ Saved, and prevents accidental double-save taps from triggering the duplicate warning.

Added: Scan page now has editable Tower/Site Name plus Save All. Save All writes scan edits to the matched registry record and shows ✓ Saved after success.

Added: Dedicated Signal Values box directly below Scan & Identify. RSRP/RSRQ/SNR automatically mirror each screenshot and can be manually corrected; all signal ratings and expected-experience text recalculate from those values.

Added: Manual Signal Values accepts single readings or ranges (including negative dashes/en-dashes) and has a standalone Submit Signal Values button. No screenshot is required; ranges are graded at both endpoints and overall experience uses the weaker endpoint conservatively.
