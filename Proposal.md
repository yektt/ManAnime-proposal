## Application purpose

#### Who will use the application?

  The MangAnime application will serve people who would like to
  * get information about an anime or a manga,
  * rate & review animes watched or mangas read for future watchers or readers,
  * find a direct link to watch animes from an official website,
  * share their thoughts or discuss something about an anime or a manga,
  * save what they have watched or read so far,
  * talk about the differences between an anime and its manga,
  * save animes or mangas to their list to watch or read them in the future.
  </br>        

#### Why it is needed and useful?
    
Before starting an anime or a manga, it's good to know if it's worth to start. With this application, people can find information about animes & mangas and can communicate with other people. They can also check the ratings and reviews of an anime or a manga and decide if they should watch or read it. Moreover, users can check if they have watched an anime or a manga before. So, they will not waste time watching or reading the same thing until they remember that they have already watched it or read it. They can see if they have given any rating to an anime or a manga and recommend it to someone else. All in all, users will save time and spend their time more efficiently and pleasantly. Moreover, they will join a community and will be socialising. </br>

## Front end

#### CSS
For the CSS part of the project, I am thinking of using Bootstrap for all the pages except for the Home Page. For the home page, I will write a CSS file from scratch. I am thinking of using 'grids' and its attributes to make animes and mangas in blocks. You can check the 'views.pdf - home page' as a reference.

#### JAVASCRIPT

I am planning to use JavaScript in these places;
1. For writing comments asynchronously,
2. For writing replies asynchronously,
3. For submitting ratings & reviews asynchronously,
4. For checking if any of the checkboxes are clicked
5. For adding or deleting a character to a manga or an anime in adding anime or manga pages,
6. For searching for an anime or a manga asynchronously in the search page;
    - Results will change with every character entered in the search bar. 
    - Other than that, there will be an 'advanced search' button. Search page HTML code will contain the HTML code for advanced search, whose display attribute will be hidden. When a user clicks it, the hidden part's display attribute will change from 'hidden' to 'inline'.

#### HTML
! Animes and mangas both belong to the "content" model. In the following parts, I will be using 'content' for referring to both. 

##### Header
The header will contain different elements for every user role.

  * For anonymous user:
    - Logo and home links: When users click any of them, they will head to the home page. These links will be reachable from all pages.
    - Anime list link: This link will display the anime list page when it's clicked.
    - Manga list link: This link will display the manga list page when it's clicked.
    - Search link: This link will display the search page when it's clicked.
    - Login link: This link will display the login page. 
    - Sign-up link: This link will display the sign-up page.
  </br> 

  * For logged-in registered users: Except for the login and sign-up links, all the other header elements are the same for this user type. Additionally, this user type has a profile and logout link in the header.
    - Profile link: This link will display logged-in user's account.
    - Logout link: When the logged-in user clicks this link, the opened session will be closed. The home page will be displayed in an anonymous user's perspective.
  </br>

  * For logged-in admins: All the header elements will be the same with logged-in registered users. There are two more links as extra in the header for admins.
    - Add link: this link will display an add page, for adding content to the application, when admins click it.
    - Reports link: this link will display the reports page when admins click it.

##### Footer
Footer will change its attributes according to different types of users.

  * For anonymous and logged-in users, there will be the following links in the footer;
    - Home link: it will display the home page when a user clicks it. This link is reachable from all pages of the application. 
    - About link: this link will direct the user to the about page
    - Help & Rules link: this link will direct the user to the rules page
    - Contact link: this link will direct the user to the contact page.
  </br>

  * For admins; the home link, about link and contact link will be displayed and will function in the same way as from logged-in users’ perspective.
    - Rules link will be different from other types of users. The general rules link will be hidden. Admin rules link will be displayed instead, and will direct admins to the admin rules page.

! All pages that will appear in the following parts have the same header and footer. These information will not be repeated in the following parts.

