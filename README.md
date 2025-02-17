# Employee Management System (GraphQL, Node.js, Express, Apollo, MongoDB)

# Soham Chaudhari 101414821

## Overview
The Employee Management System (EMS) is a backend application built using **Node.js, Express, GraphQL (Apollo Server), and MongoDB**. This system provides CRUD operations for managing employees through GraphQL queries and mutations. The project follows best practices for full-stack development and ensures data integrity through proper validation and error handling.

## Features
- Employee CRUD operations (Create, Read, Update, Delete)
- GraphQL API using Apollo Server
- MongoDB database with Mongoose ODM
- Input validation and error handling
- Authentication and Authorization (if implemented)
- GraphQL Playground for testing queries and mutations

## Tech Stack
- **Node.js** - Runtime environment
- **Express.js** - Web framework for Node.js
- **GraphQL** - API query language
- **Apollo Server** - GraphQL server
- **MongoDB** - NoSQL database
- **Mongoose** - ODM for MongoDB
- **dotenv** - Environment variable management
- **nodemon** - Development server monitoring

## Installation

### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (LTS recommended)
- [MongoDB](https://www.mongodb.com/)
- [Git](https://git-scm.com/)

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/Soham714/comp3133_101414821_assignment1.git
   cd comp3133_101414821_assignment1
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file in the root directory and add the following environment variables:
   ```env
   MONGO_URI=your_mongodb_connection_string
   PORT=4000
   ```
4. Start the development server:
   ```sh
   npm run dev
   ```
   The server will run at `http://localhost:4000/graphql`.

## Usage
### GraphQL Playground
Once the server is running, open **GraphQL Playground** at:
```
http://localhost:4000/graphql
```
Use it to test queries and mutations.

### Example Queries & Mutations
#### Create Employee
```graphql
mutation {
  addEmployee(name: "John Doe", position: "Software Engineer", department: "IT") {
    id
    name
    position
    department
  }
}
```
#### Get All Employees
```graphql
query {
  employees {
    id
    name
    position
    department
  }
}
```
#### Update Employee
```graphql
mutation {
  updateEmployee(id: "EMPLOYEE_ID", position: "Senior Engineer") {
    id
    name
    position
  }
}
```
#### Delete Employee
```graphql
mutation {
  deleteEmployee(id: "EMPLOYEE_ID") {
    message
  }
}
```

## Project Structure
```
├── src
│   ├── models
│   │   ├── Employee.js
│   ├── resolvers
│   │   ├── employeeResolver.js
│   ├── schema
│   │   ├── typeDefs.js
│   ├── index.js
├── .env
├── package.json
├── README.md
```

## Testing
Test the API using **Postman** or **GraphQL Playground**.

## Version Control
Use **GitHub** for version control. Make commits with meaningful messages.

## Future Enhancements
- Implement authentication (JWT)
- Add role-based access control
- Improve logging and monitoring

## License
This project is licensed under the MIT License.

## Contributors
- Soham Chaudhari

