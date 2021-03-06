---
name: 'NMMNH Locality Bulkload'
about: Steps required to bulkload new localities for the New Mexico Museum of Natural History and Science Paleontology Collection. Best used for a sequential group of localities with similar data.
title: "NMMNH Paleo Bulkload Localities"
labels: ''
assignees: ''

---

**Bulkload the encumbered research localities**: from the main menu select [Enter Data > Batch Tools > Locality/Event/Geography > Bulkload Locality](https://arctos.database.museum/tools/bulkloadLocality.cfm)
   - [ ] Download template and save as an excel file
   - [ ] Use [Search > Geography](https://arctos.database.museum/place.cfm?sch=geog) to pull concatonated geography for the higher_geog column.
   - [ ] Use "NMMNH:Paleo:L-#" in the locality_name column
   - [ ] Fill in specific locality
   - [ ] Fill in coordinates
   - [ ] Fill in maximum error distance and units (15 meters for GPS)
   - [ ] Add accession number in remarks if applicable
   - [ ] In georeference source record original coordinate and methods used to convert or georeference
   - [ ] In georeference protocol fill in "not recorded"
   - [ ] In use_geography_polygon fill in "false"
   - [ ] Save as csv and load

**Bulkload the Locality Access Attribute**: from the main menu select [Enter Data > Batch Tools > Locality/Event/Geography > Bulkload Locality Attributes](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm). Have this file prepared and ready to go as soon as the localities finish uploading.
   - [ ] Download template and save as an excel file
   - [ ] Copy locality names into the locality names field
   - [ ] fill in "locality access" for attribute_type
   - [ ] fill in "private" for attribute_value
   - [ ] fill in the Collections Manager's name for attribute_determiner
   - [ ] fill in the current date for determined_date
   - [ ] Save as csv and load

**[Bulkload](https://arctos.database.museum/tools/bulkloadLocality.cfm?action=ld) the public research localities**
   - [ ] Open the research localities bulkoad excel file and save as a new file
   - [ ] Remove quadrangle from the higher geography string.
   - [ ] Replace locality name with "NMMNH:Paleo:L-#_public"
   - [ ] Replace specific locality with "Specific locality encumbered"
   - [ ] Delete coordinate data and remarks
   - [ ] Replace georeference source with "geography spatial data"
   - [ ] In use_geography_polygon fill in "true"
   - [ ] Save as csv and load

**Bulkload Locality Attributes**
   - [ ] Download [template](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm?action=ld) and save as an excel file
   - For Attributes shared by public and research localities each attribute will be entered twice, once under the research locality name and once under the public locality name
     - [ ] "site identifier" - localities may have multiple identifiers, enter as many as necessary.
        - NMMNH Locality Number
          - Value = NMMNH L-#
          - Determiner = New Mexico Museum of Natural History and Science
          - Date = date entered into locality ledger
        - Site Collector Number(s)
     - [ ] "site found" - enter one attribute for the person and one attribute for the date. If more than one person found the site, add an attribute for each person. 
        - Value = verbatim name of person who found the site
        - Value = verbatim site found date
        - Determiner = Arctos Agent name of person who found the site
        - Date = Date the site was found in the format YYYY-MM-DD 
     - [ ] Chronostratigraphy - The most precise known level of chronostratigraphy should be chosen. Chronostratigraphy is hierarchical, so only the most precise value is required. Attributes types are "Eon/Eonothem", "Era/Erathem", "System/Period", "Series/Epoch", "Stage/Age", and "Substage/Subage".
     - [ ] "informal chronostratigraphy" - Any chronostratigraphy not on the international chronostratigraphic chart should be entered here. 
     - [ ] Lithostratigraphy - An attribute should be created for all given stratigraphic layers. Attribute types are "lithostratigraphic group", "lithostratigraphic formation", and "lithostratigraphic member".
     - [ ] Biostratigraphy - An attribute should be created for all given biostratigraphy stratigraphic layers. Attribute types are "biochron" and "biostratigraphic zone"
     - [ ] "geology remarks" - Enter verbatim all geological observations that don't fit the above attributes. This includes descriptions of stratigraphy, lithology, etc.
     - [ ] "landholder" - pick the landowner/administrator from the [code table](https://arctos.database.museum/info/ctDocumentation.cfm?table=ctlandholder).
     - [ ] "biota remarks"
       - One entry should just have fossil types, fully spelled out, separated by semicolon (no space), in the order listed on the locality sheet.
       - The other entry should be any summary description of specimens provided. PUT IN QUOTES so biota remarks can be separated when they are concatonated in data download
   - For Attributes used only by research localities each attribute will only be entered once under the research locality name.
     - [ ] Landholder
       - If private, put name of private landholder in remarks.
     - [ ] "TRS township"
     - [ ] "TRS range"
     - [ ] "TRS section"
     - [ ] "TRS aliquot"
       - Value = verbatim aliquot
