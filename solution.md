Minutes of Meet

Solution->
  
  1. Manager or TL can create meet
  2. Manager and employee login   -   passwords are hashed
  3. manager can create a team and add members to the team
  4. have documents, media and links in separate tab and categorise by date
  5. add remainder to employee via mail for action items
  6. view action item of previous meet as check list in   next meet
      -> completed
      -> carry forward
  7. share MoM to all attendees via mail
  8. template 
    -> meet start time auto record on click of start button
    -> address scrum master
    -> mark absentees
    -> call to order
    -> old business 
    -> previous action items
    -> new business
    -> reminder of next meet if it exist
    -> end when the form is submitted - automatically
  9. Actors 
    -> Manager 
    -> Employee


Database->

  1. user_details (employeeID INT PRIMARY KEY, userToken VARCHAR(255), employeePassword VARCHAR(255), emailID VARCHAR(255));
  2. team_details (teamName VARCHAR(255) PRIMARY KEY, managerName VARCHAR(255), managerID , memberCount INT);
  3. team_mapping (employeeID INT, teamName VARCHAR(255));
  4. action_items (task VARCHAR(255), assignedTo VARCHAR(255), teamName VARCHAR(255), currentStatus INT DEFAULT 0);
  5. meet_summary (teamName VARCHAR(255), startTime DATETIME, scrumMaster VARCHAR(255), absentees VARCHAR(255), callToOrder TEXT, nextMeet DATE, endTime DATETIME);

Screens->

  1. Login/register in same screen for both user
  2. Manager login page - aesthatic welcome page
    Nav bar->
      a. create team 
          in this menu , new team can be created, members can be added. Editing can be done
      b. create meet
          on click of this menu, manager will get model to choose team.
          after choosing team, minute template page will open.
      c. history of minutes
          on click of this option, they can see all previous MoM , which will have 4 option - content, links, documents
            documents and links contents on click will only display them.
      d. dispute/query raised
          check any query or dispute raised by team members
      e. action items
          find action items assigned to you.
      f. logout 
  3. Employee login page
      a. history of minutes
          on click of this option, they can see all previous MoM , which will have 4 option - content, links, documents
            documents and links contents on click will only display them.
      b. query or dispute
          raise a query or dispute to manager in private
      c. action items
          find action items assigned to you.
      d. logout

Future enhancements ->
  1. Send E-mails                   - [paid libraries]
  2. Add reminder to action items   - [paid libraries]

things to do -> (13/13)

employee - > 
  1. home                  - done
  2. minutes content       - done
  3. minutes links         - done
  4. raise query           - done
  5. action items          - done

manager - >
  1. home                  - done
  2. create team           - done
  3. meet entry            - done 
  4. edit action items     - done
  5. minutes content       - done
  6. minutes link          - done
  7. queries               - done
  8. action items          - done