# newsapp
**********     Project     **********
 * A basic news application (NEWSNEWS)

 **********     Overview     **********
 This is a simple looking news application created with vue.js where a user can read news, delete news and add news on the app. This project is to help me understand how vue.js works and also to improve on my web development skills.

 **********     Technologies used     **********
 - Vue
 - Vanilla CSS (because of insufficient knowledge on CSS frameworks :| )

**********     Description     **********
This web app is composed of an App.vue component and six other components (details below). Let's go through individual components to better understand how they combine to work as a unit

----- App.vue -----
- This is the component in which most of the other components are imported into. It contains data that accessible to the other conponents through props based on which functionalities are executed

----- navbar.vue -----
Here acts as the navigation center (obviously :)). It contain tabs that helps you navigate the app. (Some of the tabs haven't been assigned functionalities yet except for the 'My News' tab).
   - The News App - click on this to show a drop down containing the 'Add News' and 'Delete News' functionality
   - Add News - click on this to reveal a form where news will be added
   - Delete News - click on this to delete news from the app

----- header.vue ----- 
This component displays the app name 

----- newsForm.vue -----
This form takes news updates from the user and adds to the app
It has a news title field which takes the title of the news to be posted and a news headline field which takes a summary of the news to be posted

----- newsSection.vue -----
This is where the individual news will be displayed. It has the news.vue component embedded in there

----- news.vue -----
This is the news component. It displays an image (which is supposed to be specified by the user but my app uses a general image) and the news title and headline data taken by the newsForm.vue component and displays it using a computed function. News are clickable, meaning it should lead to the main content of news but for now that has not  been added

----- footer.vue -----
The footer component displays social media icons and links which doesn't have or do or link to anything yet.

**********     End Note     **********
This is how my news app (NewsNews) works... its pretty limited but I'm looking forward to add more functionalities and also connect this to a database to make it a fully functional application.

Thank you.... :) :) :)