##### Home Page
The home page will welcome all the users. From every page of the application, it will be reachable. Users can see the most popular six animes and six mangas of all times on this page.
There will be images and names of the content that are displayed in grids. When users click one of these grids, they will be directed to that content's show page.

##### About Page
About page will explain why this application was made and by whom.

##### Help & Rules Page
This page will be mixture of terms & condition and help page. It explains what is forbidden to do and what a user can do as a registered user in detail.

##### Contact Page
In this page, users can send email to admins. Users must fill the email and body fields.

##### Admin Rules Page
Only admins can see this page. This page explains how and under which conditions admins can block a user, how they can add a content, how they can promote a user to admin status, and so on.

##### Anime List Page
I am planning to display this page in four parts:
  * In the first part, the most popular three animes will be displayed in a modified version of Bootstrap's .card component.
  * In the second part, the most popular unfinished three animes will be displayed in a modified version of Bootstrap's .card component.
  * In the third part, the most recently released three animes will be displayed in a modified version of Bootstrap's .card component.
  * In the last part, all the animes will be displayed in alphabetical order in a modified version of Bootstrap's horizontal .card component.

In the first three-parts, if an anime has got enough rating from users, the rate of that anime will be presented on the top right corner of the card element.

All four parts will be a part of a .grid layout. As such, it will be easy to display all the components nicely when screen size changes.

##### Manga List Page
I am planning to display this page in four parts:
  * In the first part, the most popular three mangas will be displayed in .card component with some modifications.
  * In the second part, the most popular unfinished three mangas will be displayed in .card component with some modifications.
  * In the third part, the most recently released three mangas will be displayed in .card component with some modifications.
  * In the last part, all the mangas will be displayed in alphabetical order in a horizontal .card component with some modifications.

In the first three-parts, if a manga has got enough rating from users, the rate of that manga will be presented on the top right corner of the card element.

All four parts will be a part of a .grid layout. As such, it will be easy to display all the components nicely when screen size changes.

##### Search page
In this page, users can search through the database for a content. Users can use the name, genre, tag or release year of contents. As mentioned under JavaScript, users can make an advanced search by clicking the 'advanced search' button. After clicking the button, a list will be displayed under the search bar which will contain the following options as checkboxes:
  - Starting decade of content: this option will start from the oldest content's decade and will continue up to the current decade.
  - Genres: all genres will be displayed here. Users can choose which genre they would like to search in.
  When users click them, the result will change with each input.
  Users can search in detail with these advanced search options. With these options, users can get more specific results that are not possible with the search tab.

##### Login page
In this page, users have to enter their email and password combination correctly. If they don’t enter the correct combination or forget to fill any of the fields, they will get a warning.
After a successful login, the application will lead the user to the home page.
If a user is blocked, they cannot log in to the application even if the request is met. They will see a pop-up message which contains the reason why they have been blocked, a link to the contact page and another link to the rules page.

##### Sign-up page
In this page, users can create a new account in the application. They have to enter a valid email address and a password to sign up. The application will check if they have entered a valid email. The password field will be displayed as password input.
After users sign up in the application, the application will lead them to their profile page. Thus, if they wish, they can edit their name or image which will be given default.

##### Add page 
Only admins can reach this page. This page is for adding content to the application's database. It has four buttons to lead to different content adding pages:
  * Anime adding: it opens a page for adding an anime to the database.
  * Manga adding: it leads to a page for adding a manga to the database.
  * Character adding: it leads to a page for adding a character to the database.
  * Genre adding: it goes to a page for adding a genre to the database.

! All adding pages will be explained in the following sections.

I will use a 'content table' in the database for animes and mangas. They will be stored in this table with a unique identification number. Anime or manga add pages will call the partial corresponding to the type of the content.
I will use a pop-up for adding characters in both these pages. This pop-up section will be explained in 'add character' page in detail. 

