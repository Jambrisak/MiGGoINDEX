# MiGGoINDEX
### Project
So the start of the project was first reading through the documentation / looking through the pictures. 
### The breakdown
To make this application work I need to build theese things.
![The App](https://user-images.githubusercontent.com/1257288/204091050-3c91e6c2-e888-4573-bb76-a16efb2f1127.png)
#### SysUser / User
- There needs to be a system admin that can oversee everything, and then the user will in the beginning be faced with two choices create an account or log in.
- (Another way to do it is a log in button only that takes you to a create / log in section).
- If the user creates an account theese needs to be given and validated.
    
    1. Name
    2. Email
    3. Password
    
#### Home Page
- If the user has created an account next will be to set up the application.
![User](https://user-images.githubusercontent.com/1257288/204089850-d04d6b7f-5be0-4378-a6da-dcceba4d0bd6.png)
     
     1. In the home page the user will be given four choices (buttons)
     2. Report Migrain, will be a choice where the User can report an migrain attack.
     3. Weekly information, will be a choice where the user can see its weekly info on a graph.
     4. Migrain information, will be a choice where the user can setup what starts a migrain based on different choices.
     5. Settings, will be a choice where the user can setup the how the app looks and etc.
     
#### Report Migrain
![ReportMigrain](https://user-images.githubusercontent.com/1257288/204090085-7b0de5c8-b508-421a-9c26-9a9508cec8b0.png)
#### Weekly Information
![WeeklyInformation](https://user-images.githubusercontent.com/1257288/204090176-e90ee3f0-703e-40aa-87bf-7607030491e1.png)
#### Migrain Information
![MigrainInformation](https://user-images.githubusercontent.com/1257288/204090342-66ea08b4-ff57-485d-b9ea-407c83d87949.png)
#### Settings
![Settings](https://user-images.githubusercontent.com/1257288/204090489-a28c61f0-386f-4ccf-9153-6a552b015df5.png)
####
- This it my breakdown on what needs to be built done with flowcharts.

#### The Project
##### Log In
- Now when the user goes to the "app" the user has to login or create an account to see the Index page.
##### ToDo
- Make the buttons open the different autoforms.

##### Project Documentation
- The start of the project was quite difficult for me, where i felt i did not realy know who to build anything of this. But I decided to take it one step at a time to showcase all the different things on at a time. This because i did not know how to put everything together, so instead i chose to showcase everything seperatly.
- To do this i started first of building the User diagram where i showcase the create and log in button, the log in button take you only to the log in page. And the create button only takes you to the create an account page.
- I need to figure out how to make the log in button actually log the user in / create a user account.
- I need to figure out how the setup information that the user selects updates the app so that the user wont have the feeling of "i need to do this again" instead it should give the user a feeling of "ah its a plug an play app". 
- How to build a diagram that shows the information that the user has selected to show.
- How to customize the input information about the Users migrain.

- After watching Hans video about authentication i finally cracked the login section to the application. Although not by buttons in the viewmodel but by auto applied buttons on the turnkeyserver.
