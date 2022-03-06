# TO-DO List API


#### Endpoints

1. User

   - GET `api/user?name=params`
     - Return name and user_id of a user (based on parameters)
   - POST `api/user`
     - Create new User

2. Activity
   - GET `api/activities?name=params`
     - Return all of the user program (based on parameters)
   - POST `api/activities`
     - Add an activity

## API Contract

1. User

- GET `api/user?name=params`

  _Get user id from name parameter_

  Response Example:

  ```json
  {
    "status": "success",
    "message": "",
    "data": {
      "user_id": 1
    }
  }
  ```

- POST `api/user`

  _Create new User_

  Payload Example:

  ```json
  {
    "name": "user1"
  }
  ```

  Response Example :

  ```json
  {
    "status": "success",
    "message": "",
    "data": {
      "id": 1,
      "name": "user1"
    }
  }
  ```

2. Activity

- GET `api/activities?name=params`

  _Get the user activities_

  Response Example:

  ```json
  {
    "status": "success",
    "message": "",
    "data": [
      {
        "activity_name": "Activity #1",
        "end_date": "date_format"
      },
      {
        "activity_name": "Activity #2",
        "end_date": "date_format"
      }
    ]
  }
  ```

- POST `api/activities`

  _Create new User_

  Payload Example:

  ```json
  {
    "user_id": "user1",
    "activity_name": "Activity #1",
    "end_date": "date_format"
  }
  ```

  Response Example :

  ```json
  {
    "status": "success",
    "message": "",
    "data": {
      "name": "Activity #1",
      "end_date": "date_format"
    }
  }
  ```