##### Anime add page
Only admins can reach this page. Admins can add new animes to the database on this page. Admins have to fill some fields to add new anime as: 
 * Anime name
 * Anime image: Admins can add it via an internet link or from local files.
 * The start date of the anime
 * How many seasons have been released
 * How many episodes have been aired
 * In which season the anime has been released: This part contains two sections: year and season. The year will be text input while the season will be a dropdown menu. The dropdown menu will have four seasons which are winter, spring, summer and fall. 
 * Genres of the anime: All genres will be displayed here as checkboxes and admins can choose more than one for the anime. 
 * Tags: Admins can add tags as text input. They have to be careful about two things; a tag shouldn't contain more than four words and each written tag in the text input has to be separated by a comma.
 * Anime description
 * Characters: This part of the page is a bit different from the other parts. It contains a search bar. When admins would like to add a character, that has already been added in the database, they can type their name or surname to this search bar. If a character has not been added to the database so far; admins don't have to go to the 'add character page'. They can click the button just next to the search bar. When this button is clicked, there will be a pop-up for adding a character to the database. So, admins can save time.
    All added characters will be displayed under the search bar. If admins have picked a wrong one, they can delete it facilely by clicking the red cross at the end of the character's name.

Some fields are optional to fill. These are:
 * An official link to watch
 * The end date of the anime

##### Anime edit page
Only admins can reach this page. If there is missing or wrong information about an anime, admins can fix it via this page. This page is similar to the add anime page. The differences between them are; 
  * All information, which has been entered for the anime, will be written in the inputs boxes. Like this, admins can see all the information that has been entered and which information should be edited. 
  * All added characters to the anime will be displayed under the character search bar. Admins can add new ones or remove an added one.
  * All genres that have been chosen for the anime will be displayed ticked. Admins can add more genres or can untick the checkbox of a genre to remove it.
  * All tags that have been written for the anime will be displayed separately under the tags input bar. At end of each one, there will be a red cross to remove the tag.

##### Anime show page
This page is reachable for all users, but the appearance and the functionality will change in some parts according to different user roles. These differences will be explained at the end of this section.
This page contains two main parts:

  1. Information about the anime: In this part, anime's image, name, start date, end date -if it has one-, description, link to watch from an official website, the average rating from the users (if more than three users have rated it), episode number, season number, genres, tags and finally characters will be displayed. 
  Characters will be displayed as grids. Each grid will contain two attributes about the character. These will be the name and the image. When users click the character's grid (the image or the name), show character page will be displayed for that character. This attribute will be the same for each user.
  </br>

  2. User's opinions: This part has two tabs. 
  
  * The first tab that welcomes to the users is the 'comments' tab. In this tab:
    - All comments will display with their replies. Each one will have clickable report, reply, upvote, downvote, edit and delete icons. The appearance of these icons will change up to the user role. These changes will be explained at the end of this section.
    - Comments will be displayed in a wide flexbox. It will contain the commenter's image and name as well as the comment body and the time the user has created the comment. If there are any replies to that comment, they will be displayed a bit narrower and under that comment. 
    - Replies will contain the replier's image and name as well as reply body and when the user has created that reply. Each reply will have a delete icon. 
    - User can write a new comment. There will be an input box and submit button to add a new comment asynchronously. 
    </br>
  * The second tab will be ratings & reviews tab. In this tab:
    - Users can see the previous ratings & reviews about this anime. Reviews will be in different categories. For example, a user can add a review to criticize about the anime in general or for the ending. 
    - When a user wants to fill this part, they don't need to fill the review part but have to fill rating part. There will be an input box to write a review and a dropdown menu from zero to ten for rating to the anime.
    - If the user has already given a rating to an anime, they will not be able to change or give it again for that anime.
  
###### This page from an anonymous user's perspective: 
An anonymous user can see all the details about an anime and can see all comments and rating & reviews. But they cannot;
  * Write, upvote, downvote, edit, reply or delete a comment: all icons will be displayed faded or hidden.
  * Give any rating to the anime: rating & reviews inputs will be hidden for anonymous users.

