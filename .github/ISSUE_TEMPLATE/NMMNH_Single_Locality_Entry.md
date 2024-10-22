---
name: NMMNH Single Locality Entry
about: This issue lists the steps required to add a new locality for the New Mexico
  Museum of Natural History and Science Paleontology Collection
title: NMMNH Paleo Locality
labels: ''
assignees: ''

---

**Create the public locality**: from the main menu select [Manage Data > Location > Create Locality](https://arctos.database.museum/editLocality.cfm?action=newLocality).
 - [ ] Use pick geography to select the county-level geography.
 - [ ] In Specific Locality enter **Specific locality encumbered**.
 - [ ] Click Save.

**Edit the public locality**:
 - [ ] Locality Nickname - enter the NMMNH Paleo locality number entered in the format "NMMNH:Paleo:L-#_public" where # is the locality number.
 - [ ] Save

**Add locality attributes**:
 - [ ] Site Identifier(s) - localities may have multiple identifiers, enter as many as necessary.
     - NMMNH Locality Number
       - Value = NMMNH L-#
       - Determiner = New Mexico Museum of Natural History and Science
       - Date = date entered into locality ledger
     - Site Collector Number(s)
- [ ] Site Found
     - Value = verbatim name of person who found the site and verbatim site found date
     - Determiner = Arctos Agent name of person who found the site
     - Date = Date the site was found in the format YYYY-MM-DD 
- [ ] Chronostratigraphy - The most precise known level of chronostratigraphy should be chosen. Chronostratigraphy is hierarchical, so only the most precise value is required.
- [ ] Informal Chronostratigraphy - Any chronostratigraphy not on the international chronostratigraphic chart should be entered here. 
- [ ] Lithostratigraphy - An attribute should be created for all given stratigraphic layers.
- [ ] Biostratigraphy - An attribute should be created for all given biostratigraphy stratigraphic layers.
- [ ] Geology Remarks - Enter verbatim all geological observations that don't fit the above attributes. This includes descriptions of stratigraphy, lithology, etc.
- [ ] Landholder - pick the landowner/administrator from the dropdown list.
- [ ] Biota Remarks
    - One entry should just have fossil types, fully spelled out, separated by semicolon (no space), in the order listed on the locality sheet.
    - The other entry should be any summary description of specimens provided. PUT IN QUOTES so biota remarks can be separated when they are concatonated in data download
- Click "Save Locality Attributes"
    
**Create the research locality**
- [ ] Clone the public locality

**Edit the research locality**
- [ ] Add specific locality
- [ ] Change locality name to "NMMNH:Paleo:L-#"
- [ ] If applicable, enter accession number into locality remarks
- [ ] if lat/long or UTM coordinates are provided, replace the county-level coordinates of the public locality with those given.
- [ ] Add maximum error distance and units (15 meters for GPS)
- [ ] In georeference source record original coordinate and methods used to convert or georeference
- Click "Save Edits"

**Add locality attributes**
- [ ] Access
    - Value = private
    - Determiner = Collections Manager
    - Date = data entry date
- [ ] USGS 7.5 or 15 minute topographic map
- [ ] Landholder
    - If private, put name of private landholder in remarks.
- [ ] TRS Township
- [ ] TRS Range
- [ ] TRS Section
- [ ] TRS Aliquot
    - Value = verbatim aliquot
