Master Cellular Tower Registry - Editable Home Screen App

This is an installable Progressive Web App (PWA).

NEW:
- Add towers
- Edit towers
- Delete towers
- Duplicate protection by carrier + radio + eNB/gNB
- Local on-device persistence
- Import/export JSON backups
- Registry counts
- LTE eNB/sector math both ways
- 5G /4096 calculation with provisional ? labeling
- PLMN carrier lookup
- Roaming detection
- Signal rating fields
- STRATA unmapped handling

iPhone/iPad:
1. Host the unzipped folder on any HTTPS static host.
2. Open index.html in Safari.
3. Share > Add to Home Screen.
4. Tap Add.

IMPORTANT:
Browser storage can be cleared by the OS/user, so use the Backup tab to export your registry after making changes.

NEW SCREENSHOT SCANNER:
- Upload a cellular screenshot from Photos/Files
- OCR attempts to extract PLMN, Cell ID/NCI, PCI, TAC, band, bandwidth, RSRP, RSRQ and SNR/SINR
- LTE or 5G ID math is calculated from the extracted Cell ID/NCI
- Review/edit OCR results before sending them into Tower Lookup
- OCR requires internet access when its OCR engine is loaded from the CDN

SCAN-BASED IDENTIFICATION UPDATE:
- Scan & Identify now uses the values extracted from the screenshot itself.
- It automatically matches PLMN + derived eNB/gNB against the Master Registry.
- The connection summary appears directly in the Scan tab.
- Open in Lookup remains available only as a secondary manual review path.

SPATIAL OCR v8:
- Scanner now uses OCR word bounding boxes instead of plain text order.
- Labels on the left are paired with values horizontally across from them on the same row.
- Cell ID/NCI, TAC, PCI, band, bandwidth, RSRP, RSRQ and SNR/SINR are extracted from their own rows.
- The app refuses to identify a tower unless PLMN + Cell ID/NCI are present.

PLMN SPATIAL UPDATE v9:
- PLMN is explicitly read from the value directly across from the PLMN label.
- If a screen uses separate MCC and MNC rows, their across-row values are combined into the PLMN.
- Known-registry PLMN text remains a safe fallback.

DIAGNOSTIC LAYOUT v10:
- Optimized for the supplied diagnostic screenshot layout.
- Reads top summary rows including TAC and PLMN.
- Supports spaced PLMN values such as "310 260" and normalizes to "310260".
- Reads "Cell Id" exactly as displayed by the diagnostic UI.
- Reads far-right values for Band, Bandwidth, Cell Id, PCI, RSRP and SNR.
- Detects the 5G section header and applies /4096 provisional gNB/local-cell math.

CELL ID FIX v11:
- More tolerant recognition of "Cell Id" including OCR mistakes such as Cell 1d / Cell ld.
- Constrained fallback searches only immediately after the Cell Id label, never arbitrary numbers.
- 5G detection improved from the 5G section header and n25/n41/n71 bands.
- n41 forces the scanned radio type to 5G in Auto mode.

LINE BAND SCANNER v12:
- Diagnostic fields are grouped by horizontal line band.
- A label and its value are matched only when they occupy the same visual row.
- The value to the right of the label is extracted, even when it is far across the screen.
- Cell Id also has a same-OCR-line fallback.
- Designed around the supplied diagnostic screen with separator lines.

AUTOFILL FIX v13:
- Runs enhanced + original OCR passes and merges the best field values.
- Uses both spatial row extraction and same-line diagnostic parsing.
- Explicitly autofills all Scan result fields after OCR.
- Manual corrections instantly recalculate eNB/gNB/local cell and re-identify the registry match.

SIMPLIFIED AUTO SCAN v15:
- Removed Home Carrier selector from Scan.
- Removed Radio Type selector from Scan.
- Screenshot automatically determines PLMN and LTE/5G.
- Scan & Identify automatically fills/identifies from the picture.
- Lookup is now a simple Cell ID/NCI box.
- Quick Lookup automatically tests LTE /256 and current 5G /4096 registry matches.
- Existing Registry, Add/Edit, Backup, PIN lock, GitHub Pages and PWA support preserved.

