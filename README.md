# Recipe-Book-Angular9
Build an awesome reactive front-end web application, designed especially for those who want to store all their recipe data in one place. In addition to that, they can separately manage the ingredients used for a particular recipe. It basically has two sections, a recipe book, and a shopping list. You can manage your recipes, view them in detail and manage the shopping list. You can even push ingredients directly from a recipe to shopping list but for that, you must be an authorized user

- As mentioned in the assignment, these are the two core functionalities that I implemented in my project:

    1. Login Route
    2. Products Route
    
## HOSTED- LIVE:

-If you want to see this app in real, then i have deployed that app on firebase.
    
    link: https://ng-recipe-book-bb122.firebaseapp.com/auth

- I have made a dummy user account for better User Experience. Login using these credentials:
        
        E-mail ID : test@test.com
        password   : tester

- After logging -in you must click on " MANAGE " (on top-right corner) and click on " FETCH DATA " to load all the recipes.

- To access source code: https://drive.google.com/drive/folders/105OmFucYwm21e2hlVNEZFfCtHJAxWlaN?usp=sharing

**[NOTE]: Please refer to HOW-TO-RUN.md file in order to run this code on your system. Otherwise, it won't work.**
    
## WEB- APP SCREENSHOTS:

**1. Login Route:**

- If a new user sign-up:

![](/recipe_book_screenshots/5.new_user_sign-up.png)

- Password Validation:If password entered is less than 6 characters:

![](/recipe_book_screenshots/1.password_validation.png)

- Password Validation:If wrong password is entered at the time of login:

![](/recipe_book_screenshots/9.wrong_password.png)

- E-mail Validation:E-mail must contain " @ " and " . " and some text after that:

![](/recipe_book_screenshots/2.email_validation.png)

- E-mail Validation:If wrong email-id is entered at the time of login / user does not exist:

![](/recipe_book_screenshots/3.if_user_not_exist.png)

- User can access shopping list column, but can't save any ingredient permanantly means, he  don't have access to the management console. 

![](/recipe_book_screenshots/4.can_access_shopping_list.png)

- Login Screen which will appear after successful login. After 1 hour of inactivity, the user will be automatically logged out.

![](/recipe_book_screenshots/6.after_logging_in-screen.png)

- User can now access management console. He can now add ingredients and can save them permanently so that after refresh or after logging in again he can click on FETCH DATA and all the previously saved ingredients data will be fetched.

![](/recipe_book_screenshots/7.now-you_can_manage.png)


**2. Products Route:**


- If user click on "NEW RECIPE", then the user can enter the required information related to recipe; **NOTE THAT: You must add image URL of an image present on the internet.As soon as the user enter the URL in the box, the image will be loaded automatically ffrom the internet**

![](/recipe_book_screenshots/10.new_recipe_add.png)

- User can add description of his/her recipe as per his choice. Also user have to add the ingredients and the quantity (in numbers only)required for the recipe. After adding all the details, user can click on SAVE to add the recipe in the catalog.

![](/recipe_book_screenshots/11.adding_ingredients.png)

- User have to select a recipe from the catalog. By just clicking on the recipe, user will be able to see the complete detail of the recipe which he has entered. User also have the option to edit recipe from here, delete recipe and can also push the ingredients to the shopping cart. (**NOTE -Tomatoes and Apples have by default added in shopping list just for demo purpose.YOu may remove them if you want**)

![](/recipe_book_screenshots/13.manage_recipe.png)

- Here is the list of all the ingredients along with the quantity specified by the user. So basically this acts as a checklist for the user, so that he/she knows what ingredients he has to buy.

![](/recipe_book_screenshots/14.item_added_to_shopping_list_&_managing_shoppinglist.png)

- User must click on " SAVE DATA" in order to permanently save your recipes. So that the next time when you login, by just clicking on " FETCH DATA" you can fetch all your previously written recipes.

![](/recipe_book_screenshots/15.Saving_data.png)

- Here is the catalog of all the recipes created by the user. User can view any recipe he wants from here.

![](/recipe_book_screenshots/16.once_added_all_recipes.png)

In case of any help or suggestion, you can contact me at **mridul.mark@gmail.com** 
