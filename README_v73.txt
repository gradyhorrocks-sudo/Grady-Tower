Master Cellular Tower Registry Frontend v73

ONLY the Search Towers verification/filter logic changed.

Fixes:
1. Verification no longer depends on tower name.
   - Confirmed status = verified, even if the name is still unknown or ends in "?"
   - Provisional/unknown/non-confirmed status = Unverified / Provisional / Unknown
   - "Unnamed only" remains a separate naming filter.

2. Search Towers now uses the EFFECTIVE current record.
   - Pending Add/Edit changes are reflected immediately.
   - A tower whose pending/current status becomes Confirmed disappears from the
     Unverified / Provisional / Unknown status view immediately.
   - Pending deletions are omitted.
   - Numeric eNB/gNB/Cell ID/NCI matching also uses effective records.

Backend is unchanged. Keep the current CellMapper backend deployment.
