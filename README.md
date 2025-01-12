INDUSTRIAL TRAINING PROJECT
===========================

At **WebGuru Infosystems**


eCommerce REST API
==================

This REST API is built using Node.js and Express.js to facilitate eCommerce functionalities such as user authentication, product management, review management, and order management. It allows users to register, log in, manage products, create and manage reviews, and place and manage orders. JWT-based authentication ensures secure access to the system.

Documentation
-----------

Access the documentation for this project:
[View](https://ecomapi-project.researchdevs.in/)

Technology Used
---------------

*   **Backend**: Node.js, Express.js
*   **Database**: MongoDB, Mongoose
*   **Authentication**: JWT (JSON Web Tokens)
*   **Image Upload**: Cloudinary API
*   **Environment Management**: dotenv for environment variable management

Roadmap
-------

*   User Authentication - Secure user registration, login, and logout with JWT.
*   Product Management - CRUD operations for products, including image uploads.
*   Review Management - Manage product reviews with CRUD operations.
*   Order Management - Create, update, and retrieve orders.
*   API Testing - Ensure robustness and security with unit and integration tests.
*   Deployment - Deploy the API on cloud platforms like Heroku or AWS.
*   Future Enhancements - Adding features like payment gateway integration, order history, and advanced user roles.

Features of the Project
-----------------------

*   **User Registration and Authentication**: Users can register, log in, and securely authenticate via JWT.
*   **Product CRUD**: Create, update, delete, and retrieve product details, including image uploads.
*   **Review Management**: Allow users to create, update, delete, and retrieve reviews for products.
*   **Order Management**: Users can place, update, and retrieve orders.
*   **JWT-based Authentication**: Secure access for users with token-based authentication.

Features of the Project
-----------------------

*   **User Registration and Authentication**: Users can register, log in, and securely authenticate via JWT.
*   **Product CRUD**: Create, update, delete, and retrieve product details, including image uploads.
*   **Review Management**: Allow users to create, update, delete, and retrieve reviews for products.
*   **Order Management**: Users can place, update, and retrieve orders.
*   **JWT-based Authentication**: Secure access for users with token-based authentication.

Feature Solutions
-----------------

We provide tailored solutions to meet specific needs, ensuring enhanced functionality, performance, and user experience. Key features include:

*   **Customization**: Tailor features to meet unique business or user requirements.
*   **Scalability**: Support for future growth and expansion with seamless integration.
*   **Security**: Robust security protocols to protect data and ensure safe transactions.
*   **User-Friendly Interface**: Intuitive design for improved user engagement.
*   **Real-Time Performance**: Fast, efficient solutions for real-time data processing.

Test Cases
----------

### 1\. User Authentication Tests

#### Test Case 1.1: User Registration

Send a POST request to `/register` with valid user details (e.g., email, password).

            Input:
            {
              "email": "user@example.com",
              "password": "password123"
            }
            

Expected Result:

*   Response status: 201 (Created)
*   Response message: "User successfully registered."
*   User added to the database.

#### Test Case 1.2: User Registration (Missing Fields)

Send a POST request to `/register` with missing fields (e.g., missing password).

            Input:
            {
              "email": "user@example.com"
            }
            

Expected Result:

*   Response status: 400 (Bad Request)
*   Error message: "Password is required."

#### Test Case 1.3: User Login

Send a POST request to `/login` with valid credentials (email and password).

            Input:
            {
              "email": "user@example.com",
              "password": "password123"
            }
            

Expected Result:

*   Response status: 200 (OK)
*   Response includes a JWT token for authentication.

#### Test Case 1.4: User Login (Invalid Credentials)

Send a POST request to `/login` with invalid credentials.

            Input:
            {
              "email": "user@example.com",
              "password": "wrongpassword"
            }
            

Expected Result:

*   Response status: 401 (Unauthorized)
*   Error message: "Invalid email or password."

### 2\. Product Management Tests

#### Test Case 2.1: Add Product (Admin)

Send a POST request to `/products` to add a new product with valid data (only accessible by admin).

            Input:
            {
              "name": "Laptop",
              "price": 1200,
              "category": "Electronics",
              "description": "High-end gaming laptop"
            }
            

Expected Result:

*   Response status: 201 (Created)
*   Response includes the product details.
*   Product added to the database.

#### Test Case 2.2: Add Product (Without Admin Privileges)

Send a POST request to `/products` to add a new product without admin privileges.

            Input:
            {
              "name": "Phone",
              "price": 500,
              "category": "Electronics"
            }
            

Expected Result:

*   Response status: 403 (Forbidden)
*   Error message: "Admin privileges required."

#### Test Case 2.3: Get Product List

Send a GET request to `/products` to retrieve the list of products.

            Input: No input required.
            

Expected Result:

*   Response status: 200 (OK)
*   Response includes an array of products with details like name, price, and category.

### 3\. Review Management Tests

#### Test Case 3.1: Add Product Review

Send a POST request to `/reviews` to add a review for a product.

            Input:
            {
              "productId": 1,
              "rating": 5,
              "review": "Great product!"
            }
            

Expected Result:

*   Response status: 201 (Created)
*   Response includes the review details.

#### Test Case 3.2: Get Product Reviews

Send a GET request to `/reviews?productId=1` to retrieve all reviews for a product.

            Input: No input required.
            

Expected Result:

*   Response status: 200 (OK)
*   Response includes a list of reviews for the product.

Error Codes
-----------

The following are the possible error codes returned by the API:

*   **400** - Bad Request
*   **401** - Unauthorized
*   **404** - Not Found
*   **500** - Internal Server Error

Project Review
--------------

### Overview

This eCommerce REST API is built using Node.js and Express.js to provide essential functionalities for an online store. It focuses on user authentication, product management, review management, and order management. The system leverages JWT-based authentication to ensure secure access and facilitate smooth user interactions. This API is designed to manage users, products, reviews, and orders efficiently, with roles and permissions to secure sensitive operations.

### Strengths

*   **Scalability:** The REST API is designed to be scalable, making it suitable for handling a growing number of products, users, and orders.
*   **Security:** JWT authentication ensures that only authorized users can access and perform actions in the system.
*   **User-Centric:** Provides an intuitive user interface for product browsing, reviews, and order management.
*   **Efficient Management:** Simplifies product and review management for administrators, providing a secure and structured way to manage data.

### Challenges

*   **Error Handling:** Improved error handling and clear responses for invalid requests can be implemented for better user experience.
*   **Rate Limiting:** To prevent abuse of the system, implementing rate limiting for API requests could enhance security and reduce the risk of DDoS attacks.
*   **Extensibility:** Further features like payment gateway integration and shipment tracking could be considered in future updates.

### Future Enhancements

*   **Payment Integration:** Adding a payment gateway (e.g., PayPal, Stripe) for handling transactions.
*   **Inventory Management:** Integrating real-time stock tracking and alerts for low stock levels.
*   **Mobile App Integration:** Building a mobile app that interacts with the API to provide a seamless shopping experience on smartphones.
*   **Product Search and Filter:** Implementing advanced search and filter functionality for products based on various criteria like price range, category, and ratings.

Conclusion
----------

This eCommerce REST API built using Node.js and Express.js offers a secure, scalable, and efficient solution for managing users, products, reviews, and orders. By implementing JWT authentication, it ensures secure access to the system. While the project successfully meets the essential eCommerce requirements, there is room for future enhancements, such as adding payment gateway integrations, inventory management, and mobile app support. Overall, the system lays a solid foundation for building a robust online store, and its flexibility allows for future growth and improvements.

Reference
---------

*   [Express.js Official Documentation](https://expressjs.com/)
*   [JWT Official Introduction](https://jwt.io/introduction/)
*   [MongoDB Official Website](https://www.mongodb.com/)
*   [JavaScript Modules - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
*   [Postman API Testing Tool](https://www.postman.com/)
*   [DigitalOcean Tutorials](https://www.digitalocean.com/community/tutorials)
*   [W3Schools - Web Development Tutorials](https://www.w3schools.com/)

© 2025 API Documentation. All Rights Reserved.
Created by: Sourav Sharma, Rajankita Saha, Subhayan Mandal, Swagata Das, Kartik Paul