FIXED PIN v16:
- App PIN is fixed to 159357.
- Each new browser/app session requires the PIN.
- Removed PIN creation/change workflow.
- Existing registry, Scan, quick Cell ID/NCI Lookup, Registry, Add/Edit, Backup,
  GitHub Pages, Safari Home Screen/PWA support remain preserved.
- Important: this is app-level protection, not server-side protection of public GitHub Pages files.

UNIVERSAL SEARCH + CARRIERS v17:
- Lookup searches Cell ID/NCI, LTE eNB, 5G gNB, carrier name, tower/site name, PLMN, and band.
- Searching by carrier returns all towers for that carrier.
- Optional LTE/5G and carrier filters.
- Numeric searches also perform LTE /256 and current 5G /4096 identifier math.
- Add/Edit now accepts any future carrier name instead of a fixed carrier dropdown.
- Entering a new carrier + PLMN adds that carrier mapping to the local registry.
- Existing Scan, Registry, Add/Edit, Backup, fixed PIN, GitHub Pages and PWA support preserved.

TOWER MAP v18:
- Added a Map tab using OpenStreetMap.
- Tower records can store latitude and longitude.
- Add/Edit supports manual coordinates, current-device location, or tapping the map.
- Saved tower locations appear as map pins with carrier/radio/ID details.
- Existing towers without coordinates remain valid and can be mapped later.
- Existing Scan, universal Lookup, future-carrier support, Registry, Add/Edit, Backup,
  fixed PIN 159357, GitHub Pages, and Safari Home Screen/PWA support preserved.

ID AUTOFILL v19:
- In Add/Edit, typing an existing eNB/gNB automatically finds the matching registry record.
- Autofills carrier, PLMN, LTE/5G, site name, status, bands, bandwidth, saved Cell ID/NCI,
  sector/local cell, PCI, TAC, coordinates, and notes.
- Automatically switches the form into Edit mode for the matched record.
- If more than one record shares the same numeric ID, current carrier/radio is preferred.
- Existing Scan, universal Lookup, Map, future-carrier support, Backup, fixed PIN 159357,
  GitHub Pages and Safari Home Screen/PWA support preserved.

UNKNOWN TOWER ADD FLOW v20:
- If Scan & Identify derives an eNB/gNB that is not in the registry, an Add This Tower button appears.
- Add/Edit opens with all scanned values prefilled: PLMN/carrier when known, radio, eNB/gNB,
  Cell ID/NCI, sector/local cell, band, bandwidth, PCI, TAC, and scan signal notes.
- Site name remains blank so the user confirms the real tower name instead of the app inventing one.
- Unknown numeric Lookup results also offer Add as LTE Tower / Add as 5G Tower.
- Existing Scan, universal Lookup, Registry, Map, ID autofill, future-carrier support,
  Backup, fixed PIN 159357, GitHub Pages and Safari Home Screen/PWA support preserved.

SATELLITE MAP v21:
- Map tab now has Street Map and Satellite basemap options.
- Satellite layer uses Esri World Imagery.
- Saved tower pins, map picking, current location, and coordinate editing remain available.
- Existing Scan, universal Lookup, Registry, Add/Edit, unknown-tower add flow, future-carrier support,
  Backup, fixed PIN 159357, GitHub Pages and Safari Home Screen/PWA support preserved.

LOCATION GLOBE v22:
- Registry records with saved latitude/longitude now display a globe symbol (🌐).
- Records without coordinates do not show the globe.
- Globe indicates that the tower has a saved map location.
- Existing satellite/street map, Scan, Lookup, Add/Edit, ID autofill, unknown-tower flow,
  Backup, PIN 159357, GitHub Pages and PWA support preserved.

