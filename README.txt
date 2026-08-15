Master Cellular Tower Registry — OFFICIAL v63

Official production frontend.

Backup page:
- Restored from the last build that contained the real working Backup page.
- Compact layout.
- Export JSON, Import JSON, Reset Registry.
- CellMapper backend settings collapsed under one small expandable section.
- Every time the Backup tab is opened, PIN 159357 is required.
- Backup access is not remembered between openings.
- Existing first-time device trust for opening the overall app is otherwise unchanged.

CellMapper:
- Production background lookup retained.
- Automatic lookup defaults to towers not already in the Registry.
- Green CellMapper tower = verified.
- Verified green tower autofills eNB/gNB and CellMapper coordinates into Add/Edit.
- Red or unknown does not auto-fill.
- Testing/diagnostic labels and giant diagnostic presentation removed.