###### This page from a logged-in user's perspective:
A logged-in user can see all the details about an anime and all comments and ratings & reviews as anonymous users. As extra, they can;
  - Add the anime to their anime list by clicking 'add anime to my list' button. This button is available only for logged-in users and admins,
  - Write a comment,
  - Edit or delete a comment they have made,
  - Upvote, downvote, report any comment,
  - Write a reply to any comment,
  - Write a review and give a rating to the anime.

###### This page from an admin's perspective:
An admin can see all the details about an anime, all comments and ratings & reviews as logged-in users. As extra from logged-in users, they can;
  - Edit the anime by clicking the 'edit' button. This button is available only for admins.
  - Delete any reply.
  - Delete any comment and its replies with it if it has.
  - Delete any reviews about the anime. Rating cannot be deleted. Thus, the average rating for the anime will not change.

##### Manga add page
Only admins can reach this page. Admins can add a new manga to the database on this page. 
Admin has to fill some fields to add new manga as: 
 * Manga name
 * Manga image: Admins can add it via an internet link or from local files.
 * The start date of the manga
 * How many volumes have been published
 * How many chapters have been released
 * In which season the manga has been released: this part contains two sections: year and season. The year will be text input while the season will be a dropdown menu. The dropdown menu will have four seasons which are winter, spring, summer and fall. 
 * Genres of the manga: All genres will be displayed here as checkboxes and admin can choose more than one for the manga. 
 * Tags: Admins can add tags as text input. They have to be careful about two things; a tag shouldn't contain more than four words and different tags in the text input have to be separated by a comma.
 * Manga description
 * Characters: This part of the page is a bit different from the other parts. This part contains a search bar. When admins would like to add a character, that has been already added in the database, they can type their name or surname to this search bar. If a character has not been added to the database so far; admins don't have to go to the 'add character page'. They can click the button just next to the search bar. When this button is clicked, there will be a pop-up for adding a character to the database. As such, admins can save time.
   All added characters will be displayed under the search bar. If the admin has picked a wrong one, s/he can delete it facilely by clicking the red cross end of the character's name.  

One field is optional to fill. That is:
 * The end date of the manga

##### Manga edit page
Only admins can reach this page. If there is missing or wrong information about the manga, admins can fix it via this page. This page is similar to the add manga page. Only differences between them are;
* All information, which has been entered for the manga, will write in the input boxes. Like this, admins can see all the information that has been entered and which should change. 
* All added characters to the manga will be displayed under the character search bar. Admins can add new ones or remove an added one.
* All genres that have been chosen for the manga will be displayed ticked. Admins can add more genres or can untick the checkbox of a genre to remove it.
* All tags that have been written for the manga will be displayed separately under the tags input bar. End of each one, there will be a red cross to remove it.

##### Manga show page
This page is reachable for all users, but the appearance and the functionality will change in some parts for different users. These differences will be explained at the end of this section. This page contains two main parts:

1. Information about the manga: In this part, manga's image, name, start date, end date -if it has one-, description, average rating from the users (if more than three users have rated it), chapter number, volume number, genres, tags and finally characters will be displayed. 
Characters will be displayed as grids. Each grid will contain two attributes about the character. These will be the name and the image. When a user clicks the character's grid (the image or the name), show character page will be displayed for that character. This functionality will be the same for each user. 

2.  The comments and ratings & reviews tabs which are the same as the anime show page. Their descriptions will not be repeated for this page.

###### This page from an anonymous user's perspective: 
An anonymous user can see all the details about a manga and all comments and ratings & reviews. But they cannot;
  * Write, upvote, downvote, edit, reply or delete a comment: all icons will be displayed faded.
  * Give any rating to the manga: rating & reviews inputs will be hidden for anonymous users.

###### This page from a logged-in user's perspective:
A logged-in user can see all the details about a manga, all comments and ratings & reviews. As extra, they can;
  * Add the manga to their manga list by clicking 'add manga to my list' button. This button is available only for logged-in users and admins,
  * Write a comment,
  * Edit or delete a comment they have made,
  * Upvote, downvote, report a comment,
  * Write a reply to any comment,
  * Write a review and give a rating to the manga.

