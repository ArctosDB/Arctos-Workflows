![image](https://github.com/ArctosDB/Arctos-Workflows/assets/47402809/d2d89cdc-2714-4665-8267-8668b7d1d4e1)---
name: NMMNH Locality Bulkload
about: Steps required to bulkload new localities for the New Mexico Museum of Natural
  History and Science Paleontology Collection. Best used for a sequential group of
  localities with similar data.
title: NMMNH Paleo Bulkload Localities
labels: ''
assignees: ''

---

**Create upload file for public and encumbered localities**: go to [Bulkload Locality](https://arctos.database.museum/tools/bulkloadLocality.cfm)
   - [ ] Download template and save as an excel file
   - [ ] In column locality_name enter the locality numbers in the format "NMMNH:Paleo:L-#". Below that, enter the locality numbers in the format "NMMNH:Paleo:L-#_public"
   - [ ] Use [Search Geography](https://arctos.database.museum/place.cfm?sch=geog) to pull concatonated geography for the higher_geog column.
   - [ ] Fill in specific locality for the encumbered versions of the locality. For the public versions of the locality enter "Specific locality encumbered"
   - [ ] Fill in coordinates, maximum error distance (15 meters for GPS), and units for the encumbered localities.
   - [ ] Add accession number in remarks if applicable for the encumbered localities.
   - [ ] In georeference protocol fill in "not recorded"
   - [ ] For encumbered localities, in use_geography_polygon fill in "false". For public localities, in use_geography_polygon fill in "true"
   - Do not load yet.

**Create upload file for locality attributes**
   - [ ] Download [template](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm?action=ld) and save as an excel file
   - For Attributes shared by public and research localities each attribute will be entered twice, once under the research locality name and once under the public locality name
   - [ ] "site identifier" - localities may have multiple identifiers, enter as many as necessary.
      - NMMNH Locality Number
        - Value = NMMNH L-#
        - Determiner = New Mexico Museum of Natural History and Science
        - Date = date entered into locality ledger
      - Site Collector Number(s)
   - [ ] "site found" - If more than one person found the site, add an attribute for each person. 
      - Value = verbatim name and date
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
   - [ ] "georeference source":
      - encumbered localities - record original coordinate and methods used to convert or georeference
      - public localities - enter "geography spatial data"
   - For Attributes used only by encumbered localities each attribute will only be entered once under the research locality name.
   - [ ] "locality access"
     - attribute_value: fill in "private"
     - attribute_determiner: Collections Manager's name
     - determined_date: current date
   - [ ] USGS 7.5 or 15 minute topographic map
   - [ ] Landholder
     - If private, put name of private landholder in remarks.
   - [ ] "TRS township"
   - [ ] "TRS range"
   - [ ] "TRS section"
   - [ ] "TRS aliquot"
     - Value = verbatim aliquot
       
**Bulkload**
   - [ ] Go to [Bulkload Locality](https://arctos.database.museum/tools/bulkloadLocality.cfm) and load the localities.
   - [ ] Go to [Bulkload Localitye Attributes](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm?action=ld) and load the attributes.
