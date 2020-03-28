NOTE: FIRST OF ALL, IN ORDER TO CONTINUE YOU MUST HAVE ALL THE PRE-REQUISITES SATISFIED.

SO BEFORE PROCEEDING WITH THESE STEPS PLEASE REFER TO ***PREREQUISITES.MD*** FILE 


# HOW-TO-RUN:

- Download the source code from the link provided to you.

- Extract the file contents. 
 
- Now go to this location in your system, where your project file is created: **C:\WINDOWS\system32\**  and then search for final-project.

- Open this folder and delete all the content inside this first. 

- After that copy all the content of "final-project" **(the one which you extracted)** to  "final-project" **(the one present at C:\WINDOWS\system32\ this location)**

- Now open command prompt as administrator and type these commands:

      $ cd first-app
      $ code . 

- This should open VS Code in your system along with the source code of my project.

-Now you need to set up your back-end and database. For that, I have used FIREBASE.

    a) Go to  https://firebase.google.com/
  
    b) Click  “ go to console ”
  
    c) Click “add project”
  
    d) Give name to your project “ng-recipe-book” press continue and create your project.
  
    e) Then after that, click DataBase --->In realtime database, click create database ---> start in test mode ----> enable
    
    f) In rules, change default text to this text and click Publish:
  
                {
                  "rules": {
                    ".read": "auth != null",
                    ".write": "auth != null"
                  }
                }
        
    g) Go to data and copy your  URL ; for eg : mine is " https://ng-recipe-book-bb122.firebaseio.com/ "
    
  
    h) In VS CODE, go to src→ app→ shared→ data-storage.service.ts, in there paste that above link in .put() and .get(), and add recipes.json in the end.
    So the complete URL becomes:
    https://ng-recipe-book-bb122.firebaseio.com/recipes.json    [ NOTE : Copy your URL , NOT MINE. ]
    
    
     j) Click on settings icon adjacent to Project Overview → project settings→ copy your WEB API KEY [ NOTE: For example, mine is: AIzaSyDZ05eBcR-MkhYB3N5qh206ItCc-P-Qq1g ]
     
  
    k) Go to VS Code→ src→ environment→ Open environment.ts → Replace your key with mine written alongside firebase APIKey → Open environment.prod.ts→ Replace your key with mine written alongside "firebase APIKey".
    
    
    l) Open this:   https://firebase.google.com/docs/reference/rest/auth#section-create-email-password
    And copy endpoint link.


    m) In VS Code, Open src→ app→ auth→  auth.service.ts  → replace my link with your endpoint link in signup {} function.  
    [ NOTE: exclude [API_KEY] in the end ]


    n) Open this:   https://firebase.google.com/docs/reference/rest/auth#section-sign-in-email-password
    And copy endpoint link.


    o) In VS Code, Open src→ app→ auth→  auth.service.ts  → replace my link with your endpoint link in login {} function.
    [ NOTE: exclude [API_KEY] in the end]
  
  
    p) Save all the files.
    
    
    q) Open a new command prompt running as administrator, type:
    
       $ cd final-project
       $ ng serve
  
  
    q) You can check the application running on “ localhost:4200 ” in your browser.

 
 - Build your project by typing this in Command Prompt running as administrator:
 
        $ ng build --prod
 
 
 - After that you need to install firebase-tools, type:
 
        $ npm install  -g  firebase-tools
    
        It will prompt you to log in. So through CLI, log in to your firebase account
  
 - Finally, the last step is, open Command prompt (Administrator), write these commands :
 
        $ cd final-project
        $ firebase init
        
        Then follow these steps:
        
        press enter for Y → With down arrow key go to  hosting , press space to select, then press enter → choose an existing project the project ( ng-recipe-book) → write this in terminal when asked about public directory: dist/ng-complete-guide-update → Yes ( for single-page app) →  No ( for overwrite).
        
        Then type this command in terminal:
        
        $ firebase deploy 
        
        Copy the hosting URL provided by your Firebase CLI. Enter in browser to see your app running on a hosted server.

      
