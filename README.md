# Mongoose Express CRUD Mastery

## **Assignment Requirements**

**Objective**: Build a Node.js Express application with MongoDB (using Mongoose) to manage user data and their orders. Implement validation using Joi for data integrity.

### **Set up the Project**

- Create a new Node.js Express project.

- Set up a MongoDB database using Mongoose for storing user and order data.

### **Define Data Models**

- Create Mongoose models for User and Order based on the provided data structure.

- Define appropriate data types, validations, and relationships between the User and Order models.

## **Implement CRUD Operations**

## Main Section (50 Marks):

### **User Management:**

#### 1. **Create a new user**

- Endpoint: **POST /api/users**
- Request Body:

```json
{
  "username": "string",
  "fullName": {
    "firstName": "string",
    "lastName": "string"
  },
  "age": "number",
  "email": "string",
  "isActive": "boolean",
  "hobbies": ["string", "string"],
  "address": {
    "street": "string",
    "city": "string",
    "country": "string"
  }
}
```

- Response: Newly created user object.

```json
{
	"success": true,
	"message": "User created successfully!"
	"data" : {
		  "username": "string",
		  "fullName": {
		    "firstName": "string",
		    "lastName": "string"
		  },
		  "age": "number",
		  "email": "string",
		  "isActive": "boolean",
		  "hobbies": ["string", "string"],
		  "address": {
		    "street": "string",
		    "city": "string",
		    "country": "string"
		  }
		}
}
```

#### 2. **Retrieve a list of all users**

- Endpoint: **GET /api/users**

- Response: List of user objects.

```json
{
	"success": true,
	"message": "Users fetched successfully!"
	"data" : [
		{
		  "username": "string",
		  "fullName": {
		    "firstName": "string",
		    "lastName": "string"
		  },
		  "age": "number",
		  "email": "string",
		  "isActive": "boolean",
		  "hobbies": ["string", "string"],
		  "address": {
		    "street": "string",
		    "city": "string",
		    "country": "string"
		  }
		},
		// more objects...
	]
}
```

#### 3. **Retrieve a specific user by ID**

- Endpoint: **GET /api/users/:userId**

- Response: User object.

```json
{
	"success": true,
	"message": "User fetched successfully!"
	"data" : {
		  "username": "string",
		  "fullName": {
		    "firstName": "string",
		    "lastName": "string"
		  },
		  "age": "number",
		  "email": "string",
		  "isActive": "boolean",
		  "hobbies": ["string", "string"],
		  "address": {
		    "street": "string",
		    "city": "string",
		    "country": "string"
		  }
		}
}
```

#### 4. **Update user information**

- Endpoint: **PUT /api/users/:userId**

- Request Body: Updated user data (similar structure as in user creation).

- Response: Updated user object.

```json
{
	"success": true,
	"message": "User updated successfully!"
	"data" : {
		  "username": "string",
		  "fullName": {
		    "firstName": "string",
		    "lastName": "string"
		  },
		  "age": "number",
		  "email": "string",
		  "isActive": "boolean",
		  "hobbies": ["string", "string"],
		  "address": {
		    "street": "string",
		    "city": "string",
		    "country": "string"
		  }
		}
}
```

#### 5. **Delete a user**

- Endpoint: **DELETE /api/users/:userId**

- Response: Success message.

```json
{
	"success": true,
	"message": "User deleted successfully!",
	"data" : null
}
```

## Bonus Section (10 marks):

### **Order Management:**

#### 1. Add New Product in Order

- Append a new product to the order property of an existing user.

- Endpoint: **PUT /api/users/:userId/orders**

- Request Body:

```json
{
    "productName": "string",
	"price": "number",
	"quantity": "number"
}
```

- Response: 

```json
{
	"success": true,
	"message": "Order created successfully!",
	"data" : null
}
```

#### 2. **Retrieve all orders for a specific user**

- Endpoint: **GET /api/users/:userId/orders**

- Response: List of order objects for the specified user.

```json
{
	"success": true,
	"message": "Order fetched successfully!"
	"data" : {
            "orders": [
                {
                    "productName": "Product 1",
                    "price": 23.56,
                    "quantity": 2
                },
                {
                    "productName": "Product 2",
                    "price": 230.56,
                    "quantity": 5
                }
            ]
	    }
}
```

#### 3. **Calculate Total Price of Orders for a Specific User**

- Endpoint: **GET /api/users/:userId/orders/total-price**
- Response: Total price of all orders for the specified user.

```json
{
	"success": true,
	"message": "Total price calculated successfully!",
	"data" : {
            "totalPrice": 454.32
	    }
}
```


## **Validation with Joi**

- Use Joi to validate incoming data for user and order creation and updating operations.
- Ensure that the data adheres to the structure defined in the models.
- Handle validation errors gracefully and provide meaningful error messages in the API responses.

## **Instruction**

1. **Coding Quality:**
    - Write clean, modular, and well-organized code.
    - Follow consistent naming conventions for variables, functions, and routes.
    - Use meaningful names that reflect the purpose of variables and functions.
    - Ensure that the code is readable.
2. **Comments:**
    - Try to provide inline comments to explain complex sections of code or logic.
3. **API Endpoint Adherence:**
    - Strictly follow the provided API endpoint structure and naming conventions.
    - Ensure that the request and response formats match the specifications outlined in the assignment.
4. **Validation and Error Handling:**
    - Implement validation using Joi for both user and order data.
    - Handle validation errors gracefully and provide meaningful error messages in the API responses.
    - Implement error handling for scenarios like user not found, validation errors.
5. **Coding Tools and Libraries:**
    - Avoid the use of AI tools or libraries for generating code. Write the code manually to demonstrate a clear understanding of the concepts.
    - Utilize only the specified libraries like Express, Mongoose, Joi and avoid unnecessary dependencies.
6. **Coding Style:**
    - Consider using linting tools (e.g., ESLint) to enforce coding style and identify potential issues.
    - Ensure there are at least 10 commits in your GitHub repository.

### **Submission:**

- Share the GitHub repository link and the live deployment link as part of your submission.
- Include a README file with clear instructions on how to run the application locally.

### **Deadline:**

- 60 marks: November __, 2023, 11:59 PM
- 50 marks: November __, 2023, 11:59 PM
- 30 marks: After __, November, 11.59PM