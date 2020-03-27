
## PRE-REQUISITES:

- First you need to install angular CLI with the help of npm. And for that, you need to install Node.js

  a) Download using this link: https://nodejs.org/en/download/  (Download the LTS version)

  b) After downloading and installing, now open command prompt as Administrator
  
  c) On the CLI write, npm install -g @angular/cli ( if using MAC write sudo prior to this)
  
  d) Also you must have one IDE. I have used Visual Studio for this. You can download the same from       here:https://code.visualstudio.com/download

  e)Then type these commands:( don’t include $ )
  
        $ ng new final-project

        $ cd final-project

        $ code .

        $ ng serve
        

- You must have bootstrap version 3. Run these commands in command prompt
        
        $ npm install --save bootstrap@3
        

- Now you need to set up your back-end and database. For that, I have used FIREBASE.

  a) Go to  https://firebase.google.com/
  
  b) Click  “ go to console ”
  
  c) Click “add project”
  
  d) Give name to your project “ng-course-recipe-book” press continue and create your project.
  
  e) Then after that, click DataBase --->In realtime database, click create database ---> start in test mode ----> enable
  
  f) In rules, change default text to this text:
  
                {
                  "rules": {
                    ".read": "auth != null",
                    ".write": "auth != null"
                  }
                }
        
  g) Go to data and copy your  URL ; for eg : mine is **https://ng-course-recipe-book-55554.firebaseio.com/**
  
  h) In VS CODE, go to src→ app→ shared→ data-storage.service.ts, in there paste that above link in .put() and .get(), and add    recipes.json in the end 

    So the complete URL becomes:
    **https://ng-course-recipe-book-55554.firebaseio.com/recipes.json**
    **Copy your URL , NOT MINE.**

  i) Then go to authentication→ sign-in methods → email/password→ click on enable( only the upper one, don’t touch below one) → save

  j) Click on settings icon adjacent to Project Overview → **project settings→ copy your WEB API KEY (mine is AIzaSyC-eBn11t2PDvFo4CrGDSSm13fIeZ2nQ_U)
  
  k) Go to VS Code→ src→ environment→ Open environment.ts → **Replace your key** with mine written alongside firebase APIKey → Open environment.prod.ts→ **Replace your key** with mine written alongside firebase APIKey.
  
  l) Open this: https://firebase.google.com/docs/reference/rest/auth#section-create-email-password
And copy endpoint link.

  m) In VS Code, Open src→ app→ auth→  auth.service.ts  → replace my link with your endpoint link in signup {} function.  [**exclude [API_KEY] in the end**]

  n) Open this: https://firebase.google.com/docs/reference/rest/auth#section-sign-in-email-password
And copy endpoint link.

  o) In VS Code, Open src→ app→ auth→  auth.service.ts  → replace my link with your endpoint link in login {} function.[**exclude [API_KEY] in the end**].
  
  p) Save all the files.
  
  q) You can check the application running on “**localhost:4200**”
  
  
  
- Build your project by typing this in CLI :
    
    $ ng build --prod



- Install firebase-tools:
    
    $ npm install  -g  firebase-tools
    
    It will prompt you to log in. So through CLI, log in to your firebase account



- Open Command prompt (Administrator), write these commands → cd final-project → firebase init → with down arrow key go to  hosting , press space to select, then press enter→ choose the project ( ng-course-recipe-book) → (public) dist/ng-complete-guide-update → Yes ( for single-page app) →  No ( for overwrite) → Copy the hosting URL provided by your Firebase CLI → enter in browser to see your app running on a hosted server .

