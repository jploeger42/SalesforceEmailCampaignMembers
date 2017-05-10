# SalesforceEmailCampaignMembers  
Code to create an email template with all campaign members BCC'ed  
  
For Javascript button code:  
1. Go to Setup --> Customize --> Campaigns --> Buttons, Links, and Actions --> New Button or Link  
2. Change Display Type equal to Detail Page Button  
3. Set Behavior equal to Execute JavaScript  
4. Paste the code in 'OnClickJavascriptButtonCode' file into the code window  
5. Save, add to your page layout, and enjoy  

For Lightning:
1. Log into your sandbox
2. Go to Setup --> Developer Console
3. Hit File --> New --> Apex Class
4. Name it ltng_CampaignEmailAttendees
5. Paste in the code from the ApexClass file, make sure the api version in the dropdown is set to your current org's, and save
6. Hit File --> New --> Apex Class
7. Name it ltng_CampaignEmailAttendeesTest
8. Paste in the code from the ApexClassTest file, make sure the api version in the dropdown is set to your current org's, and save
9. Hit File --> New --> Lightning Component
10. Hit 'Bundle Version Settings' on the far right and make sure the api version is set to your production org's
11. Paste code from 'Component' file into Component code area in developer console and save
12. Hit Ctrl+Shift+2 in the developer console to open up the Controller code area and paste in the code from the 'Controller' file and save
13. Hit Ctrl+Shift+7 in the developer console to open up the Design code area and paste in the code from the 'Design' file and save
14. Close out of developer console
15. Go to outbound change sets and create a new change set
16. Select 'Apex Class' from the component type dropdown and then check the 'ltng_CampaignEmailAttendees' and 'ltng_CampaignEmailAttendeesTest' files to and hit 'Add To Change Set' to add them
17. Hit 'Add' again and select 'Lightning Component Bundle' from the component type dropdown and then select the 'Campaign_EmailAttendees' box and hit 'Add To Change Set'
18. Hit 'Upload' on the change set page, select the org to upload it to, and deploy
19. Go to your org you just uploaded the change set to and go to 'Inbound Change Sets'
20. Select the change set you just uploaded and hit 'Deploy'
21. Wait for the tests to run and then you should be able to add the 'Email Attendees' button to your Campaign page layout in lightning
