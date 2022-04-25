---
name: 'NMMNH Inventory Upload'
about: This issue lists the steps required to add completed inventories and create object tracking for the New Mexico Museum of Natural History and Science Paleontology Collection
title: "NMMNH Inventory"
labels: ''
assignees: ''

---

**Transcribe the inventory**
- [ ] Enter the data into excel if it isn't already typed (all catalog numbers in one column, all disposition in the next column).

**Check for Discrepencies**
Almost all specimens are stored in one location. We can use this fact to catch invetory mistakes and misplaced specimens.
- [ ] Check for Discrepencies within the current inventory.
   - Select the catalog numbers in the excel sheet and use conditional formatting > highlight cell rules > duplicate values.
- [ ] Check for discrepancies in the database.
   - Use [make comma list](https://arctos.database.museum/DataServices/listerizer.cfm) to [search](https://arctos.database.museum/nmmnh_paleo) for all specimens in the inventory.
- [ ] Compile all discrepancies into an excel sheet and print.
   - The catalog numbers should be in the first column, the next columns should have the potential storage locations of the specimens
- [ ] Physically check for the storage location of each specimen.
   - Can be done by a student/volunteer
   - Have them circle the correct storage location
   - Have them report anything odd to you, such as a specimen in two locations
   - Pull old check out tags for specimens that are found in another location
- [ ] Correct the inventory/object tracking
   - Update either Arctos or the inventory sheet, depending on what was found in the previous step
   - Reconcile specimens in two locations by moving specimens to one drawer, recording separate part locations, or fixing mislabeled or double-cataloged specimens.

**Create Containers**
- [ ] Use [bulkload container tool](https://arctos.database.museum/tools/create_container.cfm?action=ld). Use the previous upload file as a template. Before filling in the barcodes, check to make sure the next barcode is open.

**Move Containers**
- [ ] Use [batch scan](https://arctos.database.museum/batchScan.cfm?action=loadCSV) to move the new containers into their parent containers. Use the create containers file to create the move containers file.

**Move Parts into Containers**
- [ ] Download the template from [bulkload parts into containers](https://arctos.database.museum/tools/BulkloadPartContainer.cfm?action=ld).
- [ ] Add part IDs and barcodes to the the template.
   - Open the inventory and create container spreadsheets.
   - For each drawer:
      - Copy the drawer barcode into the template spreadsheet.
      - Copy the catalog numbers in that drawer.
      - Create a [comma list](https://arctos.database.museum/DataServices/listerizer.cfm) of the catalog numbers.
      - Copy the catalog numbers into [find container](https://arctos.database.museum/findContainer.cfm) and check that nothing is already in a container.
      - Copy the catalog numbers into [search](https://arctos.database.museum/nmmnh_paleo). Check that the number of specimens is correct.
      - Download parts list
      - Copy the part IDs into the template spreadsheet.
      - Fill down the barcodes.
- [ ] After adding all drawers, bulkload the template to [bulkload parts into containers](https://arctos.database.museum/tools/BulkloadPartContainer.cfm?action=ld).

**Add to Project**
- [ ] Create a [comma list](https://arctos.database.museum/DataServices/listerizer.cfm) of all specimens and add them to the [Inventory Project](https://arctos.database.museum/project/10003513)

**Update remarks and disposition**
- [ ] Update disposition and specimen remarks for specimens missing or with old check out tags.
   - Green tag: enter "“old green check out tag” into SPECIMEN remark. Update disposition to "on loan"
   - Missing: Update disposition to "missing", add remark about inventory.