###### This page from an admin's perspective:
An admin can see all the details about a manga, all comments and ratings & reviews. As extra from logged-in users, they can;
  * Edit the manga by clicking the 'edit' button. This button is available only for admins,
  * Delete any reply,
  * Delete any comment and its replies it if it has any,
  * Delete any reviews of a user about the manga. Ratings cannot be deleted. Therefore, the average rating for the manga will not change.

##### Character add page
Only admins can reach this page. In this page, admins have to fill some fields for creating a character to add to a content later. For adding a character, admin has to fill these fields:
  * Character's name
  * Character's surname
  * Character's picture: admins can add it via an internet link
  * Character's information: This part is a bit different from other parts of the page. Here, admins can put a certain text in between a specific character to embolden it. They can also use '\</br>' to go to the beginning of the line.
  For example; this will be the input for the character's information:
  '\<b>Birthday\<b>:02/07/1839\</br>This character is the main character.' It will be displayed on character show page as: 
  "**Birthday**: 02/07/1839
  This character is the main character."
  This way, admins can add specific information about each character without overloading the database.

##### Character show page
This page is reachable for all users, but the appearance and the functionality will change in some parts for admins.
In this page, there will be three main sections:
  * Character's information: In this part, the character's image, name, surname and information will be displayed.
  * Animes: In this part, all animes in which this character has a role, will be displayed. If there is no such an anime, this part will not be present on the page.
  * Mangas: In this part, all mangas in which this character has a role, will be displayed. If there is no such a manga, this part will not be present on the page.
I am planning to create each content mentioned above as grids. Each grid will be clickable and will contain content's picture and its name under the picture. When a user clicks them, the corresponding show page will be displayed.

###### From an admin's perspective:
There is only one button, which is 'edit' button, on top of other users' views. Admins can reach character edit page by clicking this button.

##### Character edit page
Only admins can reach this page. If there is missing or wrong information about a character, admins can fix it via this page. This page is similar to add character page. The difference between them is that all information, which has been previously entered for the character, will be written in the input boxes. As such, admins can see all the information that has been entered and what should be changed. 

##### Genre add page
Only admins can reach this page. In this page, there is only one input: the name of the genre. If there is a new genre which is not in the database, admins can add them easily by using this page.

##### Reports page
Only admins can open this page. 
In this page, admins can see if there is any comment which has been reported, with its author and reporter. These three details of the report will be clickable. Thus, admin can go without spending any energy to solve the reported issue. 
There might be two situations:
1. When reported comment is not against the rules, admin has the authority to delete the report.
2. If there is a comment against the rules, admin can delete the comment. When they delete it, the report will disappear automatically with all other reports for the same comment. 

##### Profile page
In general, this page's elements are in one direction. Because of that, I am planning to use flexbox on this page. This page has two parts: 
  * Information about the user: user's avatar, user's name, when the user has become a member of this application, user's role such as admin, user and blocked, the last comment of the user. 
  * Anime and manga lists tab: If the user added any anime or manga to his/her lists, these would be displayed in these tabs. 

###### This page from an anonymous user's perspective:
The anonymous user can see the user's information as well as user's anime and manga lists.

###### This page from an logged-in user's perspective:
  * If the user is looking at someone else's page: it will be same with the anonymous user perspective. There will not be any action for the logged-in user.
  * If the user is looking at their own page: the user can see an 'edit' button at the top right corner. When the user clicks this button, they can edit their own account. Edit page will be explained in the following sections.

###### This page from an admin's perspective:
  * When admins open a registered user's page, they can see two buttons:
    - 'Block' button: If the user has done something against the rules, the admin has the authority to block that user with this button so that they cannot enter the application again. 
    When an admin clicks this button, a pop-up will appear and show all possible reasons to block a user. Admin should choose the reason why they are blocking the user.
    - 'Make admin' button: If admin wants to promote a user from 'registered' to 'admin', they should use this button. Other than this button, there is no way to change the role of a user.
  * When admins open their own pages, they can see an edit button like other users but, cannot see the block and make admin buttons.
  * When admins open another admins' page, they cannot see edit or make admin button. But they will be able to block that admin by clicking block button.

##### Edit profile page
Only a logged-in user can reach this page for editing their account. In this page, the user can modify the following information about their profile:
  * User's name
  * User's avatar: for editing the user's avatar, there are two ways. User can upload an image from local or can paste a link of an image from the internet. 

##### Log out link
It's available for a user when they log-in. When the user logs in the application, a session will be opened for that user. When the user wants to finish the session, it will be enough to click log out link.

## DATA STRUCTURE AND MODELS

The database of the application will be explained in this section.

**Model_name** : explanation about the model.
  * attribute_name **!\*** : attribute_type 
  * attribute_name **!** : attribute_type
  * attribute_name : attribute_type
  * attribute_name **\*** : attribute_type

  the **\*** means; presence: true
  the **\!** means; uniqueness: true

**model_relationship**
belongs_to : another_model

**User model**: This model will be used for registered users or admins.
  * email **!\*** : string
  * password_digest* : string
  * role **\*** : string inclusion: {in: %w(registered admin)} (default will be registered)
  * name : string
  * is_blocked **\*** : boolean (default will be false)
  * avatar : string
  * avatar_url : string

  ! If the avatar or avatar_url are empty, an image will be assigned by application.
  ! If the name is empty, a name will be assigned by application.
  
  has_many: comments
  has_many: replies
  has_many: review
  has_and_belongs_to_many: contents
  has_and_belongs_to_many : reports

  has_secure_password
  mount_uploader : avatar, AvatarUploader

**Content model**: This model will be used for animes and mangas.
! For this model, I am still thinking if should I split the model as anime and manga for response time of the page. 
! I am planning to use SecureRandom for id of content model's elements.
  * name **\*** : string
  * type **\*** : string - inclusion: {in: %w(anime manga)} 
  * start_date **\*** : time
  * end_date : time
  * tags : string
  * link_to_watch : string
  * description **\*** : string
  * volume_or_season_number **\*** : number
  * chapter_or_episode_number **\*** : number
  * image : string (from link)
  * image_url : string (from local)
    - One of the image or image_url attribute should be filled. This check will be held in HTML part of adding and editing content's page.
  
  has_many : comments
  has_many : review
  has_and_belongs_to_many : users
  has_and_belongs_to_many : genres
  has_and_belongs_to_many : characters

**Character model**: This model is for anime's and manga's characters.
  * name **\*** : string
  * surname **\*** : string
  * information **\*** : string

has_and_belongs_to_many : content

**Comment model**: This model is for anime's and manga's comment.

  * body **\*** : string
  * user_id
  * content_id
  * upvote : number (default will be 0)
  * downvote : number (default will be 0)

  belongs_to : user
  belongs_to : content
  has_many : replies, dependent: :destroy
  has_and_belongs_to_many : reports

**Reply model**: This model is for comment's replies.

  * reply_body **\*** : string
  * user_id
  * comment_id

  belongs_to : user
  belongs_to : comment

**Review model**: This model is for making ratings & reviews for a content.

  * review_body : string
  * rating **\*** : number
  * user_id
  * content_id
  * categories : string

  belongs_to : user
  belongs_to : content

**Genres model**: This model is for genres' of a content.

  * name **!\*** : string
  
  has_and_belongs_to_many : content

**Report model**: This model is for saving a report.

  * reporter_id 
  * comment_id
    
  has_and_belongs_to_many : user
  has_and_belongs_to_many : comment

## THIRD PARTY SERVICES

* kaminari gem : for paginating the results
* bcrypt gem : for crypt the password safely
* carrierwave gem : for uploading images from local
* fog-aws and figaro gem : for being able to upload images from local when application is alive.
* filterrific gem : it will be used for filter, search, and sort in search page.
* mail_form gem : for sending mails from users to the admins in contact page.
* Bootstrap CSS library
* Heroku : for making the application alive.
