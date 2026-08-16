Master Cellular Tower Registry Frontend v80

NEW: automatic band enrichment for EXISTING towers.

When a scan matches an already-saved tower:
- preferred match is carrier + LTE/5G + eNB/gNB
- if carrier metadata is missing, a unique radio + eNB/gNB match may be used
- if the scan contains a valid band, that band is merged into the saved record
- existing bands are preserved
- duplicate bands are not added
- bands are normalized (LTE Bxx, 5G nxx) and kept in a clean list
- the band enrichment is saved immediately
- if the tower has a pending Add/Edit preview, the new band is merged there too
- Registry, Lookup, and Map refresh immediately
- a brief toast reports the band that was learned

IMPORTANT:
- This does NOT automatically create missing towers.
- The existing Yes/No prompt for a tower not in the Registry is preserved.
- Only the band is auto-enriched by this feature.
- v79 return-to-Lookup/show-just-added behavior is preserved.
- v77 compact signal experience descriptions are preserved.

Backend remains v67.
