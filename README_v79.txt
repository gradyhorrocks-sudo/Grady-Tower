Master Cellular Tower Registry Frontend v79

After Save Tower succeeds:
- automatically return to Lookup
- set Search Towers to the just-saved eNB/gNB ID
- temporarily switch verification filter to All towers so the newly saved record cannot be hidden
- refresh the Lookup results immediately
- scroll the first matching result into view
- briefly outline/highlight it

Existing v78 behavior is preserved.
Existing v77 compact signal experience descriptions are preserved.
Existing simple Yes/No missing-tower workflow is preserved.
Backend remains v67.
