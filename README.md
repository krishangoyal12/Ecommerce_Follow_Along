# Ecommerce-Follow-Along
'E-commerce website'  follow along project for Semester 2

***Milestone 1***: **Project Overview**

In todays live session our mentor introduced us to overall structure of MERN Stack.
He taught us the foundational steps to set up the environment for future milestones, we created a new repository for our follow along project.

***Milestone 2***: **Front-end setup and login page**

In todays live session we learnt to organize the files into separate frontend and backend directories.

Set up React for frontend

Node.js setup for backend

Tailwind CSS configurations

We also designed the front end for login page of the e-commerce application.


***Milestone 3***: **File organizing and MongoDB**

Set up dedicated folders for organizing backend code effectively.
Initialize and configure a Node.js server to handle API requests.
Connect your application to MongoDB to store and manage data.
Implement basic error handling to ensure your server runs smoothly.

***Milestone 4***: **Created and Configured Files**

Created a User Model: Our mentor explained how a MODEL in MVC architecture works and how it interacts with database.
Created a User Controller: We got to know the purpose of a controller in MVC.
Enable and Configure Multer: In the live session mentor told us what is a multer and what is it used for and how it can be configured to handle file uploads.

***Milestone 5***: **Created Frontend UI for signup page and added the code for authentication of the inputs**

In this part of the Follow Along project we made the UI (Frontend) for the sign up page of our website. This page allows the users to add their details.

After the user is done with entering backend comes into play. Backend does the form validation part, it verifies whether the user has entered the details in the right format(e.g. email, minimum length)

***Milestone 6***: **Backend for Signup page and password encryption**

1. Encrypt the Password Using bcrypt

During the user signup process, encrypt the user's password using the bcrypt hashing algorithm. This ensures that the password is stored in a secure, non-reversible format.
The bcrypt algorithm adds a "salt" to the password before hashing, making it resistant to common password-cracking techniques.
The hashed password should never be stored in plain text.

2. Save the Hashed Password in the Database

Only store the hashed version of the password in the database.
Do not store plain text passwords for security reasons.
Ensure the hashed password is securely saved in the database along with other user information.

3. Store Complete User Data

In addition to the hashed password, save the user's other information, such as their name, email, and any other relevant data.
The complete user data should be stored securely, ensuring that sensitive information like the password remains encrypted.

4. Handle Login with Hashed Passwords

During the login process, compare the entered password with the hashed version stored in the database.
Use bcrypt to safely verify if the entered password matches the stored hash.

***Milestone 7***: **Backend endpoint for user login**

In this milestone we implemented the backend for our login page, which will be validating user credentials and verifying the encrypted password already stored in the database.

Firstly we created an endpoint for user login to enable user to enter the credentials like email,username,password.

Then retrieving the data particular user from the database.

Validate the entered data using tools like `bcrypt` to hash the entered password.

Compare the hashed password with the data stored in the database for authentication.



***Milestone 8***: **Creating frontend for home page**

In this milestone we will be creating card components for showing product cards on the home page.

Then we will be implementing the functionality to display the cards dynamically.

Then we will be designing overall layout of the home page.



