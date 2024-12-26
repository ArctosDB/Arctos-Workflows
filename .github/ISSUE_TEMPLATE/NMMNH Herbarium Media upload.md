---
name: NMMNHS Herbarium Media upload
about: Template for uploadeding Media and Media metadata to Arctos, specifically for Herbarium Specimens. Currently this is a draft. Arctos Project Number 10004420
---

**Create Metadata sheet**
- Navigate N: Herbarium folder under Arctos
- [ ] Create folder with "Meta Data Herbarium yyyy-mm-dd" with todays date
- [ ] Create a new excel worksheet, Copy the headers from one of the previous uploaded files and paste into the new excel sheet
- [ ] Save the file as an excel worksheet with the same name as the folder

**WinSCP**
- Open WinSCP
- Select users profile and login
- Navigate to the Bioscience folder
- [ ] Create folder with todays date
- [ ] Move images under the folder "Arctos" from the local drive to the new TACC folder
- [ ] Rename folders with "_tacc" once transferred
- [ ] Highlight images and right click -- File Names -- Copy to Clipboard (Include Paths)
  - Paste into the excel sheet that was made under the column MEDIA_URI
     
**Excel Sheet**
- Follow the example worksheet below or one of the previous uploaded files to fill it out for upload
- [ ] Find: /corral/projects/arctos/web
- [ ] Replace: https://web.corral.tacc.utexas.edu/arctos
- [ ] Check the catalog number column for duplicates
- [ ] Once file is filled out, save as a CSV-8

**Arctos Upload**
- Go to [Bulkload Media](https://arctos.database.museum/loaders/BulkloadMedia.cfm)
- [ ] Upload CSV file
- [ ] Review users data and review to make sure it looks right
- [ ] Then select "Check All and set Status to Autoload"
- [ ] Then click "Change status for checked records"
- [ ] Then go to Component Loader Status and see if the priority needs to change.
- [ ] Once done, check a few records to make sure images loaded, it will take a bit for thumbnails to be made
- [ ] Update image folders in the Collections drive to have "_Arctos"

**SEINet**



Example worksheet: [Meta Data Herbarim Template.xlsx](https://github.com/user-attachments/files/18254802/Meta.Data.Herbarim.Template.xlsx)

