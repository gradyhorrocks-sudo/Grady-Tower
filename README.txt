Master Cellular Tower Registry — OFFICIAL v66

CellMapper lookup now supports:
- 4G LTE / eNB
- 3G UMTS / NodeB
- 5G NR / gNB

Designed for backend v23 HUMAN UI WORKFLOW.

The frontend now trusts the explicit backend result:
- Verified / green
- Unverified / red
- Not in CellMapper

If browser automation finds the tower but cannot read the visible marker color,
the UI reports a lookup error instead of falsely turning it red or claiming the
tower is absent. That is an execution error, not a fourth tower status.

v65 Save All fixes and compact PIN-protected Backup behavior are preserved.
