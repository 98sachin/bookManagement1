# bookManagement1

# the server we are making here is a local server i.e., why we are using "HTTP" and running on port= 8081. If you want to make the server global use "HTTPS".

# Book Record Management System(Library Management)
 we will first build a Server 
 this server will be handling 
        > storing book data
        > user registration
        > subscription
        >> the books.json file created in the data folder is to get/store the books information.

# different types or Routes and Endpoint we'll have here :-
## /users 
    > GET (to get the list of all users)
    > POST (all the user information when the user want to register or simply to create a new user)
    >> the users.json file created in the data folder is to get/store the user's information.

## /users/{id}
GET: get a user by id
PUT: update a user by id
DELETE: delete a user by id (check if the person has the book issued and its still with them and if there is and pending payment or fine to be collected).

    >> subscription
        > 3 months (basic subs.)
        > 6 months (standard subs.)
        > 9 months (plus subs.)
        > 12 months (premium subs.)

# /users/subscription-details/{id}
GET: get user subscription
    >> date of subscription
    >> valid till
    >> fine (if any)

# /books
GET: get all books 
POST: add new books in the library/system

# /books/book/{id}
GET: get book by id
PUT: update a book by id

# /books/issued
GET: get all issued books

# /books/issued/withFine
GET: get all issued books with fine

# fineCalculation
    >> If the user has an issued book and the issued book is to be returned on 01/01/2024 and if the user missed the date of renewal or return , then the user needs to pay a penalty/fine of 100 INR. 

    >> If the user has an issued book and the issued book is to be returned on 01/01/2024 and if the user missed the date of renewal or return also if the user's subscription is expired, then the user needs to pay a penalty/fine of 200 INR. 


# to get the server started we need to install :-
    >> npm init
    >> npm i express
    >> npm i nodemon --save-dev (this --save-dev is written which indicates that its a developer dependency)

to run the application, follow the command below:-
    >> npm run dev