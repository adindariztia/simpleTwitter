# <center> Halo! </center>
### As said on description, this is a twitter-like backend (super simple edition). Features are explained below.

## Before you start


- **app.py** as a main file to execute the whole back end. Run this file first by typing `py app.py`

- **twitter.py** contains a so-called twitter's API. Further explanation after this section

- **data.txt** contains user data as seen below:
    ```
     [{
    "username": "John",
    "email": "john@haha.com",
    "password": "Hoooa123",
    "fullname": "John rukmana"
    },
    {
    "username": "jeff",
    "email": "jeff@haha.com",
    "password": "Hahaha123",
    "fullname": "John rukmana"
    }] 
    ```

- **tweet.txt** contains recorded tweets
    ```
    [{
    "email": "john@haha.com",
    "tweet": "Ini ceritanya tweet Twitter yah"
    },
    {
        "email": "jeff@haha.com",
        "tweet": "Ini ceritanya tweet Twitter yah"
    }]
    ```


## Features
- **sign up** a post-type http request. Send request.json via postman/insomnia containing these informations:
    ```
    {
    "username": "John",
    "email": "john@haha.com",
    "password": "Hoooa123",
    "fullname": "John rukmana"
    }
    ```
    this information will be stored in data.txt. Keep in mind that we use email and password information in login.
    ```
    for user in json.load(json_file):       
        if (user['email'] == request.json["email"]):
            if (user['password'] == request.json["password"]):
                return "Login successful!"
            else:
                return "email/password salah" 
    return "user does not exist"
    ```
- **view all tweet/user** a get-type http request that will show all tweet/users from tweet.txt/data.txt
- **post a tweet** a post-type http request, allow recognized user (according to data.txt) to post tweets
- **delete tweet** delete tweets