QUICK MAP LOCATION UPDATE v23:
- Map tab now includes an Update Tower Location panel.
- Enter an eNB/gNB and paste decimal coordinates to update that tower's saved location.
- Example accepted format: 40.455500, -109.528700.
- The registry globe indicator and map pin update immediately.
- If the numeric ID matches multiple records, the app refuses to silently update all of them.
- Existing satellite/street map, Scan, Lookup, Registry, Add/Edit, ID autofill,
  unknown-tower flow, Backup, PIN 159357, GitHub Pages and PWA support preserved.

DRAGGABLE MAP EDIT v24:
- Map tab includes Place / Drag Tower.
- Enter an eNB/gNB and select the matching tower.
- If the tower has a saved location, its marker becomes draggable.
- Dragging the marker saves the new coordinates immediately.
- While a tower is selected for map editing, tapping anywhere on the map moves that tower there and saves immediately.
- Towers without a saved location can be placed by selecting them and tapping the map.
- Stop Editing exits the map-edit mode.
- Existing coordinate-paste updater, satellite/street map, Registry globe indicator,
  Scan, Lookup, Add/Edit, Backup, fixed PIN 159357, GitHub Pages and PWA support preserved.

MAP LINK PARSER v25:
- Map > Update Tower Location accepts plain coordinates, Apple Maps links, and Google Maps links.
- Supports Apple Maps ll/sll/center/q coordinate formats.
- Supports Google Maps @lat,lon and !3dLAT!4dLON formats.
- Paste From Clipboard can pull the copied Maps link directly when Safari allows clipboard access.
- The extracted coordinates immediately update the chosen eNB/gNB location and map pin.
- Existing draggable/tap map editing, satellite/street layers, Registry globe, Scan, Lookup,
  Add/Edit, Backup, fixed PIN 159357, GitHub Pages and PWA support preserved.

SCANNED UNKNOWN MAP FLOW v26:
- If Scan & Identify finds an eNB/gNB not in the registry, the result now shows Place on Map.
- Place on Map opens the Map tab and waits for a map tap.
- After tapping the tower location, Add/Edit opens automatically with screenshot data plus latitude/longitude prefilled.
- Prefilled fields include PLMN/carrier when known, LTE/5G, eNB/gNB, Cell ID/NCI, sector/local cell,
  band, bandwidth, PCI, TAC, signal notes, and selected map coordinates.
- Tower/site name stays blank for user confirmation.
- Cancel Scanned Tower Placement is available while map placement is active.
- Existing map-link parsing, draggable map editing, satellite/street layers, Registry globe,
  universal Lookup, ID autofill, future-carrier support, Backup, PIN 159357,
  GitHub Pages and Safari Home Screen/PWA support preserved.

SCAN CLEAR + PHOTO PASTE v27:
- Scan page now has ✕ Clear Scan to reset the selected image, preview, OCR fields,
  identity result, signal fields, and unfinished scanned-tower map placement.
- Scan page now has Paste Photo for screenshots copied to the clipboard.
- When browser clipboard image access is supported, pasted photos feed into the same scanner.
- Safari may require clipboard permission; photo picker remains available as fallback.
- Existing unknown scan-to-map flow, map-link parsing, draggable map editing, satellite/street map,
  Registry globe, Lookup, Add/Edit, Backup, fixed PIN 159357, GitHub Pages and PWA preserved.

IPHONE SAFE AREA v28:
- App now detects iPhone/iOS-style browser and Home Screen environments.
- Uses Apple's CSS safe-area insets so text and controls stay clear of the Dynamic Island,
  camera/sensor cutout, rounded corners, and Home indicator.
- viewport-fit=cover enabled with safe padding on all four sides.
- Mobile layout becomes single-column where needed and keeps controls readable at iPhone width.
- Landscape mode also respects left/right cutout safe areas.
- Exact iPhone model is not guessed because Safari does not reliably expose model identity;
  layout adapts to the actual viewport/safe-area instead.
- All v27 Scan, Paste Photo, Clear Scan, map, registry, lookup, backup and PIN features preserved.

