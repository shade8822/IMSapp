# IMSapp
Inventory Management System For Books

READ ME FILE FOR IMS APP OR INVENTORY MANAGEMENT APPLICATION

Purpose:

The IMS app or Inventory Management App is designed to store an inventory of books.  The user will login, add books to the database using the “Data” tab, then search the database using the “Search” tab. 
 
Installation:

Double-click the setup.exe file to install the necessary components for the program to operate correctly.  The program may run after the installation of the Microsoft SQL software bundle.  The first application window that the user will see is a login page.  

How it works:

There is a database file that stores the book data.  That database is linked to this program.  The text fields in the data tab are sent to the database when the user creates a record, fills out that record, then clicks the save record button.  YOU MUST CREATE A RECORD BEFORE FILLING OUT THE TEXTBOXES IF YOU PLAN ON SAVING THE DATA IN THE TEXTBOX TO THE DATABASE.

1.	 Click the create record button
2.	Fill out the record with the book information.  THE “Id” FIELD, ALSO KNOWN AS THE IDENTIFICATION NUMBER FIELD, MUST BE UNIQUE.  Primary keys must be not null, and unique for a database to function.  The program will close to prevent the user from violating database rules.  These numbers refer to separate books.  IT IS RECOMMENDED TO START WITH A NUMBER SUCH AS 10000001 AS THE FIRST BOOK’S ID NUMBER, SO THAT YOU CAN HAVE AN 8-BIT NUMBER AND THE NUMBER OF DIGITS ARE THE SAME FOR EVERY BOOK (NO TRAILING ZEROS TO DEAL WITH).  Using 8 digits will also allow for a robust book inventory without running out of 8-digit combinations.  SEE “Data Tab” ILLUSTRATION.
3.	Press the save record icon.  The save button will update the database table so that the entered data will override the existing data.  

Buttons on Data Tab:

First: will highlight the first record
Previous: will highlight the previous record
Next: will highlight the next record
Last: will highlight the last record
Add: will add a new record.  The add button is required before data can be saved.
Delete: deletes a record permanently.
Save: saves a record to the database table.

Login Page:
 
The user will enter their username in the username textbox and their password in the password textbox, then click “Login.”  If the credentials are correct, then the group box will hide itself, and the user will be able to view the search and data tabs.  If the credentials are wrong, then the user will notice that the username and password they entered in the textbook will disappear.  This communicates a failed attempt.  The system will close if the credentials are entered incorrectly three times.  The user will have to re-launch the program to try again.  

***Professor note:  The credentials are “Username” and “Password”, “username” and “password”, or “user” and “pass”.  

Search Tab:
 
The search tab is designed to search for titles, authors, genres, or ISBNs of books in the database.  The search fields are not case sensitive; however, they may need to be typed in the correct order to get a match.  For instance, the search result will come up with “Rice, Anne” if I type in “rice” then press the search button.  However, the record will not show if a user types “Anne” and clicks the search button, because I entered the last name first when I entered the record into the database.  The search box works well with case sensitivity, but it doesn’t function well with order of terms.  The user must use the search button that corresponds with the adjacent search textbox.  Only one search category can be searched at a time.  Any data in the fields outside of the current search field will be ignored. The user may try searching for “The Covenant” if “Covenant” doesn’t come up in a title search.

Step 1: Fill in one of the fields.  Only the field near the clicked search button will be searched.
 
Step 2:  Click the corresponding search button.  The genre will fill in with the first result’s genre.  
 
Step 3: Make sure to clear the searched field and press “search” to view all records once more, or else they won’t show on either the search tab or the data tab pages.
 
Data Tab:
 
The data tab is where records are added to the database.  Entering the records in the same format for each book is important to maintain consistency and to be able to search easily from the other tab later.  My database stores 10000001 as the first book so I can store an 8-bit number, there are no leading zeros, each record will have the same number of digits, and so I don’t run out of numbers for books.  I enter the authors in last name first because most libraries operate in the same manner.  The genre section consists of a drop-down menu.  The ISBN should be ISNB-13 codes for the titles, like in the illustration.  The quantity is an integer type value.  The price is a DECIMAL (13,2) type for use with currency.  Empty fields will produce a reminder warning on the screen when the user presses the save button.  
