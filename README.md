
contiue reading after logo ------> :)
![logonav](https://github.com/Vince-mel/Capstone-backend/assets/137229406/8dcb73b5-8420-4c54-969f-1b1b92e342b6)






                               WAYSTONE BACKEND SERVER


The waystone backend server is an efficient component of waystone application that you can find here -> https://github.com/iam-Igor/food2you](https://github.com/Vince-mel/Capstone-frontend, responsible for handling various backend functionalities, including user authentication, order processing, and communication with external APIs.

Developed using the Spring framework, this server ensures smooth and reliable operation, enabling seamless integration with the frontend client.

Key Features:
User Authentication and Authorization: The backend server provides secure endpoints for user registration, login, and authentication, ensuring that only authorized users can access the application's features.

Posts management: With dedicated endpoints for posts  creation delete and updates, the server facilitates efficient order processing and management, enhancing the overall user experience.

User management: Update your bio in the profile page

Category management: create and delete category 

Comment mangement: Create comment and delete 

Database Management: As and Admin in sinergy whit front end you can delete users and posts, create and delete category and see activity

Data Persistence and Storage: Utilizing Spring Data JPA and relational database management systems

Security Measures: The backend server implements robust security measures, including encryption, input validation, and access control, to protect sensitive user data and prevent unauthorized access or malicious activities.

Installation
1- Clone the repository:

bash $ git clone https://github.com/Vince-mel/Capstone-backend

Environment Variables Configuration
In your root folder create a file named env.properties and add it to .gitignore


Add the values just created in the env.properties file, see example below:

DB_PASSWORD=yourbdpassword

DB_USERNAME=yourpostgresusername

DB_NAME=thenamechosenforthedatabase

JWT_SECRET=thejwtsecretusedforhashingthepasswordsoftheusersTheLongerTheBetter

PORT_SERVER=yourlocalhostportserver

Contributing
If you'd like to contribute to the development of the Food2You-Be_Server, follow these steps:

1- Fork the repository.

2- Create a new branch: bash $ git checkout -b your-branch-name

3- Make your changes and commit them: bash $ git commit -m 'Description of your changes'

4- Push your changes to your fork: bash $ git push origin your-branch-name

5- Submit a pull request to the main repository.

6- Do not forget to star the project if you liked it :)

API Reference:

User Controller API Reference

Get All Users

URL: /api/users
Method: GET
Success Response:
Code: 200 OK
Content:
json

[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com"
  },
  {
    "id": 2,
    "name": "Jane Doe",
    "email": "jane@example.com"
  }
]

Get Single User by ID

URL: /api/users/{userId}
Method: GET
URL Params: userId=[long]
Success Response:
Code: 200 OK
Content:
json

{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com"
}

Update User by ID

URL: /api/users/{userId}
Method: PUT
URL Params: userId=[long]
Request Body:
json

{
  "name": "John Updated",
  "email": "johnupdated@example.com"
}
Success Response:
Code: 200 OK
Content:
json

{
  "id": 1,
  "name": "John Updated",
  "email": "johnupdated@example.com"
}

Delete User by ID

URL: /api/users/{userId}
Method: DELETE
URL Params: userId=[long]
Success Response:
Code: 200 OK
Content:
json

{
  "message": "User with User id 1 has been deleted",
  "success": true
}

Post Controller API Reference

Create New Post

URL: /api/user/{userId}/category/{categoryId}/posts
Method: POST
URL Params: userId=[long], categoryId=[long]
Request Body:
json

{
  "title": "New Post Title",
  "content": "Post content here",
  "imageName": "image.jpg"
}
Success Response:
Code: 201 CREATED
Content:
json

{
  "id": 1,
  "title": "New Post Title",
  "content": "Post content here",
  "imageName": "image.jpg",
  "userId": 1,
  "categoryId": 1
}

Get All Posts

URL: /api/posts
Method: GET
URL Params: Optional: pageSize=[integer], pageNumber=[integer], sort=[string], order=[string]
Success Response:
Code: 200 OK
Content:
json

{
  "posts": [
    {
      "id": 1,
      "title": "Post Title",
      "content": "Post content",
      "imageName": "image.jpg"
    }
  ],
  "totalItems": 1,
  "totalPages": 1,
  "currentPage": 0
}

Delete Post by ID

URL: /api/posts/{postId}
Method: DELETE
URL Params: postId=[long]
Success Response:
Code: 200 OK
Content:
json

{
  "message": "Post with id 1 has been deleted",
  "success": true
}

Update Post

URL: /api/posts/{postId}
Method: PUT
URL Params: postId=[long]
Request Body:
json

{
  "title": "Updated Post Title",
  "content": "Updated post content",
  "imageName": "updated-image.jpg"
}
Success Response:
Code: 200 OK
Content:
json

{
  "id": 1,
  "title": "Updated Post Title",
  "content": "Updated post content",
  "imageName": "updated-image.jpg",
  "userId": 1,
  "categoryId": 1
}


Category Controller API Reference


Create New Category
URL: /api/category/
Method: POST
Request Body:
json

{
  "name": "New Category",
  "description": "Category Description"
}
Success Response:
Code: 201 CREATED
Content:
json


{
  "id": 1,
  "name": "New Category",
  "description": "Category Description"
}

Get All Categories

URL: /api/category/
Method: GET
Success Response:
Code: 200 OK
Content:
json

[
  {
    "id": 1,
    "name": "Category 1",
    "description": "Description 1"
  },
  {
    "id": 2,
    "name": "Category 2",
    "description": "Description 2"
  }
]

Comment Controller API Reference

Create New Comment

URL: /api/post/{postId}/comment
Method: POST
URL Params: postId=[long]
Request Body:
json

{
  "text": "This is a comment",
  "postId": 1
}
Success Response:
Code: 201 CREATED
Content:
json

{
  "id": 1,
  "text": "This is a comment",
  "postId": 1
}

Delete Comment by ID

URL: /api/comment/{commentId}
Method: DELETE
URL Params: commentId=[long]
Success Response:
Code: 200 OK
Content:
json

{
  "message": "Comment with id 1 has been deleted",
  "success": true
}

Questa documentazione API fornisce un'overview generale su come interagire con i vari endpoint. 