CUSTOM HOME SCREEN ICON v29:
- The actual Tower Registry PWA now uses the tower-on-a-mountain sunset artwork with a person holding a phone.
- Added Apple touch icon (180x180) for Safari Add to Home Screen.
- Added 192x192 and 512x512 PWA icons and updated the web manifest.
- This changes the real Tower Registry Home Screen icon, not a mockup of an iPhone Home Screen.
- If an older icon remains on iPhone, remove the existing Home Screen shortcut and add the site to Home Screen again after deploying v29.

FIRST-TIME DEVICE PIN v30:
- PIN remains fixed at 159357.
- PIN is required only the first time the app is opened on each device/browser.
- After successful entry, that device is marked trusted in localStorage and opens automatically later.
- Clearing Safari/site data removes the trust and requires the PIN again.
- Backup includes a "Require PIN Again on This Device" control to manually revoke device trust.
- This remains an app-level lock; public GitHub Pages files are not server-side password protected.
- All v29 functionality and custom Home Screen icon are preserved.

AUTO UNKNOWN SCAN PAGE v31:
- When Scan & Identify successfully derives a PLMN + eNB/gNB that is not in the registry,
  the app automatically opens the full Add/Edit page.
- The page is titled "Add Unknown Scanned Tower" and includes an Unknown tower detected banner.
- Prefills carrier when known, PLMN, LTE/5G, eNB/gNB, Cell ID/NCI, sector/local cell,
  band, bandwidth, PCI, TAC, and signal notes.
- Tower/site name and coordinates remain for user confirmation.
- User can save directly or place the tower on the map before saving.
- Existing scan-to-map, paste photo, clear scan, map-link parsing, draggable map editing,
  satellite/street maps, universal Lookup, Registry globe, Backup, first-device PIN trust,
  custom Home Screen icon, GitHub Pages and PWA support preserved.

UNKNOWN SCAN SAVE v32:
- Add Unknown Scanned Tower page now has a prominent "Save Tower to Registry" button.
- Requires a confirmed tower/site name plus eNB/gNB ID and carrier/PLMN before saving.
- Uses the existing registry save path so duplicate protection and local persistence remain active.
- After a successful save, the tower is removed from the unresolved Unknown scan state.
- The old Unknown result card is cleared and the app opens Registry so the newly saved record is visible.
- All v31 and earlier functionality is preserved.

FIRST-TIME MAP LOCATION v33:
- Map section formerly called Update Tower Location is now Add Tower Location by eNB/gNB.
- Enter an existing registry eNB/gNB plus coordinates, Apple Maps link, or Google Maps link.
- Adds latitude/longitude only when that tower does not already have a saved location.
- If the tower already has coordinates, the app refuses to overwrite them and directs the user to Place / Drag Tower.
- Registry 🌐 indicator and map pin appear immediately after first-time placement.
- All v32 and earlier functionality is preserved.

AUTHORITATIVE MAP MOVES v34:
- Coordinates are authoritative for tower placement.
- Set / Move Tower Location by eNB/gNB replaces any previous coordinates with the newly supplied coordinates or Maps-link location.
- Selecting a tower under Place / Drag Tower makes its pin draggable.
- Dragging the pin immediately replaces the saved coordinates.
- Tapping a new map location while a tower is selected immediately replaces the saved coordinates.
- Towers with no prior location are placed the same way.
- Restored complete map runtime functions so map controls operate consistently.
- All earlier registry, scan, unknown-tower, PIN, icon, backup and GitHub Pages features are preserved.

CONFIRM MAP LOCATION v35:
- Coordinate entry, Maps-link placement, map tapping, and marker dragging now preview the proposed tower location instead of saving immediately.
- Added Save Location and Cancel controls.
- Save Location commits the new latitude/longitude to the registry.
- Cancel restores the previously saved tower location.
- This prevents accidental map moves from immediately changing the authoritative registry.
- All v34 and earlier functionality is preserved.

