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

##### Project Documentation
- The start of the project was quite difficult for me, where i felt i did not realy know who to build anything of this. But I decided to take it one step at a time to showcase all the different things on at a time. This because i did not know how to put everything together, so instead i chose to showcase everything seperatly.
- To do this i started first of building the User diagram where i showcase the create and log in button, the log in button take you only to the log in page. And the create button only takes you to the create an account page.
- I need to figure out how to make the log in button actually log the user in / create a user account.
- I need to figure out how the setup information that the user selects updates the app so that the user wont have the feeling of "i need to do this again" instead it should give the user a feeling of "ah its a plug an play app". 
- How to build a diagram that shows the information that the user has selected to show.
- How to customize the input information about the Users migrain.
- After watching Hans video about authentication i finally cracked the login section to the application. Although not by buttons in the viewmodel but by auto applied buttons on the turnkeyserver.

#### Things in progress to be learnet.
- Making buttons go to VM.
- Saving User data to be shown on diffrent sections.
- Make color theme be shown.

#### Tips from Lars
- a server / computer does not have a direction everything needs to be stored. It needs to be told to move from part to another part. Login SysSingleton -> some part loaded from settings but also a memory pointer.
- does not need a seperat user class. Use instead SysUser. Or link SysUser to User.
- Be aware that SysUser u have 1 seekers - they are just looking for any object for a certain class. Things connected to 1 user is not intersting to look at without context is not useful. Its pointless to have a report migrain without User. A user is looking it shows report, it does not need a seeker.
- The user needs to add.
-> User view -> button Create settings etc -> Bind the object to the user. report.migrain.create let report = report.migrain.create r.user = currentuser.
Classic mistake difference between general search class like user or other which is owned by a user, which should only be created by the user.
-> Replace SysUser with User. Make the User own report migrain. Create out of the context of the user. User action that calls a method. 
-> User object .> Method createreportmigrain () use that method in the action. it is also a class action. 
Dropdown menu -> viewmodel actions.
Globalaction - > get to the context (seeker)
Its not MigrainSettings. its MigrainLog. 
AppSettings is only 1. Several VM that shows different informatiun. AppSettings Vm rooted in User. that shows the info. Different VM for User. Aggregation to consunption.

##### Progress
- After following Lars advice i have redone the application to make it more understandable and follow the logic.
- I only have a SysUser class and a ReportMigrain class. This because the other were changed into a viewmodel that is now accessed via a global action.
- What's currently being done, creating the date / time selections. Creating menus for selecting different choices.
- A few bugs have been created that i have not sorted down from 70 bugs to 5 bugs.
- Most of the time was spent redisigning the application and making it work. 
- Still have a difficulty in making button display viewmodel it only goes to accessdenied screen.
- Color chosen button is somthing i have to scrap i think.

#### The process of building
What I have had trouble with is not the building blocks (classes, VM or names (somtimes i named things wrong like a class was named ReportMigrain when thats a method because its doing somthing rather then being somthing) But the big problem for me has been the OCL, what to write and how to write it. Its not that i dont understand what for instance onCreate does and when to use it but its how to use it im struggling with.)
After batteling through this i watched alot of the OCL videos on the wiki, and although its greate and ive learned alot from it its not easy to implement. A sort of cheat sheet for OCL would be great, although the time to make somthing like that would probably be too high. But maybe a scaled down cheat sheet where for instance. I want to create a new report when i press this button how do i implement that. Or, how do i take information from one VM to another and show it in a graph.
Another thing that is linked to OCL is the issue in making methods, i dont really know when and how yet to make method.
Another thing that me Lars helped me with alot was the "how to think", because i think that i still think of this as a JavaScript process when its very much not like a JavaScript process. And just talking have unlocked somthing in my mind about how to think. I felt that i understood in the beginning that the wording has to be precise and the wording has to be very direct. And Lars said somthing "Its like talking to a baby", and thats true you have to treat the computer as a baby and you cant make assumptions. Other editors like VScode eliminates that and you can make assumptions which i think has hindered me in this case.
Other then that im quite pleased at what i managed to achive, although its far from where i want to be due to me having a very high bar for myself. I feel that i get the basics, and that im ready to start learning how to build things more advanced with the help of maybe a cheat sheet, and maybe as Lars pointed out loading up more examples and see how things have been built.
Another idea that struck me while going through this process was how to teach this, and i think that actually studying other examples and maybe doing a report on what each thing does and track it would be somthing to help in the process of learning.
##### Still in process of being done.
- Make the graph show data from the users selection.
- Make the log in button / create button direct the user to proper page ie. Create button -> Startup information. Login button -> Home Page.
- Make the color theme chosen display on the page.
- Save the data from Migrain reports, lifetime log to showcase in a graph.
- make the settings actually drop indications that the user dont want to log, and make it as an on/off switch.
- Style the page.
