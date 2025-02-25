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

***Milestone 9***: **Creating forms**

Created the form for products.

This form will take multiple product images images as input.

***Milestone 10***: **Creating mongoose schema**

In this milestone we learnt how to define product schema.

Learnt how to create an end point to validate and store product details in mongodb.


***Milestone 11***: **Creating Endpoint for interacting with Database**

- Adding new products with required details such as name, description, category, price, stock, and images.
- Fetching all products or filtering products by the user's email.

The application is built with the following core components:

Express.js: Framework to handle HTTP requests.
MongoDB: Database to store product and user data.
Multer: Middleware for handling file uploads (product images).
Mongoose: ODM for MongoDB to interact with the database.

***Milestone 12***: **Creating MyProducts page**

In this milestone, we are focusing on creating a "My Products" page that will display all the products added by a user, based on their email. We will achieve this by creating a backend endpoint to filter and send the products that match the user's email stored in MongoDB. On the frontend, we will dynamically display the data using the Product Card component that we created in a previous milestone.

In this milestone we learnt:


How to write an endpoint that filters products by email and sends the filtered data from MongoDB.

How to fetch the filtered data in the frontend and display it dynamically using the Product Card component.

**Steps followed:**

Backend Development:

Write an endpoint that will filter all products stored in the database by the email of the user.
Fetch the products from MongoDB based on the email passed from the frontend.

Frontend Development:

Write a function to fetch all the products data by email from the backend.
Display the fetched data dynamically using the Product Card component created earlier.



***Milestone 13***: **Edit data and auto fill**

In this milestone, we implemented the ability to edit existing product details by adding an edit button to the product card and updating the backend endpoint to handle changes in MongoDB.

We will go through all the changes made, one by one:

1. Add Edit Button on Product Cards:

- Added an "Edit" button to each product card on the frontend.

- The button allows users to initiate the editing process for a specific product.

2. Handle Edit Button Click:

- When the user clicks on the "Edit" button, the product details are passed to a form.

- The form is pre-filled with the current product details, allowing the user to edit the information.

3. Create Backend Endpoint to Handle Update:

- Wrote a backend API endpoint that receives the updated product data.

- The endpoint performs a database query to find the specific product by its unique identifier.

- Once the product is found, it updates the necessary fields in MongoDB with the new data.

4. Implement Form Submission to Update Product:

- Created a form submission process that sends the edited data to the backend endpoint.

- The updated product details are then saved in MongoDB.

5. Display Updated Information:

- Once the data is successfully updated, the frontend dynamically reflects the changes in the product card without requiring a page refresh.


***Milestone 14***: **Added Delete button**

1. Frontend Implementation (UI)

- Delete Button Added:

A "Delete" button was added next to each product in the product list.
The button was styled and placed for easy user interaction.

- Delete Button Functionality:

On clicking the "Delete" button, an event is triggered to send a DELETE request to the backend API with the product's ID.
A confirmation prompt was added to ensure that the user intends to delete the product before performing the operation.

- UX Enhancements:

After a successful deletion, the product is removed from the UI in real-time without needing to reload the page.
Error messages are displayed in case of a failure (e.g., product not found, network error).

2. Backend Implementation (API)

- DELETE Endpoint Created:

A new DELETE route was added to the backend to handle requests for deleting products by their ID.

The endpoint /api/products/:id accepts the product ID as a parameter and deletes the corresponding product from the MongoDB database.

- MongoDB Query:

The backend queries MongoDB using findByIdAndDelete() to find the product by its ID and remove it from the database.

If the product is found, it is deleted, and a success message is returned to the frontend.

If no product with the specified ID exists, a 404 error is returned to inform the user that the product was not found.

- Error Handling:

The backend includes proper error handling to catch any issues (e.g., invalid ID, database errors).
Appropriate HTTP status codes (200 for success, 404 for not found, etc.) are returned based on the outcome.

3. Testing

- Unit Testing:

Unit tests were written for the DELETE endpoint to ensure that it works as expected in various scenarios (e.g., product exists, product does not exist).

Tests verify that the correct HTTP status codes are returned and that the product is actually deleted from MongoDB.

- End-to-End Testing:

Manual testing was performed to ensure that the delete button works correctly in the frontend and that the product is successfully removed from the database.