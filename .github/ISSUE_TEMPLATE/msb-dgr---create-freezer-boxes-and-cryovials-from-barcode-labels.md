---
name: MSB DGR - create freezer boxes and cryovials from barcode labels
about: The following workflow describes the MSB DGR process for designating barcode
  labels as a particular container type in Arctos.
title: MSB DGR - create freezer boxes and cryovials from barcode labels
labels: ''
assignees: ''

---

The following workflow describes the process for designating barcode labels as a particular container type in Arctos. In this case, the process specifically refers to converting barcode labels into freezer boxes or cryovials in MSB DGR, but the process is the same for any other container type.
Some preliminary info:

    Barcode labels are ordered pre-preprinted (we currently use https://barcode-labels.com/) as 1D or 2D labels with machine and human readable code with base 36. See separate entry for how this is done.
    -The alphanumeric code series is reserved in Arctos for MSB at Manage Data > Object Tracking > Barcode Series (https://arctos.database.museum/info/barcodeseries.cfm).
    -creating containers and positions now requires admin_container role. This is to prevent students from creating positions within cryovials and other undesirable actions which are extremely difficult to undo. This also requires museum admins to create containers in bulk in advance, following procedures below.

**Step 1:** **When the labels are received, the series must be created in Arctos as follows:**

Before beginning, decide how you will create your container series. You either must decide the container types in advance - e.g. by determining all will be cryovials, or all will be freezer boxes, based on the type of label - or you can upload the series as labels, e.g. "cryovial label" or "container label". If you do the latter, cryovial labels will automatically convert to cryovials when they are scanned into freezer boxes, which has the advantage of only showing containers as cryovials if they have actually been scanned into position. Other labels will remain labels until you later designate what type of container to assign them to, using Bulk Edit Container. However, at MSB, we have switched to creating cryovials as cryovials from the beginning, rather than as cryovial labels, because in order to add a part to a barcode during cataloging, that barcode must be a container, not a label, or Arctos will throw an error during cataloging. Since cataloging occurs separately from object tracking in different divisions, this blocks cataloging from moving forward if even a single barcode for that record has not yet been scanned in DGR. 

- [ ] Go to Manage Data> Object Tracking > Create Container (bulk) at https://arctos.database.museum/tools/create_container.cfm Click Load csv to go to https://arctos.database.museum/tools/create_container.cfm?action=ld to see the required fields for the csv upload, and to download a csv template. 
- [ ] Add data to the template as appropriate
- [ ] Go to [Manage Data> Object Tracking > Create Container (bulk)](https://arctos.database.museum/tools/create_container.cfm) Click Load csv. Browse to the file you created above and select Upload this file
- [ ] After the file has successfully loaded, select Review for this User/status
- [ ] If all looks good, click the blue box for "Check all and set status to autoload", and then click the tan box for "Change status for checked records"
- [ ] Give the tool some time to process the records, then go to [Manage Data> Object Tracking > Create Container (bulk)](https://arctos.database.museum/tools/create_container.cfm) and check the status of the records you loaded. Once the items have loaded, they will disappear from this view and should be visible in a search on the barcode at [Manage Data > Object Tracking > Find Container](https://arctos.database.museum/findContainer.cfm).

**Step 2: Using Bulk Edit Container to change container type and add labels to containers.**

This method is used for converting any container type into another container type, or to add label information, dimensions, or positions to an existing container.  At MSB, this tool is most frequently used to add label fields to barcoded containers (this is how we add labels to cryovials) and to convert container labels to freezer boxes, to convert cryovial labels to parasite vials or to envelopes to archive Nobuto blood strips or hair samples, etc. 

- [ ] [Go to Manage Data > Object Tracking > Bulk Edit Container](https://arctos.database.museum/tools/bulkEditContainer.cfm). Click Load csv to view data fields, download a template and upload csv file. Note that one of the required fields is the existing ("old") container type in order to change the container. You may not have this information for a large list of barcodes. If not, you can download a csv file with this information by going to [Reports/Services >Data Services > Get Container from Barcode](https://arctos.database.museum/DataServices/getContainerFromBarcode.cfm) by inputting a single column csv with header "input_barcode".
- [ ] Add data to the template as appropriate
- [ ] [Go to Manage Data > Object Tracking > Bulk Edit Container](https://arctos.database.museum/tools/bulkEditContainer.cfm). Click Load csv. Browse to the file you created above and select Upload this file.
-[ ] After the file has successfully loaded, select Review for this User/status
-[ ] If all looks good, click the blue box for "Check all and set status to autoload", and then click the tan box for "Change status for checked records
- [ ] Give the tool some time to process the records, then go to [Go to Manage Data > Object Tracking > Bulk Edit Container](https://arctos.database.museum/tools/bulkEditContainer.cfm) and check the status of the records you loaded. Once the items have loaded, they will disappear from this view and should be visible in a search on the barcode at [Manage Data > Object Tracking > Find Container](https://arctos.database.museum/findContainer.cfm).

For Freezer Boxes, freezer racks, or anything else with positions, there is another step to create positions.

**Step 3: Bulk Create Positions:**
Once the steps above are completed and the container has been created or edited to add container positions, do the following

-[ ] Go to [Manage Data > Object Tracking > Bulk Create Positions](https://arctos.database.museum/tools/bulkCreateContainerPositions.cfm). Click Load csv to see the required fields, download a template and upload csv file. **Note:** this form requires position dimensions. In the previous forms, you had to enter position orientation and number, eg. 10 x 10 horizontal for a freezer box.  In this form, you will need to enter values that are just slightly smaller than the total dimensions of the container when added together - not an easy task to figure out. Go to a similar container in Find Container and click on the positions to see what has previously been used. For freezer box positions, this is:  width = 1 cm, length = 1 cm, height = 4 cm.  Note that the order of W L H is not always the same in different forms  . . . don't get the order wrong.
- [ ] Add data to the template as appropriate
- [ ] [Go to [Manage Data > Object Tracking > Bulk Create Positions](https://arctos.database.museum/tools/bulkCreateContainerPositions.cfm). Click Load csv. Browse to the file you created above and select Upload this file.
-[ ] After the file has successfully loaded, select Review for this User/status
-[ ] If all looks good, click the blue box for "Check all and set status to autoload", and then click the tan box for "Change status for checked records
-[ ] Give the tool some time to process the records, then go to [Manage Data > Object Tracking > Bulk Create Positions](https://arctos.database.museum/tools/bulkCreateContainerPositions.cfm) and check the status of the records you loaded. Once the items have loaded, they will disappear from this view and should be visible in a search on the barcode at [Manage Data > Object Tracking > Find Container](https://arctos.database.museum/findContainer.cfm).

**Step 3B: Create positions one container at a time:**
- [ ] Go to [Manage Data > Object Tracking >Find Container](https://arctos.database.museum/findContainer.cfm) and enter the barcode of the container you wish to edit
-[ ] Click the box next to the barcode to bring up Container Details at right
-[ ] Click Positions
-[ ] If you see the error: 
insufficient data to proceed; a container must have

    NUMBER_ROWS
    NUMBER_COLUMNS
    ORIENTATION
    POSITIONS_HOLD_CONTAINER_TYPE

Then you must instead go back one screen, click instead on Edit Container at right, and add in the information on number of rows, columns, orientation, and positions. Don't forget to save. Then return to this form to create positions.
There is a default value of 1 cm length, 1 cm width, 4 cm height provided for cryovial positions in a freezer box. But for all other positions, you will have to enter the values needed. Go to Find Container for similar containers and look at the position dimensions currently in use.
