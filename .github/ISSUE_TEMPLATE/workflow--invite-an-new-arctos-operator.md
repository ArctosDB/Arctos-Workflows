---
name: 'Workflow: Invite an new Arctos Operator'
about: This issue lists the steps required to add a new Arctos Operator
title: "[Arctos Operator]"
labels: ''
assignees: ''

---

1. Does the person have an Arctos Agent?
    - [ ] YES - Move to step 2.
    - [ ] NO - Create an Agent for them

2. Does the person have an Arctos Login that conforms to the specifications [here](https://handbook.arctosdb.org/how_to/How-to-Create-your-Arctos-Team-Users-and-Operators.html#1-have-each-team-member-create-an-arctos-user-account)?
    - [ ] YES - Add their Arctos username to their Agent as name type = login.
    NO
    - [ ] Have them create one using the specifications [here](https://handbook.arctosdb.org/how_to/How-to-Create-your-Arctos-Team-Users-and-Operators.html#1-have-each-team-member-create-an-arctos-user-account)
    - [ ] Have them send you their Arctos username.
    - [ ] Add their Arctos username to their Agent as name type = login.

3. Invite the Arctos user to become an operator.
 - [ ] Go to https://arctos.database.museum/AdminUsers.cfm
 - [ ]  enter the Arctos username into the form
 - [ ]  select their username to administer their account
 - [ ]  Select "Invite as Operator"
 - [ ] an email will be sent to the new operator from Arctos with instructions for accepting the invitation, after the user has accepted the invitation, have them let you know they have completed this step

4. Assign permissions to the new Arctos operator
 - [ ] Go to https://arctos.database.museum/AdminUsers.cfm
 - [ ]  enter the Arctos username into the form
 - [ ]  select their username to administer their account
 - [ ] ensure the Database User Status is "Account open and active"
 - [ ] read the [documentation for user management](https://arctos.database.museum/Admin/user_roles.cfm)
 - [ ] select "enable user management"
 - [ ]  provide access to the appropriate collection(s)
 - [ ] ALL operators should be assigned the role coldfusion_user
 - [ ] assign other roles as needed - PLEASE ensure that any operator is aware of documentation for all shared data roles!
 - [ ] email the new operator to let them know they re ready to begin work in Arctos
