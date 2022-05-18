---
name: 'NMMNH Locality Bulkload'
about: This issue lists the steps required to bulkload new localities for the New Mexico Museum of Natural History and Science Paleontology Collection
title: "NMMNH Paleo Localitis"
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
   - [ ] Save as csv and load

Immediately **Bulkload the Locality Access Attribute**: from the main menu select [Enter Data > Batch Tools > Locality/Event/Geography > Bulkload Locality Attributes](https://arctos.database.museum/tools/bulkloadLocalityAttributes.cfm)
   - [ ] Download template and save as an excel file
   - [ ] Copy locality names into the locality names field
   - [ ] fill in "locality access" for attribute_type
   - [ ] fill in "private" for attribute_value
   - [ ] fill in the Collections Manager's name for attribute_determiner
   - [ ] fill in the current date for determined_date
   - [ ] Save as csv and load

**Bulkload the public research localities
