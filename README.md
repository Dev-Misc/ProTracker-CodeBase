## ScreTask

-  ScreTask API For Task Management Related Stuff. Developers may utilise this API to support the backend of their apps by coding them in the tech stack of their choosing. 
## Tech Stack

**Database :** MongoDB

**Server :** Node, Express , TypeScript

**Frontend :** [Flutter App](https://github.com/Dev-Adnani/ScreTask-Flutter)


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`PORT`

`MONGODB_URL`

`JWT_SECRET`

`CUSTOM_EMAIL`

`CUSTOM_PASS`


## Run Locally

Clone the project

```bash
  git clone https://github.com/Dev-Adnani/ScreTask-Backend
```

Go to the project directory

```bash
  cd ScreTask-Backend
```

Install dependencies

```bash
  npm i
```

Start the server

```bash
  npm run dev
```


## API Reference

- [Base Url](https://scre-task.herokuapp.com/)
- Authorization Key : "Test"


### Authentication

#### Send Email Verification

```http
  POST /auth/send-email-verification
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `useremail` | `string` | **Required**. User's Email |


#### Sign Up 

```http
  POST auth/signup
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `useremail` | `string` | **Required**. User's Email |
| `userpassword` | `string` | **Required**. User's Password |
| `username` | `string` | **Required**. User's Name |
| `userphoto` | `string` | **Required**. User's Profile URL |
| `secretcode` | `string` | **Required**. Secret Code Generated By Server |
| `secretcodeinput` | `string` | **Required**. Secret Code Enterted By User |

#### Login

```http
  POST /auth/login
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `useremail` | `string` | **Required**. User's Email |
| `userpassword` | `string` | **Required**. User's Password |


#### Decode User Data

```http
  GET /auth/verify
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `tokenData` | `authorization` | **Required**. JWT  |

### Tasks

#### Add Tasks

```http
  POST task/add
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `user_id` | `string` | **Required**. User's ID |
| `task_title` | `string` | **Required**. Task's Title |
| `task_desc` | `string` | **Required**. Task's Description |
| `task_type` | `string` | **Required**. Task's Types |
| `task_date` | `string` | **Required**. Task's Date |
| `task_completed` | `boolean` | **Required**. Task's Completed Status |


#### Get Tasks

```http
  GET task/:userId
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userId` | `Parameter` | **Required**. User's ID |

#### Get Completed Task Count

```http
  GET task/count/:userId
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userId` | `Parameter` | **Required**. User's ID |

#### Get Detail Task [Particular Task]

```http
  GET task/detail/:taskId
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `task_id` | `Parameter` | **Required**. Task ID |


#### Get Categories Type Of Task

```http
  POST task/taskType
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `task_type` | `string` | **Required**. Task Types |
| `user_id` | `string` | **Required**. User's ID |


#### Update Tasks

```http
  PUT task/update
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `task_id` | `Parameter` | **Required**. Task ID |
| `task_title` | `string` | **Required**. Task's Title |
| `task_desc` | `string` | **Required**. Task's Description |
| `task_type` | `string` | **Required**. Task's Types |
| `task_date` | `string` | **Required**. Task's Date |
| `task_completed` | `boolean` | **Required**. Task's Completed Status |



#### Delete Task

```http
  DELETE task/delete/:taskId
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `task_id` | `Parameter` | **Required**. Task ID |




## Authors

- [@Dev-Adnani](https://github.com/Dev-Adnani)


## Feedback

If you have any feedback, please reach out to us at devadnani26@gmail.com


## License

[MIT](https://choosealicense.com/licenses/mit/)
