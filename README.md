# Task Manager API

Tasks list app that enables you to create a user account and start writing down what you have to do with CRUD (This repo is backend.).



### Tech stack

- JavaScript
- NodeJS
- MongoDB
- JWT



### **Features**

- Create a user account.

- Create, edit and delete tasks.

- Sort tasks by date.

- Choose count of tasks to see.

- Update your account information

- Sending automated email using the SendGrid API.

  

## Running locally

```
$ git clone https://github.com/ahmedsamirdev/task-manager.git
$ cd task-manager
$ yarn
$ yarn dev
```

Make sure to Create a `dev.env` file inside a config folder in the root of the project with the following:

##### Configuration

```
PORT=
SENDGRID_API_KEY=
MONGODB_URL=
JWT_SECRET=
```



## Endpoints

Requires a valid JWT token as ` Authorization: Bearer <jwt_token>)`

- Authorization
  - Create user - `POST /users`
  - Login user - `POST /users/login`
- User action
  - Logout user - `POST /users/logout`
  - Logout all users - `POST /users/logoutAll`
  - Read profile - `GET /users/me`
  - Update user - `PATCH /users/me`
  - Delete user - `DELETE /users/me`
  - Upload avatar - `POST /users/me/avatar`
  - Delete avatar - `DELETE /users/me/avatar`
  - Get user avatar - `GET /users/:id/avatar`
- CRUD Task 
  - Create task - `POST /tasks`
  - Read tasks - `GET /tasks`
    - completed - `Boolean`
    - sortBy - `<field_name>:asc|desc`
    - limit - `Number`
    - skip - `Number`
  - Read task - `GET /tasks/:id`
  - Update task - `PATCH /tasks/:id`
  - Delete task - `DELETE /tasks/:id`

[Backend API](https://task-manager-api-as.herokuapp.com/)
