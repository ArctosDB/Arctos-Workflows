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
   - [ ] Add accession number in remarks if applicable
   - [ ] In georeference source record original coordinate and methods used to convert or georeference
   - [ ] In georeference protocol fill in "not recorded"
   - [ ] Save as csv and load

**Bulkload the Locality Access Attribute**: from the main menu select [Enter Data > Batch Tools > Locality/Event/Geography > Bulkload Locality Attributes](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm). Have this file prepared and ready to go as soon as the localities finish uploading.
   - [ ] Download template and save as an excel file
   - [ ] Copy locality names into the locality names field
   - [ ] fill in "locality access" for attribute_type
   - [ ] fill in "private" for attribute_value
   - [ ] fill in the Collections Manager's name for attribute_determiner
   - [ ] fill in the current date for determined_date
   - [ ] Save as csv and load

**Bulkload the public research localities**
   - [ ] Open the research localities bulkoad excel file and save as a new file
   - [ ] Use "NMMNH:Paleo:L-#_public" in the locality_name column
   - [ ] fill in "Specific locality encumbered" in specific locality
   - [ ] Delete coordinates
   - [ ] Go to [Find Localities](https://arctos.database.museum/place.cfm?sch=locality)
   - [ ] In Locality Name Search for State, County (no specific locality) to find a georeferenced, whole-county locality
   - [ ] Copy the coordinates, uncertainty radius, and georeference source from this locality into the bulkload file for public localities in this county.
   - [ ] Save as csv and load

**Bulkload Locality Attributes**
   - [ ] Download [template](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm?action=ld) and save as an excel file
   - For Attributes shared by public and research localities each attribute will be entered twice, once under the research locality name and once under the public locality name
     - [ ] Site Identifier(s) - localities may have multiple identifiers, enter as many as necessary.
        - NMMNH Locality Number
          - Value = NMMNH L-#
          - Determiner = New Mexico Museum of Natural History and Science
          - Date = date entered into locality ledger
        - Site Collector Number(s)
     - [ ] Site Found - enter one attribute for the person and one attribute for the date. If more than one person found the site, add an attribute for each person. 
        - Value = verbatim name of person who found the site
        - Value = verbatim site found date
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
       - The other entry should be any summary description of specimens provided.
   - For Attributes used only by research localities each attribute will only be entered once under the research locality name.
     - [ ] Landholder
       - If private, put name of private landholder in remarks.
     - [ ] TRS Township
     - [ ] TRS Range
     - [ ] TRS Section
     - [ ] TRS Aliquot
       - Value = verbatim aliquot