SAVE ALL PENDING CHANGES v36:
- Existing tower edits are staged as pending changes instead of being saved immediately.
- Map moves, coordinate changes, Maps-link moves, tower detail edits, and deletions require Save All Changes.
- Global Pending Changes bar shows the number of records with unsaved changes.
- Save All Changes commits all staged modifications together.
- Discard All throws away every staged change.
- New tower records are still saved normally when explicitly added.
- Registry shows a Pending change badge on records with staged edits.
- All v35 and earlier features are preserved.

LIVE CLIPBOARD PASTE v37:
- Scan button is now Paste Current Clipboard.
- Each tap reads the clipboard fresh at that exact moment.
- The current copied image is placed into the real Scan file input and scanned immediately.
- Older pasted images are never reused.
- If the clipboard currently contains text rather than an image, the app reports that instead.
- Clear Scan also clears any pasted-image fallback.
- Safari may require clipboard permission.
- All v36 and earlier functionality is preserved.

CLEAR CURRENT PICTURE v38:
- Fixed Clear Scan button implementation.
- Clear now revokes and removes the current screenshot blob URL, empties the image source,
  hides the preview and wrapper, clears the file input and pasted-image state.
- Also clears OCR/results/identity fields and unfinished scan-to-map state.
- Selecting or pasting the next screenshot restores the preview normally.
- All v37 and earlier functionality is preserved.

IOS SCAN CLEAR + PASTE v39:
- Clear Scan now recreates both the file input and screenshot preview image nodes.
  This avoids iOS Safari/PWA retaining the old selected file or decoded image.
- Direct Paste Current Clipboard still reads the image clipboard when Safari grants Clipboard API access.
- Added an iOS-native Paste Photo Here target. Tap it and choose Paste from the iOS menu;
  the paste event reads the copied image directly and loads it into Scan.
- Scanner always uses the current selected/pasted image.
- All v38 and earlier registry functionality is preserved.

UNKNOWN SCAN AUTO-ADD v40:
- When Scan & Identify derives a valid PLMN + eNB/gNB that is not in the registry, Add Unknown Scanned Tower opens automatically.
- Screenshot-derived carrier (when known), PLMN, LTE/5G, eNB/gNB, Cell ID/NCI, sector/local cell, band, bandwidth, PCI, TAC, and signal notes are prefilled.
- Tower/site name remains blank for user confirmation.
- Save Tower to Registry uses the actual DB.records/saveRecord path, then clears the unresolved Unknown scan state.
- Removed a misplaced old auto-route from Cancel Scanned Tower Placement.
- All v39 functionality is preserved.

LOOKUP SEARCH FIX v41:
- Restored the missing Search Registry JavaScript used by the Lookup tab.
- Search now finds direct LTE eNB IDs and direct 5G gNB IDs.
- Finds exact stored Cell ID/NCI values.
- LTE Cell IDs are also converted to eNB + sector using /256 and reverse checked.
- 5G NCIs are also converted using the current /4096 interpretation.
- Carrier, site, PLMN, band and other text searches continue to work.

CLEAR AFTER NEW SAVE v42:
- After a brand-new tower is successfully saved, Add/Edit clears all entered values and returns to a blank Add Tower form.
- Unknown scanned towers also clear the form after they are successfully saved.
- Existing tower edits remain staged under the Save All Changes workflow and are not prematurely cleared/saved.
- Carrier and PLMN no longer default after a new save, leaving the form ready for unrelated new data.
- All v41 and earlier functionality is preserved.

CARRIER BRAND COLORS v43:
- Carrier names/badges use recognizable brand colors throughout registry/lookup/scan displays.
- T-Mobile: magenta.
- AT&T: blue.
- Verizon: red.
- STRATA Networks: orange.
- Union Wireless: green.
- T-Mobile Starlink: black/light in dark mode.
- Unknown/future carriers remain neutral until a brand color is assigned.
- All v42 functionality is preserved.

UNVERIFIED SEARCH v44:
- Lookup adds a Verification filter: All, Unverified/Provisional/Unknown, Unnamed only, Verified only.
- Searching keywords such as unverified, unknown, provisional, unnamed, unmapped, or no name returns records needing confirmation.
- Registry search also understands unverified/unknown/provisional and unnamed/unmapped/no name.
- Unnamed includes blank names, UNKNOWN, UNMAPPED, names ending in ?, and similar unresolved labels.
- All v43 functionality is preserved.

