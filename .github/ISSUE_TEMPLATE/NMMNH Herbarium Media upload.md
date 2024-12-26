---
name: NMMNHS Herbarium Media upload
about: Template for uploadeding Media and Media metadata to Arctos, specifically for Herbarium Specimens. Currently this is a draft.
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
- [ ] Rename folders wtih "_tacc" once transferred
- [ ] Highlight images and right click -- File Names -- Copy to Clipboard (Include Paths)
  - Paste into the excel sheet that was made under the column MEDIA_URI
- 
Example worksheet:
