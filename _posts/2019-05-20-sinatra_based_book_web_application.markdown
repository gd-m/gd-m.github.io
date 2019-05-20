---
layout: post
title:      "Sinatra Based Book Web Application"
date:       2019-05-20 19:41:45 +0000
permalink:  sinatra_based_book_web_application
---


I have created a web application for books, where an user can make a book entry with book name, author name and notes on that particular book. He can share this book entry with all the users of the application.


This sinatra based web application has two models : 
1. User
2. Book


* User : Users of the application can sign in , sign up and sign out. As an user, you can keep track of books you read and notes regarding the same.
					
* Book: Book model has all the details regarding book_entries. 

**Associations** 

The main association in this web application is 
		1. user has_many book_entries
		2. book belongs_to user

  So the book_entry table will contain the column of user_id. 
	
**Schema of the Database**
* User's table : 
It will have following deatils:
 1. name
 2. email
 3. password (password_digest as i have used bcrypt to encrypt passwords of the users) 
 4. timestamps (created_at and updated_at)
                              
* Book's Table : 
It will have following details:
 1. User_id
 2. Book Name
 3. Author
 4. Notes
 5. timestamps (created_at and updated_at
                    
										
**Flow of the Web Application**

When an user is signed in , it will be directed to the home where all the book entries of all the users are listed. Each book entry will have a book name, authors name, notes and a name of the user who created that book entry. User name will have a link which will take to the User's profile. Profile will have Name of the User , Number of Book entries he has created and Number of unique authors in his book entries. 
'Books' page is a index page of all the books a user has created . here an user can see all the books he created. Each book entry in this list is clickable and will take to the show page of that particular book entry, where user can see the details of that book entry. Also this show page will contain the edit and delete button which a user can use to update the book entry of delete the book entry. 
Logout tab in the navigation bar will end the user's session and log him out of his profile and take to the welcome page of the web application. 

***features of the web application which i think are useful and logical in this web application***

* When user click on a web application logo : he will be directed to the home screen if he is logged in , if the user is not logged in then it will take to the welcome page of the home screen
* an user can visit other users' profile.
* user can see other user's book entry but will not be able to edit or delete it.
* The delete and edit button will not be visible to user if he doesn't own that book entry.
* User will be logged in automatically after the user sign ups for the first time. 


**GitHub repo link for this web application is as follows:
https://github.com/gd-m/sinatra-portfolio-project-book-list
Any contribution to this project is always welcome. Thank You.!