SEARCH TOWERS UNVERIFIED v45:
- Verification filtering is now placed directly under Search on the Search Towers page.
- Added one-tap Show Unverified and Show Unnamed buttons.
- Options remain All towers, Unverified/Provisional/Unknown, Unnamed only, and Verified only.
- All v44 functionality is preserved.

SEARCH ANYTHING v46:
- Search Towers now indexes essentially every useful record field.
- Searchable fields include tower/site name, carrier, PLMN, LTE/5G, eNB/gNB, Cell ID/NCI,
  sector/local cell, PCI, TAC, bands, bandwidth, status, notes, coordinates, and record key.
- Natural aliases such as LTE, 4G, 5G, NR, eNB, gNB, ECI, NCI, unknown, unverified,
  provisional, unnamed, and unmapped are recognized.
- Multi-word searches require all terms to match somewhere in the same tower record,
  e.g. "T-Mobile n41", "STRATA 1070", or "AT&T B14".
- Existing numeric direct-ID and LTE /256 / 5G /4096 math remains available.
- All v45 functionality is preserved.

CARRIER MAP PIN COLORS v47:
- Tower map pins now use carrier brand colors.
- T-Mobile: magenta.
- AT&T: blue.
- Verizon: red.
- STRATA Networks: orange.
- Union Wireless: green.
- T-Mobile Starlink: dark.
- Unknown/future carriers use neutral gray until assigned a brand color.
- Draggable/edit-preview pins keep the tower's carrier color.
- All v46 functionality is preserved.

CELLMAPPER ALL-CARRIER TEST v48:
- Experimental CellMapper Tower Search panel under Search Towers.
- Supports known carriers: STRATA, T-Mobile, AT&T, Verizon, Union Wireless, T-Mobile Starlink.
- Supports future/custom carriers by entering a PLMN manually.
- Network selector switches between 4G LTE and 5G NR.
- User enters eNB/gNB, then Open CellMapper launches the correct MCC/MNC and LTE/NR map.
- The preview tells the user to use CellMapper Search > Tower Search with the same eNB/gNB.
- This test does not silently scrape or overwrite registry data.

CELLMAPPER EVERY-SCAN TEST v49:
- During testing, every successful Scan automatically opens Search Towers and fills the CellMapper panel.
- Auto-filled fields: carrier from PLMN, PLMN, LTE vs 5G NR, and derived eNB/gNB.
- The panel tells whether the tower already exists in the local registry.
- User then opens CellMapper and uses Search > Tower Search with the prefilled eNB/gNB.
- Automatic Scan Behavior selector supports:
  1. Every Scanned Tower (testing)
  2. Unknown Towers Only (planned final mode)
  3. Off
- Unknown tower Add/Edit flow remains available, but CellMapper is shown first during testing.

BACKGROUND CELLMAPPER NETLIFY TEST v51:
- This build is for Netlify, not plain GitHub Pages.
- Every successful scan attempts a background lookup without leaving Tower Registry.
- Frontend sends PLMN, radio, derived eNB/gNB, and TAC to /.netlify/functions/cellmapper-lookup.
- The experimental backend tries an exact LTE base-station lookup when TAC/LAC is available.
- Returned tower coordinates/details are previewed and can be transferred to Add/Edit.
- 5G NR background lookup is intentionally reported unsupported in this first experiment instead of fabricating data.
- CellMapper can rate-limit or change undocumented API behavior, so this remains a test.

SEARCH RESULT ADD/EDIT (TEST):
- Search Towers result cards now include Add/Edit Info.
- Tapping it opens the exact registry record in Add/Edit with existing fields prefilled.
- User can add missing Cell ID/NCI, PCI, TAC, bands, bandwidth, notes, map location, name, or other details.
- Existing-record changes still follow the app's normal pending Save All Changes workflow where applicable.
